# Lecture 5: Training Neural Networks, Part 1

### Overview
- One time Setup
  - preprocessing
  - weight initialization
  - regularization
  - activation functions
  - gradient checking
  <br />
  - loss function
  - how many layers
  - network achitecture
  - opt alg
  
- Training dynamics
  - babysitting the learning process
  - parameter updates
  - hyperparameter optimization
  
- Evaluation
  - model ensembles
    - about 2% improvement

### Activation Functions
- Sigmoid

- Tanh

- ReLU

- Leaky ReLU

- Maxout

- ELU


### Data Preprocessing
- normalizaiton
  - mean, std
  
- PCA and Whitening

- Batch Normalization
  - x = (x - mean(x)) / sqrt(var(x))

### Weight Initialization
- First Idea
  - small random numbers: Gaussian ~ (0, 1e-2)
  - okay for small nn, lead to non-homogeneous distributions of activations across the layers of a larger nn.
  
- Activation statistics
  - mean, std for every layer

- Xavier initialization
  - randn(in, out) / sqrt(fan_in)
  - randn(in, out) / sqrt(fan_in/2) He et al.

### Babysitting the Learning Process
- Preprocess data
- Choose the architecture
- hyperparameter optimization
  - coarse -> fine, random search
    - learning rate, ...
- Monitor and visualize the loss curive

### Questions
- make everything as parameters, Is it possible? opt similar as DRL?
  
### TO CHALLENGLE
- do activation statitics
