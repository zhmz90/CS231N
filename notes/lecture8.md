# Lecture 8: Spatial Localization and Detection

- Computer Vision Tasks
  - Classification, Classification + Localization, Object Detection, Instance Segmentation

- Classification + Localization: Task
  - Classification
    - input: Image
    - Output: Class label
    - Evaluation metric: Accuracy
  - Localizaition
    - input: Image
    - ouput: Box in the image (x,y,w,h)
    - Evaluation metric: Intersection over Union

### Idea #1: Localization as Regression
  - Step 1: Train (or download) a classification model (AlexNet, VGG, GoogLeNet)
  - Step 2: Attach new fully-connected "regression head" to the nework
  - Step 3: Train the regression head only with SGD and L2 loss: where?
  - Step 4: At test time use both heads

### Idea #2: Sliding Window
  - Step 1: Run classification + regression network at multiple locations on a high resolution image
  - Step 2: Convert fully-connected layers into convolutional layers for efficient computation
    - **why more efficient?**
  - Step 3: Combine classifer and regressor predictions across all scales for finial prediction
  - Overfeat(2014)

## Object Detection: find the possible region, do regression and classification
  - Detection as classification
  - Region Proposals: Selective Search, EdgeBoxes
  - R-CNN: slow at test time, SVMs and regressors are post-hoc, complex multi-stage training pipeline
    - Train (or download) a classification model for ImageNet(AlexNet)
    - Fine-tune model for detection
    - Extract Features
    - Train one binary SVM per class to classify region features
    - bbox regression: for each class, train a linear regression model to map from cached features to offsets
  to GT boxes to make up for "slightly wrong" proposals. 
  - Evaluation: mean average precision (mAP) [0, 100] high is good
  - Fast R-CNN
  - Faster R-CNN
    - CNN + Region Proposal Network (RPN) + Rol Pooling --> classifier + bbox regressor
    
### Questions
    - Rol Pooling layer? 
    - N anchor boxes? 
