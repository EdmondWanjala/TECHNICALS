        DIGITAL SIGNAL PROCESSING (DSP)
Digital Signal Processing (DSP) is the processing of signals represented as sequences of numerical samples using digital systems such as microcontrollers, microprocessors, DSP processors, FPGAs and computers.
A digital signal is represented as:
    x[n]
Where:
x = signal amplitude.
n = discrete-time sample index.
DSP involves mathematical algorithms that manipulate digital samples to achieve a desired result.
  Main Objectives of DSP;
- Noise reduction: remove unwanted disturbances.
- Filtering: select or suppress particular frequency components.
- Signal enhancement: improve signal quality.
- Signal analysis: study signal characteristics.
- Feature extraction: identify important signal properties.
- Signal detection: determine the presence of specific signals.
- Signal estimation: estimate unknown signal parameters.
- Compression: reduce storage and transmission requirements.
- Signal reconstruction: recover signals from sampled data.
- Signal transformation: convert signals between different representations.
  Applications of DSP;
- Digital communication and wireless networks.
- Audio and speech processing.
- Radar and sonar systems.
- Medical signal processing (ECG, EEG).
- Robotics and autonomous systems.
- Digital image and video processing.
- Industrial automation.
- Sensor data acquisition.
- Embedded systems.
- Navigation and positioning systems.

 DIGITAL SIGNAL REPRESENTATION
  Discrete-Time Signals;
A discrete-time signal is a sequence of values defined at specific time intervals.
Representation:
    x[n] = x(nTs)
Where:
Ts = sampling period.
n = integer sample index.
  Digital Signals;
Digital signals have discrete-time indices and quantized amplitude values, commonly represented in binary.
A digital signal is therefore both:
- Discrete in time.
- Discrete in amplitude.
  Sampling;
Sampling converts a continuous-time signal into a discrete-time sequence by measuring its amplitude at regular intervals.
    x[n] = x(nTs)
Sampling frequency:
    fs = 1/Ts
Where:
fs = samples per second (Hz).
  Nyquist-Shannon Sampling Theorem;
A band-limited signal can be reconstructed from its samples if:
    fs > 2fmax
Where:
fmax = highest frequency component.
The minimum theoretical sampling frequency is called the Nyquist rate.
  Aliasing;
Aliasing occurs when a signal is sampled below the required sampling frequency, causing different frequency components to become indistinguishable.
Prevention:
- Use an adequate sampling frequency.
- Apply an anti-aliasing low-pass filter before sampling.
- Ensure the analog input is sufficiently band-limited.
  Quantization;
Quantization converts sampled amplitudes into a finite number of discrete amplitude levels.
For an n-bit ADC:
    L = 2^n
Where L = number of quantization levels.
For a uniform quantizer:
    Δ = (Vmax - Vmin)/L
Where:
Δ = quantization step size.
Quantization error:
    e[n] = x[n] - xq[n]
For an ideal rounding quantizer:
    -Δ/2 ≤ e[n] ≤ Δ/2
  Binary Encoding;
Quantized signal values are converted into binary numbers for digital storage and processing.
Example:
An 8-bit ADC has:
    L = 2^8 = 256 levels.
A 12-bit ADC has:
    L = 2^12 = 4096 levels.
Higher resolution generally allows finer amplitude representation, although actual accuracy also depends on noise, linearity and other ADC characteristics.

 DIGITAL SIGNAL PROCESSING SYSTEM ARCHITECTURE
A typical DSP system follows this sequence:
Physical quantity
       ↓
Sensor / Transducer
       ↓
Signal Conditioning
       ↓
Anti-Aliasing Filter
       ↓
ADC
       ↓
Digital Signal Processor
       ↓
DAC (where analog output is required)
       ↓
Reconstruction Filter
       ↓
Output / Actuator

  Sensor / Transducer;
Converts physical quantities into electrical signals.
Examples:
- Microphone: sound to electrical signal.
- Accelerometer: acceleration to electrical signal.
- Temperature sensor: temperature to electrical signal.
- Photodiode: light to electrical signal.
  Signal Conditioning;
Prepares the signal for digital conversion.
Functions:
- Amplification.
- Attenuation.
- Filtering.
- Isolation.
- Impedance matching.
- Level shifting.
  Anti-Aliasing Filter;
An analog low-pass filter placed before the ADC.
Its purpose is to remove frequency components above the usable sampling bandwidth to prevent aliasing.
  Analog-to-Digital Converter (ADC);
Converts analog input signals into digital data.
Main stages:
1. Sampling.
2. Quantization.
3. Encoding.
Important ADC specifications:
- Resolution.
- Sampling rate.
- Input voltage range.
- Accuracy.
- Conversion time.
- Signal-to-noise ratio.
  Digital Signal Processor;
Performs mathematical operations on digital samples using programmed algorithms.
Functions:
- Filtering.
- FFT calculations.
- Signal detection.
- Noise cancellation.
- Compression.
- Signal transformation.
  Digital-to-Analog Converter (DAC);
Converts processed digital samples into an analog electrical signal.
A reconstruction filter is commonly used after the DAC to suppress unwanted spectral images.

 DISCRETE-TIME SYSTEMS AND DSP MATHEMATICS
  Discrete-Time System;
A discrete-time system transforms an input sequence into an output sequence.
    y[n] = T{x[n]}
Where:
x[n] = input sequence.
y[n] = output sequence.
T = system operation.
  Linear Systems;
A system is linear if it satisfies superposition.
    T{ax₁[n] + bx₂[n]} = aT{x₁[n]} + bT{x₂[n]}
  Time-Invariant Systems;
A system is time-invariant if shifting the input sequence produces an equivalent shift in the output.
If:
    x[n] → y[n]
Then:
    x[n-n₀] → y[n-n₀]
  Causal Systems;
A causal system depends only on present and past input values, not future values.
  Stable Systems;
A system is BIBO stable if every bounded input produces a bounded output.
For a discrete-time LTI system:
    Σ(n=-∞ to ∞)|h[n]| < ∞
Where h[n] is the impulse response.
  Memoryless Systems;
Output depends only on the current input.
Example:
    y[n] = 3x[n]
  Systems with Memory;
Output depends on previous or other input samples.
Example:
    y[n] = x[n] + x[n-1]
  Difference Equations;
Discrete-time systems are commonly represented using difference equations.
General form:
a₀y[n] + a₁y[n-1] + ... + a_Ny[n-N] = b₀x[n] + b₁x[n-1] + ... + b_Mx[n-M]
They are important in digital filter implementation and discrete-time system analysis.

 DISCRETE-TIME SIGNAL OPERATIONS
  Amplitude Scaling;
y[n] = Ax[n]
Multiplies every sample by a constant.
  Time Shifting;
y[n] = x[n-n₀]
Delays the sequence when n₀ is positive.
y[n] = x[n+n₀]
Advances the sequence.
  Time Reversal;
y[n] = x[-n]
Reverses the sample sequence around n = 0.
  Addition;
y[n] = x₁[n] + x₂[n]
Combines two sequences.
  Multiplication;
y[n] = x₁[n]x₂[n]
Used in modulation, amplitude control and signal windowing.
  Accumulation;
y[n] = Σ(k=-∞ to n)x[k]
Calculates the cumulative sum of a sequence.
  Difference Operation;
y[n] = x[n] - x[n-1]
Measures the difference between successive samples.
Used in edge detection, change detection and digital differentiation.

 DISCRETE-TIME FOURIER TRANSFORM (DTFT)
The DTFT converts a discrete-time signal into a continuous function of frequency.
    X(e^jω) = Σ(n=-∞ to ∞)x[n]e^(-jωn)
Where:
x[n] = discrete-time signal.
X(e^jω) = frequency-domain representation.
ω = digital angular frequency in rad/sample.
Inverse DTFT:
    x[n] = (1/2π)∫(-π to π)X(e^jω)e^(jωn)dω
  Importance of DTFT;
- Analyses the frequency content of discrete-time signals.
- Helps design digital filters.
- Describes the frequency response of digital systems.
- Supports digital communication analysis.
  Periodicity;
The DTFT is periodic in frequency with period 2π:
    X(e^j(ω+2π)) = X(e^jω)
  Frequency Response;
For an LTI discrete-time system:
    H(e^jω) = Σh[n]e^(-jωn)
It describes how the system modifies the magnitude and phase of different frequency components.

 DISCRETE FOURIER TRANSFORM (DFT)
The DFT converts a finite-length sequence of N samples into N discrete frequency-domain components.
    X[k] = Σ(n=0 to N-1)x[n]e^(-j2πkn/N)
Where:
N = number of samples.
n = time-domain sample index.
k = frequency-bin index.
Inverse DFT
    x[n] = (1/N)Σ(k=0 to N-1)X[k]e^(j2πkn/N)
Applications;
- Frequency spectrum analysis.
- Digital filtering.
- Signal compression.
- Communication systems.
- Audio processing.
- Vibration analysis.
  Frequency Resolution;
For an N-point DFT:
    Δf = fs/N
Where:
fs = sampling frequency.
N = number of samples.
Frequency represented by bin k:
    fk = kfs/N
For a real-valued input, the unique non-redundant spectrum generally extends from DC to the Nyquist frequency.
  Spectral Leakage;
Spectral leakage occurs when a finite observation window does not contain an integer number of cycles of a signal, spreading energy across neighbouring frequency bins.
Reduction:
- Apply suitable window functions.
- Increase observation duration when possible.
- Choose suitable sampling and analysis parameters.
  Window Functions;
A window is multiplied by a finite signal segment before calculating its DFT.
Common windows:
- Rectangular.
- Hann.
- Hamming.
- Blackman.
- Kaiser.
Each window provides a different trade-off between main-lobe width and sidelobe suppression.

 FAST FOURIER TRANSFORM (FFT)
The FFT is an efficient computational algorithm used to calculate the Discrete Fourier Transform.
It does not represent a different mathematical transform from the DFT; it computes the same result more efficiently.
  Computational Complexity;
Direct DFT:
    O(N²)
Typical FFT:
    O(N log₂N)
  Radix-2 FFT;
A common FFT implementation that divides an N-point DFT into smaller DFT operations.
It typically requires N to be a power of two.
Examples:
N = 64, 128, 256, 512, 1024.
  Butterfly Operation;
The butterfly is a basic computational structure used in FFT algorithms.
It combines intermediate complex values through additions, subtractions and multiplication by twiddle factors.
Twiddle factor:
    W_N^k = e^(-j2πk/N)
Applications
- Spectrum analysers.
- Digital audio equalizers.
- Radar systems.
- Communication systems.
- Machine vibration monitoring.
- Image processing.
- Fault diagnosis.

 DIGITAL FILTER DESIGN
A digital filter is a discrete-time system designed to modify a signal's frequency characteristics.
Its purpose is to allow desired frequencies to pass while attenuating unwanted frequencies.
  Types of Digital Filters;
 Low-Pass Filter (LPF)
Allows low frequencies to pass and attenuates high frequencies.
Applications:
- Sensor noise reduction.
- Audio smoothing.
- Removal of high-frequency interference.
 High-Pass Filter (HPF)
Allows high frequencies to pass and attenuates low frequencies.
Applications:
- Removal of DC offsets.
- Detection of rapid changes.
- Audio signal processing.
 Band-Pass Filter (BPF)
Allows frequencies within a specified band to pass.
Applications:
- Radio receivers.
- Wireless communication.
- Biomedical signal extraction.
 Band-Stop Filter (BSF)
Attenuates frequencies within a selected band.
Applications:
- Removing unwanted interference.
- Eliminating specific noise frequencies.
 Notch Filter
A narrow band-stop filter designed to reject a particular frequency.
Example: removing 50 Hz electrical interference from an ECG signal.
 Filter Specifications
Important parameters:
- Passband: range of frequencies allowed through.
- Stopband: range of frequencies attenuated.
- Cut-off frequency: specified boundary of the filter response.
- Transition band: frequency region between passband and stopband.
- Passband ripple: variation in passband gain.
- Stopband attenuation: suppression of unwanted frequencies.
- Filter order: determines filter complexity and affects selectivity.
 Finite Impulse Response (FIR) Filters
FIR filters have an impulse response of finite duration.
General equation:
    y[n] = Σ(k=0 to M)b[k]x[n-k]
Where:
b[k] = filter coefficients.
M = filter order.
Characteristics:
- No recursive feedback.
- Always BIBO stable for finite coefficients.
- Can provide exact linear phase.
- Often require more coefficients than IIR filters.
Applications:
- Audio processing.
- Communication systems.
- Image processing.
  Infinite Impulse Response (IIR) Filters
IIR filters use feedback from previous output samples.
General equation:
    y[n] = Σ(b[k]x[n-k]) - Σ(a[k]y[n-k])
For normalized coefficients, a[0] = 1.
Characteristics:
- Recursive structure.
- Can achieve sharp filtering with fewer coefficients.
- Computationally efficient.
- Stability must be checked.
- Generally have nonlinear phase.
Applications:
- Real-time filtering.
- Audio equalization.
- Embedded systems.
  FIR vs IIR
FIR:
- Non-recursive.
- Inherently stable for finite coefficients.
- Can achieve linear phase.
- Often computationally more demanding.
IIR:
- Recursive.
- Stability depends on pole locations.
- Usually more efficient for comparable magnitude-response requirements.
- Generally nonlinear phase.

 DIGITAL FILTER DESIGN METHODS
  Window Method;
Used mainly in FIR filter design.
Steps:
1. Specify the desired frequency response.
2. Calculate the ideal impulse response.
3. Select a suitable window.
4. Multiply the ideal impulse response by the window.
5. Obtain finite filter coefficients.
6. Evaluate the resulting frequency response.
  Frequency Sampling Method;
Constructs an FIR filter by specifying its desired frequency response at selected frequency points and calculating the corresponding impulse response.
  Bilinear Transformation;
A method used to convert analog filter designs into digital filter designs.
Transformation:
    s = (2/T) [(1-z⁻¹)/(1+z⁻¹)]
Where T is the sampling period.
It maps the left-half s-plane into the interior of the z-plane unit circle.
  Impulse Invariance Method;
Converts an analog filter into a digital filter by sampling its analog impulse response.
It can cause aliasing in the frequency domain, so it is unsuitable for some filter designs.

 Z-TRANSFORM
The Z-transform is a mathematical tool used to analyse discrete-time signals and systems.
    X(z) = Σ(n=-∞ to ∞)x[n]z^(-n)
Where:
z = complex frequency variable.
  Common Z-Transform Pairs;
Unit impulse:
    δ[n] → 1
Unit step:
    u[n] → 1/(1-z⁻¹), |z| > 1
Exponential:
    aⁿu[n] → 1/(1-az⁻¹), |z| > |a|
  Region of Convergence (ROC);
The ROC is the region in the complex z-plane where the Z-transform summation converges.
It is important because the same algebraic expression can represent different sequences with different ROCs.
  Transfer Function;
For a discrete-time LTI system with zero initial conditions:
    H(z) = Y(z)/X(z)
Where:
H(z) = transfer function.
Y(z) = output Z-transform.
X(z) = input Z-transform.
  Poles and Zeros;
Zeros:
Values of z that make the numerator of H(z) zero.
Poles:
Values of z that make the denominator of H(z) zero.
For a causal rational LTI system:
- All poles strictly inside the unit circle: BIBO stable.
- A pole outside the unit circle: unstable.
- A pole on the unit circle: not BIBO stable.
Pole locations determine important system characteristics such as stability and transient response.

 DIGITAL SIGNAL CONVOLUTION
Convolution determines the output of a discrete-time LTI system from its input and impulse response.
    y[n] = x[n] * h[n]
    y[n] = Σ(k=-∞ to ∞)x[k]h[n-k]
  Properties;
Commutative:
    x[n]*h[n] = h[n]*x[n]
Associative:
    x*(h*g) = (x*h)*g
Distributive:
    x*(h+g) = x*h + x*g
Identity:
    x[n]*δ[n] = x[n]
  Linear Convolution;
Produces the output of an LTI system from two finite sequences.
If the input length is L and impulse-response length is M, the output length is:
    L + M - 1
  Circular Convolution;
Convolution of finite sequences treated as periodic sequences.
It is closely related to multiplication in the DFT domain.
To obtain linear convolution using DFT multiplication, zero-pad both sequences to at least:
    N ≥ L + M - 1
Applications:
- Digital filtering.
- Audio effects.
- Image processing.
- Communication channels.

 CORRELATION AND SIGNAL ESTIMATION
  Autocorrelation;
Measures similarity between a signal and a shifted version of itself.
For a finite-energy sequence:
    Rxx[m] = Σ(n=-∞ to ∞)x[n]x*[n-m]
Applications:
- Periodicity detection.
- Signal analysis.
- Frequency estimation.
  Cross-Correlation;
Measures similarity between two different signals.
    Rxy[m] = Σ(n=-∞ to ∞)x[n]y*[n-m]
Applications:
- Signal synchronization.
- Radar.
- Time-delay estimation.
- Pattern recognition.
  Signal Estimation;
Signal estimation involves determining unknown signal characteristics from observed or noisy data.
Examples:
- Estimating frequency.
- Estimating signal amplitude.
- Estimating phase.
- Estimating position and velocity from sensor measurements.
  Digital Signal Detection;
Determines whether a particular signal or event is present within noisy observations.
Applications:
- Radar target detection.
- Wireless receivers.
- Fault detection.
- Digital communication.

 NOISE REDUCTION AND DIGITAL SIGNAL ENHANCEMENT
  Signal-to-Noise Ratio (SNR);
SNR = Ps/Pn
In decibels:
    SNR(dB) = 10log₁₀(Ps/Pn)
For voltage measurements across equal impedances:
    SNR(dB) = 20log₁₀(Vs/Vn)
  Common Digital Noise Reduction Methods;
 Moving Average Filter
Averages a specified number of consecutive samples.
    y[n] = (1/M)Σ(k=0 to M-1)x[n-k]
Used for smoothing sensor data.
 Median Filter
Replaces each sample with the median value of a neighbouring group of samples.
Useful for removing impulsive noise, particularly in images.
 Adaptive Filtering
Adjusts filter coefficients according to changing signal conditions.
Common algorithms:
- LMS.
- NLMS.
- RLS.
 Digital Notch Filtering
Suppresses a specific unwanted frequency.
 Wavelet Denoising
Uses wavelet decomposition and coefficient thresholding to remove noise while preserving important signal features.
  Common Noise Sources;
- Thermal noise.
- Shot noise.
- Flicker noise.
- Impulse noise.
- Quantization noise.
- Electromagnetic interference.

 MULTIRATE DIGITAL SIGNAL PROCESSING
Multirate DSP involves processing signals at different sampling rates.
  Decimation;
Reduces the sampling rate by an integer factor M.
Procedure:
1. Apply an anti-aliasing low-pass filter.
2. Retain every Mth sample.
    y[n] = x[Mn]
  Interpolation;
Increases the sampling rate by an integer factor L.
Procedure:
1. Insert L-1 zeros between successive samples.
2. Apply an interpolation low-pass filter.
  Sample Rate Conversion;
Converts a signal from one sampling frequency to another.
Used in:
- Digital audio systems.
- Video processing.
- Communication systems.
- Data acquisition systems.
  Applications;
- Audio sample-rate conversion.
- Efficient communication processing.
- Digital audio interfaces.
- Multiband signal processing.

 DIGITAL COMMUNICATION AND DSP
DSP is fundamental in modern digital communication systems.
  Digital Modulation;
Modulation represents digital information by changing a carrier signal's properties.
 ASK (Amplitude Shift Keying)
Changes carrier amplitude according to digital data.
 FSK (Frequency Shift Keying)
Changes carrier frequency according to digital data.
 PSK (Phase Shift Keying)
Changes carrier phase according to digital data.
 QAM (Quadrature Amplitude Modulation)
Changes both amplitude and phase using combinations of two orthogonal carrier components.
  Demodulation;
Recovers the transmitted information from the received modulated signal.
  Channel Equalization;
Compensates for distortion introduced by a communication channel.
  Error Detection and Correction;
DSP-based communication systems may use coding techniques to detect or correct transmission errors.
Examples:
- Parity checking.
- CRC.
- Hamming codes.
- Convolutional codes.
- Turbo codes.
- LDPC codes.
  Software-Defined Radio (SDR);
SDR implements many radio functions through software rather than dedicated analog hardware.
DSP operations include:
- Digital filtering.
- Modulation.
- Demodulation.
- Frequency conversion.
- Synchronization.
- Channel estimation.
Applications:
- Wi-Fi.
- Cellular communication.
- Bluetooth.
- GPS.
- Radio receivers.

 DIGITAL IMAGE AND SPEECH PROCESSING
  Digital Image Processing;
A digital image can be represented as a two-dimensional discrete signal:
    f[m,n]
Where m and n are spatial coordinates.
Important operations:
- Image enhancement.
- Noise removal.
- Edge detection.
- Image segmentation.
- Image restoration.
- Image compression.
Common algorithms:
- Gaussian filtering.
- Median filtering.
- Sobel edge detection.
- Laplacian filtering.
- Two-dimensional FFT.
Applications:
- Computer vision.
- Medical imaging.
- Industrial inspection.
- Robotics.
  Digital Speech Processing;
Deals with analysis, enhancement and interpretation of speech signals.
Important operations:
- Speech sampling.
- Noise reduction.
- Speech enhancement.
- Voice activity detection.
- Feature extraction.
- Speech recognition.
- Speech compression.
Important techniques:
- Short-Time Fourier Transform (STFT).
- Mel-Frequency Cepstral Coefficients (MFCC).
- Linear Predictive Coding (LPC).
Applications:
- Voice assistants.
- Telephone communication.
- Speech recognition.
- Hearing aids.
- Audio conferencing.

 DSP HARDWARE AND IMPLEMENTATION
  Digital Signal Processor (DSP Chip);
A specialized processor designed to execute signal-processing operations efficiently.
Common characteristics:
- Fast multiply-accumulate operations.
- Efficient memory access.
- Specialized addressing modes.
- Efficient numerical processing.
- Support for real-time computation.
  Microcontrollers;
Microcontrollers can perform DSP operations in embedded applications.
Examples:
- STM32.
- ESP32.
- AVR.
- PIC.
Applications:
- Sensor filtering.
- Audio processing.
- Motor-control feedback.
- Data acquisition.
  FPGA;
A Field-Programmable Gate Array implements customizable digital hardware.
Advantages:
- Parallel processing.
- High throughput.
- Predictable latency.
- Custom hardware architectures.
Applications:
- Radar.
- High-speed communication.
- Image processing.
- Industrial signal acquisition.
  GPU;
A Graphics Processing Unit performs highly parallel computations.
Used for:
- Large-scale image processing.
- Video processing.
- Machine-learning-based signal analysis.
  Fixed-Point and Floating-Point Processing;
 Fixed-point:
Represents numbers using a fixed scaling convention.
Advantages:
- Often lower computational and memory requirements.
- Useful in resource-constrained embedded systems.
Limitations:
- Limited numerical range.
- Quantization and overflow must be managed.
 Floating-point:
Represents numbers using a significand and exponent.
Advantages:
- Wide dynamic range.
- Easier numerical algorithm development.
Limitations:
- May require more hardware resources and power.
  Real-Time DSP Requirements;
- Sufficient processing speed.
- Low latency.
- Adequate memory.
- Reliable data acquisition.
- Predictable execution time.
- Efficient algorithms.
- Appropriate numerical precision.

 DSP SOFTWARE AND DEVELOPMENT TOOLS
  MATLAB;
Used for:
- Signal generation.
- FFT analysis.
- Filter design.
- DSP simulations.
- Algorithm testing.
  Simulink;
Used for block-based modelling and simulation of DSP and control systems.
  Python;
Important libraries:
NumPy:
Numerical computation and array manipulation.
SciPy:
Digital filtering, FFT and signal analysis.
Matplotlib:
Signal visualization.
Pandas:
Measurement-data analysis.
OpenCV:
Image and video processing.
Librosa:
Audio and speech analysis.
  GNU Radio;
Open-source framework for building software-defined radio systems.
  CMSIS-DSP;
A collection of optimized DSP functions for Arm Cortex-M processors.
Examples of available functionality:
- FIR and IIR filters.
- FFT.
- Matrix operations.
- Vector mathematics.
- Statistics.
- Complex arithmetic.

 IMPORTANT DSP FORMULAS SUMMARY
  SAMPLING;
Sampling frequency:
    fs = 1/Ts
Nyquist criterion:
    fs > 2fmax
Quantization levels:
    L = 2ⁿ
Quantization step:
    Δ = (Vmax - Vmin)/L
  FOURIER ANALYSIS;
DTFT:
    X(e^jω) = Σx[n]e^(-jωn)
DFT:
    X[k] = Σ(n=0 to N-1)x[n]e^(-j2πkn/N)
Frequency resolution:
    Δf = fs/N
Frequency bin:
    fk = kfs/N
Z-TRANSFORM
    X(z) = Σx[n]z^(-n)
Transfer function:
    H(z) = Y(z)/X(z)
  DIGITAL FILTERING;
FIR:
    y[n] = Σb[k]x[n-k]
IIR:
    y[n] = Σb[k]x[n-k] - Σa[k]y[n-k]
CONVOLUTION
    y[n] = Σx[k]h[n-k]
MOVING AVERAGE
    y[n] = (1/M)Σ(k=0 to M-1)x[n-k]
NOISE
    SNR = Ps/Pn
    SNR(dB) = 10log₁₀(Ps/Pn)
  MULTIRATE PROCESSING;
Downsampling:
    y[n] = x[Mn]
Upsampling:
    Insert L-1 zeros between successive samples, then filter.
COMPUTATIONAL COMPLEXITY
Direct DFT:
    O(N²)
FFT:
    O(N log₂N)

 IMPORTANT ENGINEERING AND EXAMINATION TIPS
1. Understand the complete ADC-to-DSP-to-DAC process and the purpose of every stage.
2. Distinguish sampling, quantization and encoding.
3. Master the Nyquist theorem and aliasing, including numerical calculations.
4. Practise DFT and FFT calculations, including frequency-bin identification.
5. Understand the relationship between convolution and multiplication in the frequency domain.
6. Know the differences between FIR and IIR filters, particularly their structures, stability and phase characteristics.
7. Understand the Z-transform, ROC, poles, zeros and discrete-time system stability.
8. Learn how to interpret frequency-response plots, magnitude spectra and phase spectra.
9. Understand the purpose of window functions and spectral leakage.
10. In digital filter design, consider filter order, cut-off frequency, passband ripple and stopband attenuation.
11. Understand the difference between linear and circular convolution.
12. In practical DSP systems, consider processor speed, memory, numerical precision, latency and power consumption.
13. Practise implementing signal-processing algorithms using Python or MATLAB.
14. Learn how to deploy DSP algorithms on microcontrollers and dedicated DSP hardware.