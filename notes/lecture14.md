# lecture 14: Videos, Unsupervised Learning

- Spatio-Temporal ConvNets
  - 3D VGGNet
  - summary
    - model temporal motion locally (3D conv)
    - model temporal motion globally (LSTM/RNN)
    - Fusions of both approaches at the same time
  - down(CNN) + up(RNN)

- Unsupervised Learning Overview
 - definitions
 - autoencoders: Feature learning, generate samples
   - Vanilla
   - Variational autoencoder
   - Summary
     - traditional autoencoders
       - try to reconstruct input
       - used to learn features, initialize supervised model
       - not used much anymore
     - Variational Autoencoders
       - Bayesian meets deep learning
       - Sample from model to generate images
 - Adversarial Networks: how to your know, adversarial samples are not close to real examples
   - Generative adversarial networks
     - Generate samples
   - Generative Adversarial Nets: multiscale
   
### References
- Kingma and Welling, “Auto-Encoding Variational Bayes”, ICLR 2014
- Goodfellow et al, “Generative Adversarial Nets”, NIPS 2014
