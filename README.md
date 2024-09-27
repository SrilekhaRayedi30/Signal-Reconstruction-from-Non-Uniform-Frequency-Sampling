# Signal-Reconstruction-from-Non-Uniform-Frequency-Sampling

Signal Reconstruction from Non-Uniform Frequency Sampling
This project involves signal reconstruction using various interpolation techniques in the frequency domain. The project primarily focuses on the effects of non-uniform sampling in the frequency domain and the ability to reconstruct signals using interpolation techniques such as linear and polynomial interpolation, as well as the use of the Inverse Non-Uniform Fourier Transform (INUFT).

Prerequisites
Python 3.x
Libraries:
librosa for audio processing
numpy for numerical operations
matplotlib for plotting
scipy for interpolation
pynufft for the non-uniform FFT
An input audio file in .wav format to be processed
Code Overview

Step 1: Import Necessary Libraries
The code imports the necessary libraries for audio processing (librosa), numerical operations (numpy), and plotting (matplotlib), as well as specific libraries for signal processing and interpolation (scipy.interpolate and pynufft).

Step 2: Load the Audio File
The input audio file is loaded using the librosa library. The audio signal (signal) and the sampling rate (sr) are extracted for further processing.

Step 3: Non-Uniform Sampling Simulation
The function simulate_non_uniform_sampling performs non-uniform sampling in the frequency domain by retaining only a fraction of the frequency components. A mask is used to identify which components are retained.

Step 4: Frequency Domain Interpolation
Linear Interpolation: The function frequency_domain_interpolation interpolates missing frequency components using linear interpolation.
Polynomial Interpolation: The function polynomial_frequency_domain_interpolation performs polynomial fitting to estimate missing frequency components.
Step 5: Signal Reconstruction
The function reconstruct_signal reconstructs the signal from the interpolated Short-Time Fourier Transform (STFT).

Step 6: Signal Evaluation
Various evaluation metrics are calculated to compare the original and reconstructed signals:

Mean Squared Error (MSE)
Mean Intensity Error (MIE)
Peak Signal-to-Noise Ratio (PSNR)
Step 7: Inverse Non-Uniform Fourier Transform (INUFT)
The INUFT function utilizes the pynufft library to perform signal reconstruction using the Inverse Non-Uniform Fourier Transform.

Step 8: Visualizing Results
The results, including original and reconstructed signals, MSE, MIE, and PSNR, are plotted using matplotlib for various sampling fractions.

Usage
Place the input audio files in the ./input/ directory.
Run the code to simulate non-uniform sampling and perform reconstruction using various interpolation techniques.
The results will be printed in the console and plotted using matplotlib.

Output
The output includes visualizations of the original and reconstructed signals for each interpolation method.
Calculated evaluation metrics (MSE, MIE, and PSNR) are printed for each method.
Additional Information
The code supports processing multiple input audio files.
Different sampling fractions can be used to observe the effects on reconstruction accuracy.
References
This project uses audio processing and signal reconstruction techniques to explore non-uniform sampling and interpolation methods in the frequency domain.
