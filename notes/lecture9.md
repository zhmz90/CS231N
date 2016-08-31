# Lecture 9: Understanding and Visualizing Convolutational Neural Networks

### Overview
- Visualize patches: maximally activate neurons
- Visualize the weights
- Visualize the representation space (t-sne)
- Occlusion experiments: similar with visualize patches
- Human experiment comparisons
- Deconv approaches (single backward pass)
- Optimization over image approaches (optimization)

### Deconv approaches
- Guided back propagation ???

### Optimization to image
- how to find an image that maximizes some class score?
  - Forward an image
  - Set activations in layer of interest to all zero, except for a 1.0 for a neuron of interest
  - backprop to image
  - do an image update
  
- visualize the data gradient

- Given a CNN code, is it possible to reconstruct the original image?


### Summary
  - Understanding 
  - Segmenting objects in the image
  - Inverting codes and introducing privacy concerns
  - Fun (NeuralStyle, DeepDream)
  - Confusion and chaos (Adversarial examples)
