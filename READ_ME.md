# Self-Driving Car Project - CVI620

## Team Members

- Aryan Tuwar
- Aayushi Jitendra Thakkar
- Anh Chien Vu

## Project Description

We trained a convolutional neural network using the NVIDIA architecture to predict steering angles from front-facing dashcam images.

## Approach

- Data collected using simulator with left, center, and right images.
- Applied augmentation: flipping, brightness, image dropout, and cropping.
- Normalized input data and resized to (66x200).
- Used balanced dataset to reduce overfitting on straight path by removing excess 0 values.

## Major Challenges

- The car wouldn't move properly in the Simulator, especially when it approachs to the curve.
- Attempted fixes: I removed the excess values of 0 to make the dataset balanced, which not causing the biased as before. Additionally, I need to collect the data again by running the car in both sides of the road.

## Files Included

- `main.ipynb`: training logic
- `model.h5`: trained model
- `training_loss.png`: loss plot
- `demo_video.mp4`: simulation attempt
- `README.md`: this document
- `reviewData.ipynb`: review dataset

## How to Run

### Environment Setup

Required:

- Python 3.7 or 3.8
- TensorFlow 2.x
- OpenCV
- Flask
- eventlet
- socketio

### To Train

`python main.ipynb`

### To Test in Simulator

1. Open Simulator application
2. Run: `python TestSimulation.py model.h5`
