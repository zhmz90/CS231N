# Lecture 11: CNNs in Practice

### Overview
- Making the most of your data
  - data augmentation
  - tranfer learning
- All about convolutions
  - How to arrange them
  - How to compute them fast
- "implementation details"
  - GPU / CPU, bottlenecks, distrubuted training

### Data Augmentation: Very Important

  - Horizontal flips
  - Random crops/scales: traning, testing
  - Color jitter
  - Random mix of translation, rotation, strecthing, shearing, lens distortions...

### A Genereal Theme
- Training: add random noise
  Testing: Marginalize over the noise
  - Data Augmentation, Dropout, Dropconnect, Bach normalization, Model ensembles

### Transfer Learning
- DeCAF

### All About Convolutions: Part 1, How to stack them
- The power of small filters: small filters same effect as big filters but more efficient computational.
  - How big of a region in the input does a neuron on the second conv layer see?
  
- Bottleneck: [Conv1x1, C/2 filters] => [Conv3x3, C/2 filters] => [Conv 1x1, C filters]
  - why Bottlenect? it reduce channels C/2 at first, at get back to C in the end.

- fewer parameters, less compute, more nonlinearity

### All About Convolutions: Part 2, How to compute them?
- im2col
  - duplicated memeory
  - easy to implement, but big memory overhead
- FFT
  - Convolution Theorem: F(fog) = F(f) * F(g)
  - Fast Fourier Transform: N-dim vector in NlogN time 
  - Big speedups for small kernels
- Fast Algorithms: Lavin and Gray (2015)
  - F(2x2, 3x3)

- Multi-GPU training: More complex
  - Data Parallelism: sync, async
  - Model Parallelism

- Bottlenecks
  - GPU - CPU communications is a bottleneck
    - CPU data prefetch + augment thread running
      while GPU preforms forward/backward pass
  - CPU disk bottleneck
    - hard disk is slow to read from
      - pre-processed images and stored contiguously in files,
        read as raw byte stream from SSD disk
- Floating point precision
  - fp32 fp16 fp2
  - fp with stochastic rounding converges but rounding to the nearest failed.
  - 1 bit activations and 1 bit weigths



