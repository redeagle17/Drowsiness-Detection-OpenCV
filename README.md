# Drowsy Face Detection and Classification with YOLO

## Overview

This project aims to enhance safety in critical environments by developing a computer vision system that can detect and classify human faces as either drowsy or awake. It utilizes the YOLO (You Only Look Once) object detection model and a custom dataset generated by capturing images from a webcam and categorizing them with different labels.

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Dataset Collection](#dataset-collection)
- [Training](#training)

## Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

- Python 3.7
- OpenCV
- YOLO (You will need the YOLO weights and configuration files)
- Webcam (for capturing images)

Install OpenCV using pip:

```bash
pip install opencv-python
```

### Dataset Collection
To train a drowsy-awake classifier, a custom dataset needs to be collected. Follow these steps to create your dataset:

- Set up a webcam or camera.
- Capture images of faces in various states (drowsy and awake).
- Organize the images into appropriate folders, e.g., dataset/drowsy and dataset/awake.

### Training
Train the YOLO model with your custom dataset:

- Download the YOLO weights and configuration files.
- Configure YOLO for training using the provided configuration file.
- Start the training process by running the YOLO training script with your custom dataset
```bash
!yolo task=detect mode=train model=yolov5s.pt data=../content/drive/MyDrive/yolov5CustomTraining/dataset.yaml epochs=50 imgsz=320
```

### Usage

Once the YOLO model is trained, you can use it for real-time drowsy-awake face detection and classification. Run the following command:
```bash
python main.py
```


