                SIGNALS AND SYSTEMS
A signal is a physical quantity or mathematical function that carries information about a phenomenon or system. Examples include voltage, current, temperature, pressure, sound, and electromagnetic waves.
A system is a physical device, process, or mathematical operation that transforms an input signal into an output signal.
General representation:
    x(t) → SYSTEM → y(t)
Where:
- x(t) = input signal
- y(t) = output signal
- t = continuous time
For discrete-time systems:
    x[n] → SYSTEM → y[n]
Where n is an integer representing the sample index.
Applications:
- Sensors: converting physical quantities into electrical signals.
- Control: processing feedback signals to regulate system behavior.
- Communication: transmitting and receiving information through signals.
- Electronics: filtering, amplification, and signal conditioning.
- Robotics: interpreting sensor measurements and controlling actuators.

CLASSIFICATION OF SIGNALS:
 Continuous-Time and Discrete-Time Signals;
Continuous-time signal: Defined at every instant of time.
Example: x(t) = sin(2πft).
Applications: analog voltage, sound pressure, temperature variations.
Discrete-time signal: Defined only at discrete time instants.
Example: x[n] = sin(Ωn).
Applications: sampled sensor measurements and digital signal processing.
 Analog and Digital Signals;
- Analog signal: varies continuously in amplitude and usually in time.
- Digital signal: represented using discrete amplitude levels, commonly binary values 0 and 1.
Important distinction: A discrete-time signal has discrete time instants, but its amplitude may still be continuous. A digital signal has quantized amplitude levels.
 Deterministic and Random Signals;
- Deterministic: completely specified by a mathematical expression or rule.
- Random (stochastic): contains uncertainty and is described statistically.
Examples:
- Deterministic: ideal sinusoidal waveform.
- Random: thermal noise and many communication-channel disturbances.
 Periodic and Aperiodic Signals;
A continuous-time signal is periodic if:
    x(t + T₀) = x(t)
where T₀ is the fundamental period.
The fundamental frequency is:
    f₀ = 1/T₀
Angular frequency:
    ω₀ = 2πf₀ = 2π/T₀
For a discrete-time signal:
    x[n + N₀] = x[n]
where N₀ is a positive integer. A discrete-time sinusoid is periodic only when its normalized angular frequency satisfies Ω/(2π) = k/N for integers k and N ≠ 0.
 Even and Odd Signals;
Even signal:
    x(-t) = x(t)
Odd signal:
    x(-t) = -x(t)
Any signal can be decomposed into even and odd components:
    xₑ(t) = [x(t) + x(-t)]/2
    xₒ(t) = [x(t) - x(-t)]/2
Therefore:
    x(t) = xₑ(t) + xₒ(t)
These properties simplify Fourier analysis.
 Energy and Power Signals;
Signal energy:
    E = ∫₋∞^∞ |x(t)|² dt
Average power:
    P = lim(T→∞) [1/(2T)] ∫₋T^T |x(t)|² dt
For discrete-time signals:
    E = Σₙ₌₋∞^∞ |x[n]|²
    P = lim(N→∞) [1/(2N+1)] Σₙ₌₋N^N |x[n]|²
- Energy signal: 0 < E < ∞, with average power equal to zero.
- Power signal: 0 < P < ∞, with generally infinite total energy.
- Some signals are neither energy nor power signals.
Example: A finite-duration pulse is generally an energy signal. A nonzero periodic sinusoid is generally a power signal.

BASIC SIGNALS:
 Unit Impulse;
Continuous-time impulse:
    δ(t)
It satisfies:
    ∫₋∞^∞ δ(t) dt = 1
Sifting property:
    ∫₋∞^∞ x(t)δ(t - t₀) dt = x(t₀)
The impulse is an ideal mathematical model of an extremely short event with unit area.
 Unit Step;
    u(t) = 0, for t < 0
    u(t) = 1, for t ≥ 0
Relation to impulse:
    d u(t)/dt = δ(t)
The step function models switching on a source or applying a constant input.
 Ramp Signal;
    r(t) = t u(t)
Therefore:
    r(t) = 0, for t < 0
    r(t) = t, for t ≥ 0
A ramp is useful for analyzing how a system responds to an input that increases linearly with time.
 Exponential Signal 
    x(t) = Ae^(at)
- a < 0: exponential decay.
- a > 0: exponential growth.
- a = 0: constant signal.
Complex exponential:
    x(t) = Ae^(jωt)
Using Euler's identity:
    e^(jθ) = cos θ + j sin θ
Complex exponentials are fundamental to Fourier analysis and frequency-response calculations.
 Sinusoidal Signal;
    x(t) = A cos(ωt + φ)
Where:
- A = amplitude
- ω = angular frequency in rad/s
- φ = phase angle in radians
- f = frequency in hertz
- T = period in seconds
Relations:
    ω = 2πf
    T = 1/f
A sinusoidal input is used to determine a system's gain and phase response.

BASIC SIGNAL OPERATIONS:
Amplitude Scaling;
    y(t) = A x(t)
A changes the amplitude of the signal.
Time Shifting;
    y(t) = x(t - t₀): delay by t₀.
    y(t) = x(t + t₀): advance by t₀.
Time Reversal;
    y(t) = x(-t)
The signal is reflected about the vertical axis.
Time Scaling;
    y(t) = x(at)
- |a| > 1: compression in time.
- 0 < |a| < 1: expansion in time.
- a < 0: time reversal also occurs.
Addition and Multiplication;
Addition:
    y(t) = x₁(t) + x₂(t)
Multiplication:
    y(t) = x₁(t)x₂(t)
Addition models signal superposition; multiplication is used in modulation, switching, and signal weighting.

CLASSIFICATION OF SYSTEMS:
Linear and Nonlinear Systems;
A system is linear if it satisfies superposition:
    T{a x₁(t) + b x₂(t)} = aT{x₁(t)} + bT{x₂(t)}
Where T represents the system operation.
A system that does not satisfy this condition is nonlinear.
Examples:
- Ideal amplifier: y(t) = Kx(t), linear.
- Saturating amplifier: nonlinear.
- y(t) = x²(t), nonlinear.
Time-Invariant and Time-Varying Systems;
A system is time-invariant if delaying the input delays the output by the same amount without otherwise changing the response.
If:
    T{x(t)} = y(t)
Then time invariance requires:
    T{x(t - t₀)} = y(t - t₀)
Example:
- y(t) = 3x(t): time-invariant.
- y(t) = tx(t): time-varying.
Causal and Noncausal Systems;
A causal system's output at time t depends only on present and past inputs.
Example:
    y(t) = x(t) + x(t - 1)
A noncausal system may depend on future input values.
Example:
    y(t) = x(t + 1)
Physical real-time control systems must be causal, although offline signal processing can use noncausal operations.
Stable and Unstable Systems;
A system is bounded-input, bounded-output (BIBO) stable if every bounded input produces a bounded output.
If:
    |x(t)| ≤ Mₓ < ∞
then stability requires:
    |y(t)| ≤ Mᵧ < ∞
for some finite Mᵧ.
For a continuous-time LTI system, BIBO stability requires:
    ∫₋∞^∞ |h(t)| dt < ∞
For a discrete-time LTI system:
    Σₙ₌₋∞^∞ |h[n]| < ∞
where h is the impulse response.
Memoryless and Dynamic Systems;
- Memoryless: output depends only on the current input.
- Dynamic: output depends on past inputs, stored energy, or internal states.
Examples:
    - y(t) = 5x(t): memoryless.
- RC circuit: dynamic because the capacitor stores energy.

LINEAR TIME-INVARIANT (LTI) SYSTEMS:
An LTI system is both linear and time-invariant. It is especially important because its behavior can be characterized by its impulse response.
-Impulse Response;
The impulse response h(t) is the output of an initially relaxed LTI system when the input is δ(t).
Knowing h(t) allows the output for any suitable input to be calculated.
-Convolution;
Continuous-time convolution:
    y(t) = x(t) * h(t)
    y(t) = ∫₋∞^∞ x(τ)h(t - τ)dτ
Discrete-time convolution:
    y[n] = Σₖ₌₋∞^∞ x[k]h[n - k]
Convolution describes how a system combines the input with its impulse response.
Applications:
- Digital filters.
- Sensor signal conditioning.
- Communication-channel analysis.
- Predicting circuit outputs.
-Properties of Convolution
Commutative:
    x * h = h * x
Associative:
    x * (h₁ * h₂) = (x * h₁) * h₂
Distributive:
    x * (h₁ + h₂) = x * h₁ + x * h₂
For LTI systems, cascading systems corresponds to convolving their impulse responses.

DIFFERENTIAL EQUATIONS AND SYSTEM MODELS:
Continuous-time systems are often represented using differential equations.
General linear constant-coefficient model:
    aₙ dⁿy/dtⁿ + ... + a₁ dy/dt + a₀y = bₘ dᵐx/dtᵐ + ... + b₁ dx/dt + b₀x
Here, x(t) is the input and y(t) is the output.
Example: A first-order system:
    τ dy(t)/dt + y(t) = Kx(t)
Where:
- τ = time constant in seconds.
- K = steady-state gain.
For a step input x(t) = A u(t), assuming zero initial conditions:
    y(t) = KA(1 - e^(-t/τ))u(t)
The time constant τ indicates how quickly the system responds. At t = τ, the response reaches approximately 63.2% of its final value.
A first-order system reaches approximately 95% of its final value after 3τ and 99.3% after 5τ.

LAPLACE TRANSFORM AND TRANSFER FUNCTIONS:
The Laplace transform converts a time-domain function into the complex frequency domain.
Definition:
    X(s) = ∫₀^∞ x(t)e^(-st)dt
where:
    s = σ + jω
For a system initially at rest, the transfer function is:
    H(s) = Y(s)/X(s)
The transfer function describes the input-output relationship under zero initial conditions.
Example: For
    τ dy(t)/dt + y(t) = Kx(t)
the transfer function is:
    H(s) = K/(τs + 1)
 Poles and Zeros;
- Zeros: values of s that make the transfer-function numerator zero.
- Poles: values of s that make the denominator zero.
For a continuous-time rational system, all poles strictly in the left half of the s-plane indicate asymptotic internal stability for a minimal realization. For a proper rational LTI system, BIBO stability requires all transfer-function poles to lie strictly in the left half-plane.
Poles determine natural modes and strongly influence stability and transient response. Zeros shape the response but do not alone determine stability.

FOURIER ANALYSIS AND FREQUENCY RESPONSE:
Fourier analysis expresses signals in terms of sinusoidal or complex-exponential components.
-Fourier Transform;
Continuous-time Fourier transform (CTFT):
    X(jω) = ∫₋∞^∞ x(t)e^(-jωt)dt
Inverse transform:
    x(t) = (1/2π) ∫₋∞^∞ X(jω)e^(jωt)dω
The transform reveals the frequency components of a signal.
-Frequency Response;
For an LTI system:
    H(jω) = Y(jω)/X(jω)
Equivalently, for a system with impulse response h(t):
    H(jω) = ∫₋∞^∞ h(t)e^(-jωt)dt
The frequency response describes:
- Magnitude: how much each frequency is amplified or attenuated.
- Phase: how much each frequency is shifted in phase.
For sinusoidal input x(t) = A cos(ωt), a stable LTI system in sinusoidal steady state produces:
    y(t) = A|H(jω)| cos[ωt + ∠H(jω)]
-Fourier Series;
A periodic signal can be represented using a sum of harmonically related sinusoids.
Complex Fourier series:
    x(t) = Σₖ₌₋∞^∞ Cₖe^(jkω₀t)
where:
    Cₖ = (1/T₀) ∫ over one period x(t)e^(-jkω₀t)dt
Applications include harmonic analysis of electrical power signals, vibration analysis, and waveform synthesis.

SAMPLING AND DIGITAL SIGNAL PROCESSING:
Sampling converts a continuous-time signal into a discrete-time sequence.
    x[n] = x(nTₛ)
Where:
- Tₛ = sampling period.
- fₛ = sampling frequency.
- fₛ = 1/Tₛ.
 Nyquist-Shannon Sampling Theorem;
For a band-limited signal with highest frequency component fmax, ideal reconstruction requires:
    fₛ > 2fmax
The theoretical minimum sampling rate is called the Nyquist rate:
    fN = 2fmax
Sampling below the required rate can cause aliasing, where different frequency components become indistinguishable.
Practical measures:
- Use an anti-aliasing low-pass filter before sampling.
- Choose a sampling rate above the theoretical minimum when appropriate.
- Use a suitable analog-to-digital converter (ADC).
- Consider quantization resolution and noise.
 Quantization;
An ADC maps sampled amplitudes to a finite number of digital levels.
For an ideal N-bit converter:
    Number of levels = 2ᴺ
For a unipolar input range VFS:
Ideal quantization step:
    Δ ≈ VFS/2ᴺ
The exact step depends on the converter's coding convention and specified full-scale range.
For an ideal uniform quantizer with quantization error uniformly distributed over ±Δ/2:
    Quantization-noise variance = Δ²/12
Increasing the bit depth generally improves amplitude resolution but increases data size and hardware requirements.
 Discrete Fourier Transform;
The DFT converts a finite sequence into frequency-domain samples.
    X[k] = Σₙ₌₀^(N-1) x[n]e^(-j2πkn/N)
The inverse DFT is:
    x[n] = (1/N) Σₖ₌₀^(N-1) X[k]e^(j2πkn/N)
The fast Fourier transform (FFT) is an efficient family of algorithms for computing the DFT.
Applications: vibration monitoring, audio processing, spectral analysis, and fault detection.

FILTERS AND SIGNAL CONDITIONING:
A filter selectively passes or attenuates frequency components.
 Low-Pass Filter (LPF);
Passes low frequencies and attenuates high frequencies.
Applications:
- Removing high-frequency sensor noise.
- Anti-aliasing before ADC conversion.
- Smoothing measurements.
 High-Pass Filter (HPF);
Passes high frequencies and attenuates low frequencies.
Applications:
- Removing DC offsets.
- Detecting rapid changes.
- Extracting vibration or transient components.
 Band-Pass Filter (BPF);
Passes a selected frequency band.
Applications: radio receivers, communication channels, and biomedical instrumentation.
 Band-Stop Filter;
Attenuates a selected band. A notch filter is a narrow band-stop filter.
Application: suppressing 50 Hz or 60 Hz power-line interference when appropriate.
 RC Low-Pass Filter;
For a resistor R in series with the input and a capacitor C connected from the output to ground:
    H(s) = 1/(1 + sRC)
Time constant:
    τ = RC
Cutoff frequency:
    fc = 1/(2πRC)
At the cutoff frequency:
- Output magnitude is 1/√2 of the passband magnitude.
- Gain is approximately -3.01 dB.
- Phase is -45° for an ideal first-order RC low-pass filter.
The cutoff frequency is the point where the output power is half the passband power for the same input conditions.

SIGNALS IN SENSORS AND INSTRUMENTATION:
A sensor detects a physical quantity and produces a measurable output. A transducer converts energy from one form to another; many sensors operate as transducers.
Examples:
- Thermistor: temperature-dependent resistance.
- Strain gauge: resistance changes with mechanical strain.
- Photodiode: light produces electrical current.
- Microphone: sound pressure is converted into an electrical signal.
- Accelerometer: measures acceleration.
- Pressure sensor: converts pressure into an electrical quantity.
 Sensor Signal Chain;
Physical quantity → Sensor → Signal conditioning → Filter → ADC → Digital processing → Output or controller.
Important stages:
- Amplification: increases small signal levels.
- Filtering: reduces unwanted frequency components.
- Isolation: reduces unwanted electrical interaction.
- Linearization: compensates for nonlinear sensor response.
- Calibration: relates measured output to a known reference.
- ADC: converts analog measurements into digital values.
 Important Sensor Characteristics;
- Sensitivity: change in output per unit change in input.    
    S = ΔOutput/ΔInput
- Accuracy: closeness of a measurement to the true or accepted reference value.
- Precision: closeness of repeated measurements to one another.
- Resolution: smallest input change that can be distinguished.
- Linearity: closeness of the input-output relationship to a straight line.
- Hysteresis: difference in output for the same input depending on the direction of approach.
- Repeatability: ability to produce similar results under the same conditions.
- Response time: time required to respond to a change in input.
- Range: minimum and maximum measurable input values.
- Drift: gradual change in output under constant input conditions.
Sensitivity is not the same as accuracy: a highly sensitive sensor can still be inaccurate.

FEEDBACK AND CONTROL SYSTEMS:
A control system regulates a process to achieve a desired output.
 Open-Loop Control;
The controller acts without using output feedback.
Reference → Controller → Plant → Output
Advantages:
- Simple and inexpensive.
- Generally straightforward to design.
Disadvantages:
- Cannot automatically correct errors caused by disturbances or parameter changes.
Example: a timer-based irrigation system that waters for a fixed duration.
 Closed-Loop Control;
The output is measured and compared with the reference.
Reference r(t) → Comparator → Controller → Plant → Output y(t)
↑                         |
└──── Feedback ◄───────────┘
Error signal:
    e(t) = r(t) - y(t)
For a standard negative-feedback system with forward transfer function G(s) and feedback transfer function H(s):
Closed-loop transfer function:
    T(s) = G(s)/[1 + G(s)H(s)]
For unity feedback, H(s) = 1:
    T(s) = G(s)/[1 + G(s)]
Negative feedback can improve tracking and disturbance rejection, but poorly designed feedback may cause oscillations or instability.
 PID Controller;
A proportional-integral-derivative controller is widely used in industrial automation.
Control law:
    u(t) = Kp e(t) + Ki ∫₀ᵗ e(τ)dτ + Kd de(t)/dt
Where:
- Kp = proportional gain.
- Ki = integral gain.
- Kd = derivative gain.
- e(t) = control error.
- u(t) = control signal.
Effects:
- P: responds to present error; can reduce error but may leave steady-state offset.
- I: accumulates past error; can eliminate steady-state error in many systems, but may increase overshoot and settling time.
- D: responds to the rate of change of error; can improve damping, but is sensitive to measurement noise.
Practical considerations:
- Filter the derivative term when necessary.
- Use anti-windup to prevent excessive integral accumulation during actuator saturation.
- Tune gains according to system dynamics and performance requirements.
 Stability and Transient Response;
Important performance measures:
- Rise time: time taken to move from a specified lower percentage to an upper percentage of the final response.
- Settling time: time required to remain within a specified tolerance band around the final value.
- Overshoot: amount by which the response exceeds its final value.
- Steady-state error: difference between the reference and output after transients have decayed.
- Stability: whether system behavior remains bounded or converges appropriately after disturbances.
A good controller balances speed, accuracy, stability, actuator limitations, and noise sensitivity.

SIGNALS IN COMMUNICATION SYSTEMS:
A communication system transfers information from a source to a destination.
Basic chain:
    Information source → Transmitter → Channel → Receiver → Destination
Noise and interference may affect the signal at any stage.
 Modulation;
Modulation varies a carrier signal according to an information signal.
Amplitude modulation (AM):
    s(t) = Ac[1 + μmₙ(t)]cos(2πfct)
Where mₙ(t) is a normalized message with magnitude no greater than one, μ is the modulation index, Ac is the carrier amplitude, and fc is the carrier frequency.
Frequency modulation (FM) varies the instantaneous frequency of the carrier according to the message signal.
Phase modulation (PM) varies the carrier phase according to the message signal.
Digital modulation examples:
- ASK: amplitude shift keying.
- FSK: frequency shift keying.
- PSK: phase shift keying.
- QAM: quadrature amplitude modulation.
 Bandwidth;
Bandwidth is the range of frequencies occupied or passed by a signal or system.
For a band-limited baseband signal:
    B = fH - fL
where fH and fL are the upper and lower band limits.
Bandwidth requirements depend on modulation method, data rate, pulse shaping, and acceptable distortion.
 Noise and Signal-to-Noise Ratio
Noise is an unwanted random disturbance that affects the desired signal.
Signal-to-noise ratio:
    SNR = Ps/Pn
In decibels:
    SNR(dB) = 10 log₁₀(Ps/Pn)
For signal and noise voltages measured across the same resistance:
    SNR(dB) = 20 log₁₀(Vs/Vn)
The voltage formula requires equivalent measurement conditions and compatible RMS quantities.
Higher SNR generally means a cleaner received signal.
 Channel Capacity;
Shannon-Hartley theorem for an ideal band-limited channel with additive white Gaussian noise:
    C = B log₂(1 + SNR) bits/s
Where:
- C = theoretical channel capacity.
- B = channel bandwidth in hertz.
- SNR = linear power ratio, not decibels.
Capacity increases with bandwidth and SNR, but practical systems are also limited by coding, hardware, interference, and regulatory constraints.

IMPORTANT ENGINEERING EQUATIONS SUMMARY:
Frequency and period:     
   f = 1/T,  ω = 2πf
Signal energy:   
   E = ∫₋∞^∞ |x(t)|²dt
Average power:   
   P = lim(T→∞) (1/2T)∫₋T^T |x(t)|²dt
Convolution:   
   y(t) = ∫₋∞^∞ x(τ)h(t - τ)dτ
Transfer function:   
   H(s) = Y(s)/X(s), under zero initial conditions
Frequency response:   
   H(jω) = Y(jω)/X(jω)
Sampling:   
   fₛ > 2fmax for ideal band-limited reconstruction
RC filter cutoff:   
   fc = 1/(2πRC)
Negative-feedback transfer function:   
   T(s) = G(s)/[1 + G(s)H(s)]
PID control:    
    u(t) = Kp e(t) + Ki∫e(t)dt + Kd de(t)/dt
Signal-to-noise ratio:    
    SNR(dB) = 10 log₁₀(Ps/Pn)
Shannon capacity:    
    C = B log₂(1 + SNR)

PRACTICAL ENGINEERING WORKFLOW
When analyzing a real signal-processing or control problem:
1. Identify the input, output, and physical meaning of each signal.
2. Determine whether the signals are continuous-time or discrete-time.
3. Establish whether the system is linear, time-invariant, causal, and stable.
4. Select a suitable model: algebraic equation, differential equation, difference equation, or state-space representation.
5. Obtain the impulse response, transfer function, or state-space model where applicable.
6. Analyze time-domain response and frequency-domain behavior.
7. Design appropriate filtering, sampling, and signal conditioning.
8. For feedback control, analyze stability, tracking error, overshoot, and settling time.
9. For communication, evaluate bandwidth, noise, modulation, and data-rate requirements.
10. Validate the design through simulation, measurement, and testing.

EXAM AND DESIGN TIPS
- Always distinguish frequency in hertz from angular frequency in radians per second.
- Convert decibel values into linear ratios before substituting into equations that require linear quantities.
- For convolution, carefully determine the overlap of the input and impulse response.
- A system's linearity and time invariance are separate properties; test each independently.
- Do not assume that every linear system is stable or that every feedback system is stable.
- Use zero initial conditions when directly applying a transfer function as an input-output ratio.
- Apply an anti-aliasing filter before sampling when the analog input contains frequencies above the usable band.
- Sensor calibration and signal conditioning are as important as the sensor's nominal sensitivity.
- A filter may reduce noise but can also introduce phase delay or remove useful signal components.
- In control systems, faster response is not always better; excessive gain may increase overshoot, noise sensitivity, or instability.
- In communication equations, distinguish power ratios from voltage ratios and linear SNR from SNR in decibels.

END OF NOTES