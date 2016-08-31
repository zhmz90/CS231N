# Lecture 12: Software Packages Caffe/Torch/Theano/TensorFlow

- Caffe
  - C++, Python and matlib bindings
  - Good for training or finetuning feedforward models
  - Source code readable and good doc of C++
    - Blob
    - Layer
    - Net
    - Solver
  - Caffe: Training / Finetuning
    - Convert data to HDF5
    - Define net (edit prototxt)
    - Define solver (edit prototxt)
    - Train (with pretrained weights) 
  - Pros / Cons
    ![stanford CS231n](pic/caffe.jpg)
    
- Torch
  - C + Lua
  - Syntax is great, use it is easy. want to try it again, 
  but debug is still releated to C core part.
  - source code is not very elegant due to among ecosysterm most of them are
  deep learning researcher.
  - Typical Workflow
    - Prprocess data to HDF5
    - train a model in Lua/Torch
    - eval
  - Pros / Cons
    ![torch](pic/torch.jpg)

- Theano
  - Lasagne, Keras
  - error messages not useful, same as Torch in my opinion
  - Pros / Cons
    ![theano](pic/theano.jgp)
- TensorFlow
  - Google Brain
  - Pros / Cons
    ![tensorflow](pic/tensorflow.jpg)

### Questions
- I support tensorflow for now
  - 1. limited time
  - 2. Deep Mind, Google Brain etc Google have more resources than Facebook
  - 3. C++, CUDA, Python, Bazel, Protobuf are already familar for me.
  - 4. learn from master
  

