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

