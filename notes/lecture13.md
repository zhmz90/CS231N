# Lecture 13: Segmentation and Attention 
** This Lecture is important **
- Segmentation
  - Semantic Segmentation
    - Recurrent Convolutional Neural Networks for Scene Labling
    - Deconvolution? inverse of Convolutaion? Convolution transpose? 
  - Instance Segmentation
  - overview
    - Semantic segmentation
      - classify all pixels
      - fully convolutational models, downsample then upsample
      - learnable upsampling: fractionally strided convolution
      - skip connections can help
    - Instance Segmentation
      - Detect instance, generate mask
      - similar pipelines to object detection

- (Soft) Attention
  - notes
    - soft attention can use gradient descent
    - hard attention can't, need reinforcement learning
    - seems soft attention works better, maybe hard attention not good due to optimization
  - Discrete locations
  - Continuous locations (Spatical Transformers)
  - soft attention for translation
  - **soft attention for everything**
    - Atttending to arbitrary regions: DRAW
      - classify images by attending to arbitrary regions of the input
    - Atttending to arbitrary regions: spatial transformer networks

- Attention Recap
  - Soft attention
    - easy to implement: produce distribution over input locations, reweight features and feed as input
    - Attend to arbitrary input locations using spatial transformer networks
  - Hard attention
    - attend to a single input location
    - can't use gradient descent
    - need reinforcement learning
    
- References
 - Pinheiro and Collobert, “Recurrent Convolutional Neural Networks for Scene Labeling”, ICML 2014
 - Xu et al, “Show, Attend and Tell: Neural Image Caption Generation with Visual Attention”, ICML 2015

