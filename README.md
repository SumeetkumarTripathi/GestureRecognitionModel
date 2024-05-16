# Gesture Recognition Machine Learning Model

## Problem Statement
The objective is to develop a feature for a smart TV that recognizes five different gestures performed by the user, allowing control without using a remote. The gestures and their corresponding actions are:
- Thumbs down: Decrease the volume
- Left swipe: Jump backward 10 seconds
- Right swipe: Jump forward 10 seconds
- Stop: Pause the movie

## Dataset
The dataset comprises several hundred videos categorized into one of the five gesture classes. Each video, typically 2-3 seconds long, is divided into a sequence of 30 frames (images). These videos were recorded by various individuals performing the gestures in front of a webcam, akin to how the smart TV feature will operate.

## Objective
The project aims to implement and comprehend 3D convolutions as an extension of 2D convolutions for video data processing. By leveraging 3D convolutions, which capture spatiotemporal features, the goal is to extract meaningful information for tasks like action recognition, video classification, and motion analysis. Specific objectives include:
- Implementing 3D convolutional neural networks (CNNs) for video data processing.
- Understanding the analogy between 2D and 3D convolutions and their application in capturing spatiotemporal patterns.
- Investigating the impact of different filter sizes and architectures on 3D CNN performance.
- Exploring applications of 3D convolutions in computer vision tasks, such as action recognition and video classification.
- Evaluating the effectiveness and efficiency of 3D convolutional models compared to traditional 2D CNNs for video processing.

## Preprocessing Techniques
Preprocessing techniques employed include:
- Resizing images.
- Normalizing images.

## Observations
We created Eight models to determine the best accuracy. These models are as follows.
- ### VGG16 & RNN(GRU)
  - HyperParameters : `batch size=30` `frames=15`
  - Results: Training accuracy: `0.81` Validation accuracy `0.58`
  - Decision: Model overfitted the data
    
- ### RESNET-50
  - HyperParameters : `batch_size=30` `epochs=20` `frames=15` `Validation_steps=4` `weights=imagenet` `activation=relu` `loss=categorical_ crossentropy`
  - Results: Training accuracy: `0.9125` Validation accuracy `0.9100`
  - Decision: Model is accurate

- ### RESNET-50
  - HyperParameters : `batch_size=30` `epochs=30` `frames=15` `Validation_steps=4` `weights=imagenet` `activation=relu` `loss=categorical_ crossentropy`
  - Results: Training accuracy: `0.9065` Validation accuracy `0.8400`
  - Decision: Model is some what accurate
 
- ### RESNET-50
  - HyperParameters : `batch_size=30` `epochs=30` `frames=20` `Validation_steps=4` `weights=imagenet` `activation=relu` `loss=categorical_ crossentropy`
  - Results: On 23rd Epoch Training accuracy: `0.9472` Validation accuracy `0.9200`
  - Decision: Model is accurate
 
- ### CONV3D
  - HyperParameters : `batch_size=30` `epochs=15` `frames=20`
  - Results: Training accuracy: `0.9351` Validation accuracy `0.3700`
  - Decision: Model is highly overfitting
 
- ### CONV3D
  - HyperParameters : `height=width=84` `frames=25` `epochs=15`
  - Results: Training accuracy: `0.9261` Validation accuracy `0.5600`
  - Decision: Model is overfitting
 
- ### CONV3D
  - HyperParameters : `augmentation=invert color` `epochs=10` `frames=25`
  - Results: Training accuracy: `0.9306` Validation accuracy `0.1700`
  - Decision: Model is highly overfitting
 
- ### CONV3D
  - HyperParameters : `augmentation=invert color, horizontal flip` `epochs=2` `frames=25`
  - Results: NA
  - Decision: Model error received

  

## Conclusion
Among the models developed, `RESNET-50` yielded the highest performance, with a training accuracy of `94.72%` and a validation accuracy of `92%`. Thus, RESNET 50 is deemed the most suitable model for this task.
