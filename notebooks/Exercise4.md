
# Exercise 4: Fourier and Radon filtering
In this exercise we will look at seismic data in different domains and investigate how we can exploit behaviour of different kinds of noise in these domains to design filters.

Contents:
- Data
- Temporal Fourier transform
- f-k filtering
- Radon transform
- Parabolic Radon transform



```julia
using PyPlot, SeisIO
```

**Data**

We use a single midpoint gather of the data used in the previous exercises: shot.segy (no big endian this time).


```julia
# Dowload and adapt path
shot = segy_read("./data_segy/shot.segy")

shot_data = Float32.(shot.data)

h = get_header(shot, "SourceX", scale=false) - get_header(shot, "GroupX", scale=false)
dt = get_header(shot, "dt")[1]/1e6
nt = get_header(shot, "ns")[1]
T = 0:dt:(nt -1)*dt
```

    BinaryFileHeader:
                                    Job:         1
                                   Line:         1
                                   Reel:         1
                   DataTracePerEnsemble:         1
              AuxiliaryTracePerEnsemble:         0
                                     dt:      4000
                                 dtOrig:         0
                                     ns:      1001
                                 nsOrig:         0
                       DataSampleFormat:         1
                           EnsembleFold:         0
                           TraceSorting:         0
                        VerticalSumCode:         0
                    SweepFrequencyStart:         0
                      SweepFrequencyEnd:         0
                            SweepLength:         0
                              SweepType:         0
                           SweepChannel:         0
                  SweepTaperlengthStart:         0
                    SweepTaperLengthEnd:         0
                              TaperType:         0
                   CorrelatedDataTraces:         0
                             BinaryGain:         0
                AmplitudeRecoveryMethod:         0
                      MeasurementSystem:         0
                  ImpulseSignalPolarity:         0
                  VibratoryPolarityCode:         0
               SegyFormatRevisionNumber:         0
                   FixedLengthTraceFlag:         0
              NumberOfExtTextualHeaders:         0
    
    
    
    1705444 3600 1001


    [1m[33mWARNING: [39m[22m[33mFixed length trace flag set in stream: IOBuffer(data=UInt8[...], readable=true, writable=false, seekable=true, append=false, size=1705444, maxsize=Inf, ptr=3601, mark=-1)[39m





    0.0:0.004:4.0




```julia
imshow(shot_data, vmin=-1, vmax=1, cmap="Greys", extent=[h[end], h[1], T[end], T[1]], aspect=1000)
xlabel("offset [m]");ylabel("time [s]");
```


![png](Exercise4_files/Exercise4_4_0.png)


**Temporal Fourier transform**

We can use fftrl to perform a Fourier transform along the temporal direction. The power spectrum (i.e., the absolute value of the transformed data) looks like


```julia
function fftrl(a, t, mode)
    # fft for real-valued vectors
    #
    # Tristan van Leeuwen, 2012
    # tleeuwen@eos.ubc.ca
    #
    # use:
    #   [b,f] = fftrl(a,t,mode)
    #
    # input:
    #   a - input data
    #   t - time vector
    #   mode: 1: forward, -1:inverse
    #
    # output:
    #   b - vector

    nt = length(t)
    dt = t[2] - t[1]
    nf = Int(floor(nt/2)) + 1
    tmax = t[end] - t[1]
    f = 0:1/tmax:.5/dt
    if mode == 1
        b = fft(a,1)
        b = b[1:nf,:]
    elseif mode == -1
        a = [a;conj(a[Int(ceil(nt/2)):-1:2,:])]
        b = ifft(a, 1)
        b = real(b)
    else
        error("Unknown mode")
    end

    return b, f
end

```




    fftrl (generic function with 1 method)




```julia
Data_fh, f = fftrl(shot_data, T, 1)
```




    (Complex{Float32}[0.684434+0.0im 0.971781+0.0im … 0.0969428+0.0im 0.00433278+0.0im; -0.701183-0.451787im -0.412326-0.460599im … -1.3078-0.497307im -1.40236-0.48802im; … ; -0.121274+0.000705719im -0.0863834-0.000402451im … 0.157795-0.00114059im 0.110151-0.000276089im; -0.122033+0.000601768im -0.0849152-0.000236511im … 0.159012-0.000580788im 0.109696-0.000192404im], 0.0:0.25:125.0)




```julia
imshow(abs.(Data_fh), cmap="jet", extent=[h[end], h[1], f[end], f[1]], aspect=20)
xlabel("offset [m]");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_8_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')



**f-k filtering**
A Fourier transform along both time and offset direction is often referred to as an  transform. We can use fktran. The powerspectrum looks like


```julia
function fktran(a,t,x,mode)
    """
    f-k transform for real-values input.

    use:
        b, f, k = fktran(a,t,x,mode)

    input:
        a - matrix in t-x domain (nt x nx)
        t - time vector
        x - x vector
        mode - 1:forward, -1:inverse
    """

    nt = length(t)
    nx = length(x)

    dt = t[2]-t[1]
    dx = x[2] - x[1]

    xmax = x[end] - x[1]
    tmax = t[end] - t[1]


    f = 0:1/tmax:.5/dt
    k = -.5/dx:1/xmax:.5/dx

    nf = length(f)
    if mode == 1
        b = fft(a, 1)
        b = b[1:nf, :]
        b = ifft(b, 2)
        b = circshift(b,[0 ceil(Int, nx/2)-1]);
    elseif mode == -1
        b = circshift(a,[0 floor(Int, nx/2)+1]);
        b = fft(b, 2)
        b = ifft([b;conj(b[end:-1:2,:])], 1)
        b = real(b)
    else
        error("unknown mode")
    end
    return b, f, k
end
```




    fktran (generic function with 1 method)




```julia
Data_fk, fk, kx = fktran(shot_data, T, h, 1)
```




    (Complex{Float32}[0.00217381+0.375868im -0.00371527-0.375896im … -0.00371557+0.375898im 0.00217354-0.375864im; -0.0666401+0.378171im 0.0651375-0.378642im … -0.072564+0.377115im 0.0710575-0.377542im; … ; 0.00330043+0.400901im -0.00697034-0.400875im … -0.0029994+0.40092im -0.000692182-0.400906im; 0.00196619+0.400894im -0.00564895-0.400912im … -0.00433144+0.400905im 0.000641863-0.400899im], 0.0:0.25:125.0, 0.05:-0.00025:-0.05)




```julia
imshow(abs.(Data_fk), cmap="jet", extent=[kx[end], kx[1], f[end], f[1]], aspect=.001)
xlabel("wavenumber [1/m");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_12_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')




```julia
back, _, _ = fktran(Data_fk, fk, kx, -1)
imshow(back, vmin=-1, vmax=1, cmap="Greys", extent=[h[end], h[1], T[end], T[1]], aspect=1000)
xlabel("offset [m]");ylabel("time [s]");
```


![png](Exercise4_files/Exercise4_13_0.png)



```julia
size(shot_data)
```




    (1001, 401)



# Questions:
Subsample the data in the offset direction and look at the Fourier transform. (Hint: use Data[:,1:n:end] and h[1:n:end] where n is the number of times you want to subsample).

- What do you see?
- Why is it important to have a good receiver sampling?

A filter is simply a multiplicative factor applied in some transform domain, typically \(f-h\) or \(f-k\), followed by an inverse transform. For example, a band-pass filter in the \(f-h\) domain filters out higher temporal frequencies by setting them to zero. A simple band-pass filter looks like this:




```julia
F_hp = ones(length(f),length(h))
F_hp[(f.<5) .| (f.>20.),:] = 0

imshow(F_hp, extent=[h[end], h[1], f[end], f[1]], aspect=20)
colorbar()
xlabel("offset [m]");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_17_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')



The filtered data looks like this


```julia
imshow(fftrl(F_hp.*Data_fh, f, -1)[1], cmap="Greys", vmin=-1, vmax=1, extent=[h[end], h[1], T[end], T[1]], aspect=1000)
xlabel("offset [m]");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_19_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')



Do you see the artifacts? A way to reduce these artifacts is to smooth the filter. We can do this by convolving the filter with a triangular smoothing kernel. This is implemented in the function smooth_2D. The result looks like this:


```julia
# Pkg.add("Images") of you do not alread yhave it
using Images

function smooth_2D(input, n1, n2)
    t1 = [1:n1; n1-1:-1:1]/n1^2
    t2 = [1:n2; n2-1:-1:1]/n2^2
    kernel = t1 * t2'
    return imfilter(input, centered(kernel))
end
```




    smooth_2D (generic function with 1 method)




```julia
F_hp_smooth = smooth_2D(F_hp, 5, 1)
imshow(F_hp_smooth, extent=[h[end], h[1], f[end], f[1]], aspect=20)
colorbar()
xlabel("offset [m]");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_22_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')




```julia
imshow(fftrl(F_hp_smooth.*Data_fh, f, -1)[1], cmap="Greys", vmin=-1, vmax=1, extent=[h[end], h[1], T[end], T[1]], aspect=1000)
xlabel("offset [m]");ylabel("frequency [Hz]")

```


![png](Exercise4_files/Exercise4_23_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')



A (smoothed) filter in the \(f-k\) domain may look like this


```julia
ff = [fi for fi in f, kxi in kx]
kkx = [kxi for fi in f, kxi in kx]
F_kx = zeros(length(fk),length(kx))

F_kx[(ff -1e3 * abs.(kkx) .> 5) .& (ff.<60)] = 1

F_kx = smooth_2D(F_kx, 5, 5)

imshow(F_kx, cmap="jet", extent=[kx[end], kx[1], f[end], f[1]], aspect=.001)
xlabel("wavenumber [1/m");ylabel("frequency [Hz]")
```


![png](Exercise4_files/Exercise4_25_0.png)





    PyObject Text(24,0.5,'frequency [Hz]')



# Questions

Describe how you would design filters to clean up shot gathers shot_noise1 and shot_noise2. (hint: look the f-k transform and compare to the orinigal data)
Try it and compare the result with the original shot gather.

# Radon transform
The Radon tranform performs sums along lines with different intercepts $\tau$) and slopes $p$. Hence, it is sometimes refered to as the $\tau-p$ transform in geophysics.

$\hat{d}(\tau,p) = \int\mathrm{d}h\, d(t + ph, h)$

The transform is implemented in the function lpradon.

To get an idea of what this transform does, we consider the simple example in lines.segy.




```julia
function lpradon(input, t, h, q, power, mode)
    # linear and parabolic Radon transform and its adjoint.
    #
    # Tristan van Leeuwen, 2012
    # tleeuwen@eos.ubc.ca
    #
    # use:
    #   out = lpradon(input,t,h,q,power,mode)
    #
    # input:
    #   input - input matrix of size (length(t) x length(h)) for forward, (length(t) x length(q)) for adjoint)
    #   t     - time vector in seconds 
    #   h     - offset vecror in meters
    #   q     - radon parameter
    #   power - 1: linear radon, 2: parabolic radon
    #   mode  - 1: forward, -1: adjoint
    #
    # output:            println(size(L))
    #   output matrix of size (length(t) x length(q)) for forward, (length(t) x length(h)) for adjoint)
    #
    #

    dt   = t[2] - t[1]
    nt   = length(t)
    nh   = length(h)
    nq   = length(q)
    nfft = 2*(nextpow2(nt))
    
    input_padded = zeros(nfft, size(input)[2])
    input_padded[1:size(input)[1], :] = input[:, :]
    
    
    if mode == 1

        input_padded  = fft(input_padded, 1)
        out = zeros(Complex{Float64}, nfft, nq)

        for k = 2:Int(floor(nfft/2))
            f = 2.*pi*(k-1)/nfft/dt
            L = exp.(im*f*(h.^power)*q')
            tmp = input_padded[k,:].'*L
            out[k,:] = tmp
            out[nfft + 2 - k, :] = conj(tmp)
        end
        out = real(ifft(out, 1))
        out = out[1:nt, :]

    else

        input_padded  = fft(input_padded,1)
        out = zeros(Complex{Float64}, nfft, nh)

        for k = 2:Int(floor(nfft/2))
            f = 2.*pi*(k-1)/nfft/dt
            L = exp.(im*f*(h.^power)*q')
            tmp = input_padded[k,:].'*L'
            out[k,:] = tmp
            out[nfft+2-k,:] = conj(tmp)
        end

        out = real(ifft(out,1))
        out = out[1:nt, :]

    end

    return out
end
```




    lpradon (generic function with 1 method)




```julia
# Dowload and adapt path
shot_radon = segy_read("./data_segy/lines.segy")

A = Float32.(shot_radon.data)

h = get_header(shot_radon, "SourceX", scale=false) - get_header(shot, "GroupX", scale=false)
dt = get_header(shot_radon, "dt")[1]/1e6
nt = get_header(shot_radon, "ns")[1]
T = 0:dt:(nt -1)*dt
```

    BinaryFileHeader:
                                    Job:         1
                                   Line:         1
                                   Reel:         1
                   DataTracePerEnsemble:         1
              AuxiliaryTracePerEnsemble:         0
                                     dt:      4000
                                 dtOrig:         0
                                     ns:      1001
                                 nsOrig:         0
                       DataSampleFormat:         1
                           EnsembleFold:         0
                           TraceSorting:         0
                        VerticalSumCode:         0
                    SweepFrequencyStart:         0
                      SweepFrequencyEnd:         0
                            SweepLength:         0
                              SweepType:         0
                           SweepChannel:         0
                  SweepTaperlengthStart:         0
                    SweepTaperLengthEnd:         0
                              TaperType:         0
                   CorrelatedDataTraces:         0
                             BinaryGain:         0
                AmplitudeRecoveryMethod:         0
                      MeasurementSystem:         0
                  ImpulseSignalPolarity:         0
                  VibratoryPolarityCode:         0
               SegyFormatRevisionNumber:         0
                   FixedLengthTraceFlag:         0
              NumberOfExtTextualHeaders:         0
    
    
    
    1705444 3600 1001


    [1m[33mWARNING: [39m[22m[33mFixed length trace flag set in stream: IOBuffer(data=UInt8[...], readable=true, writable=false, seekable=true, append=false, size=1705444, maxsize=Inf, ptr=3601, mark=-1)[39m





    0.0:0.004:4.0




```julia
imshow(A, vmin=-.1, vmax=.1, cmap="Greys", extent=[h[end], h[1], T[end], T[1]], aspect=1000)
xlabel("offset [m]");ylabel("time [s]");
```


![png](Exercise4_files/Exercise4_30_0.png)



```julia
# which p-values
p = 1e-3.*(-3:.05:3)

# transform
A_tp = lpradon(A, T, h, p, 1, 1)

```




    1001×121 Array{Float64,2}:
     0.000378078  0.000384182   0.000384585  …  0.000202505   0.000644788
     0.000376368  0.000389721   0.00037549      0.000144312   0.000541559
     0.000387413  0.000381872   0.000383162     0.000133913   0.000409034
     0.000390602  0.000388732   0.000380008     0.000201181   0.000262995
     0.00040214   0.000383436   0.000392553     0.000302437   0.000157082
     0.00040122   0.000393219   0.000391394  …  0.000439509   0.000100834
     0.000405988  0.000390277   0.000402393     0.000551232   0.000125599
     0.000398302  0.000401124   0.000397027     0.000636942   0.000208975
     0.00039937   0.000397851   0.000403059     0.000648591   0.000347769
     0.00039261   0.000407363   0.000394245     0.000611003   0.000491774
     0.00039947   0.000402683   0.000400071  …  0.000507467   0.000622865
     0.000401411  0.000411663   0.000394785     0.00039216    0.000693264
     0.000417296  0.000408056   0.000406892     0.000268286   0.000703196
     ⋮                                       ⋱                ⋮          
     0.000378107  0.000381697  -0.000934809     0.000386704   0.000286472
     0.000374914  0.000389452  -0.000570546  …  0.000391708   5.61129e-5 
     0.000389898  0.000381116  -0.000301544     0.000381055  -9.33017e-5 
     0.000387139  0.000386579  -9.14174e-5      0.000384115  -0.000125689
     0.00039709   0.000377236   4.99588e-5      0.000373351  -3.12507e-5 
     0.000387373  0.000383037   0.000159012     0.00037831    0.000163966
     0.000389431  0.000375596   0.000224376  …  0.000370853   0.000415252
     0.000375596  0.000383775   0.000279658     0.000379835   0.000655951
     0.000377186  0.000378578   0.00030907      0.000375911   0.0008319  
     0.000368403  0.00038769    0.00034119      0.000387262   0.000893315
     0.000376956  0.000382018   0.000355017     0.000383702   0.000832146
     0.000376036  0.000389199   0.000375041  …  0.000393598   0.00065546 




```julia
# plot
imshow(A_tp, vmin=-.25, vmax=.25, cmap="Greys", extent=[p[1], p[end], T[end], T[1]], aspect=.001)
xlabel("slowness [s/m]");ylabel("time [s]");

```


![png](Exercise4_files/Exercise4_32_0.png)


#  Questions
Can you interpret the results?
Describe how you would design `filters` in the $\tau-p$ domain to separate the different events.
Try it. Use the `adjoint` option of the transform to transform back to the physical domain.
