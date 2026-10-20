Digital Signal Processing (DSP) is the engineering discipline that uses mathematical algorithms and digital processors to analyze, modify, and synthesize signals (such as audio, video, and sensor data) after converting them from a continuous analog form into discrete digital values. 

Overview;
A typical DSP system transforms real-world physical phenomena into computer-readable data through three main stages: 
1. Analog-to-Digital Conversion (ADC):
	• Sampling: Measures a continuous signal at regular time intervals (guided by the Nyquist-Shannon sampling theorem, which requires sampling at ≥ 2× the highest frequency to prevent aliasing).
	• Quantization: Maps continuous amplitude values into discrete binary levels. 
2. Digital Processing: Algorithms run on specialized microprocessors (DSPs) or general-purpose hardware to filter, compress, or transform the data stream. 
3. Digital-to-Analog Conversion (DAC): Converts the processed digital data back into a continuous analog output (if required by the application). 

Key Topics;
• Sampling & Reconstruction: Managing the transition between continuous-time and discrete-time domains (𝑥[𝑛]), avoiding aliasing, and reconstruction filtering. 
• Transform Analysis: Moving signals between domains to reveal underlying frequencies:
	• Discrete Fourier Transform (DFT) & Fast Fourier Transform (FFT): Deconstructs a signal into its constituent sinusoidal frequencies.
	• Z-Transform: Analyzes discrete-time linear time-invariant (LTI) systems and stability.
	• Wavelet Transforms: Provides multi-resolution time-frequency analysis. 
• Digital Filtering:
	• FIR (Finite Impulse Response) Filters: Stable, linear-phase filters used for precise shaping.
	• IIR (Infinite Impulse Response) Filters: Recursive feedback filters that offer high efficiency with fewer coefficients. 
• Multirate DSP: Changing sample rates (decimation and interpolation) within a system. 

Applications;
• Audio & Speech: Noise cancellation, echo suppression, audio compression (MP3), and speech recognition. 
• Telecommunications: Wireless modulation/demodulation, equalization, Software-Defined Radio (SDR), and mitigating multipath fading in 4G/5G and Wi-Fi networks. 
• Image & Video Processing: Image enhancement, facial recognition, video compression (H.264/HEVC), and computer vision. 
• Biomedical Engineering: Processing electrocardiograms (ECGs), electroencephalograms (EEGs), and medical imaging reconstructions like MRI and CT scans. 
• Radar, Sonar & Navigation: Signal detection, target tracking, Doppler shift estimation, and GPS signal decoding.