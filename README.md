BurstAudio
========

This is a collection of modules to assist in the processing of audio data in Unity.
Everything is implemented in high-performance C#, leveraging Unity's Burst compiler.
This should allow for fast, threadable audio processing tasks.


Current
-------
Currently only supports performing FFTs (Fast Fourier Transforms) and Inverse FFTs on fixed size arrays. 
This lays the ground work for performing STFTs (Short Time Fourier Transforms), which will be the basis for a pitch shifting algorithm.

The FFT and iFFT implementations are extensions of: https://github.com/keijiro/BurstFFT (Thank you!)


Future
-------

- Support for variable length arrays (but constrained to size of 2^n based on Cooley-Tukey FFT implementation)
- Vectorized STFTs on "long" signal (many times the length of the STFT window)
- Vectorized winow functions
- Vectorized pitch shifting
