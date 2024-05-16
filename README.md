# Gesture Recognition Machine Learning Model

## Problem Statement
Development of a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.
- Thumbs down: Decrease the volume
- Left swipe: Jump backwards 10 seconds
- Right swipe: Jump forward 10 seconds
- Stop: Pause the movie

## Dataset used for this project
https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL

## Data Understanding
The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

## Objective
The objective of this project is to implement and understand 3D convolutions as an extension of 2D convolutions for processing video data. While 2D convolutions are commonly used for image processing tasks, 3D convolutions provide a natural extension to analyze spatiotemporal features within videos. By leveraging the temporal dimension inherent in video sequences, we aim to extract meaningful features for tasks such as action recognition, video classification, and motion analysis.
This project seeks to
- Implement 3D convolutional neural networks (CNNs) to process video data represented as sequences of RGB images.
- Explore the analogy between 2D and 3D convolutions, understanding how filters move across three dimensions (x, y, and z) to capture spatiotemporal patterns.
- Study the impact of different filter sizes and architectures on the performance of 3D CNNs for video analysis tasks.
- Investigate applications of 3D convolutions in computer vision tasks, including but not limited to action recognition and video classification.
- Evaluate the effectiveness and efficiency of 3D convolutional models compared to traditional 2D CNNs for video processing tasks.
By achieving these objectives, this project aims to contribute to the advancement of techniques for analyzing and understanding video data using deep learning approaches, thereby opening avenues for applications in fields such as surveillance, robotics, healthcare, and entertainment.

## Preprocessing Techniques used
- Resizing Images.
- Normalization of images.

## Observations
Seven models were made in order to get the most accurate model that can perform the task.
- VGG16 & RNN(GRU ): Train accuracy: 0.81 and Validation accuracy 0.58 | Model overfitted
