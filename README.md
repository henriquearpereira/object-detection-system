# object-detection-system
Object detection is a computer vision task that involves identifying and locating multiple objects within an image or video. Unlike simple classification, object detection precisely outlines and pinpoints where each object is located, typically using bounding boxes. 

## SSD Model Architecture

The Single Shot Detector (SSD) is an excellent choice for this project due to its balance between speed and accuracy.

### Base Network for Feature Extraction

SSD uses a base network (like VGG16, MobileNet) for feature extraction. This base network is responsible for extracting high-level features from the input image, which are then used for object detection.

### Auxiliary Convolutional Layers for Multi-Scale Feature Maps

In addition to the base network, SSD adds auxiliary convolutional layers to produce multi-scale feature maps. These layers help in detecting objects at multiple scales, improving the model's ability to detect objects of varying sizes.

### Default (Anchor) Boxes

SSD uses default (anchor) boxes to predict object locations and classes. For each default box, the model predicts:
- 4 offset values (for the bounding box coordinates)
- Confidence scores for each class
- 1 score for the background class

SSD produces a fixed-size collection of bounding boxes and corresponding confidence scores for the presence of object classes in those boxes.
