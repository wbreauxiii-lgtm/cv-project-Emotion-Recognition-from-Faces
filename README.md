Emotion Recognition from Faces

Willie Lee Breaux III

Tier 2 Model

I chose this project because I am interested in robotics and in integrating artificial intelligence into robotics. Building an emotion recognition model allows me to explore the human-machine connection. Having natural interaction and adaptive robots that teach machines to understand human emotion is essential.

Problem Statement

In real-world applications, machines can recognize objects and faces but fail to understand human emotions. This lack of facial emotional awareness limits how technology interacts with human beings — for example, learning platforms cannot sense confusion, and customer service systems cannot detect frustration.

Solution Overview

This project uses a YOLO-based emotion recognition model trained on a Kaggle facial expression dataset and accelerated with GPU processing to classify emotions. The model can be applied in areas like customer sentiment analysis and human-AI interaction, where understanding human emotions helps machines respond naturally and accurately.

Technical Approach

CV Technique: Object Detection / Classification

Model: YOLOv11 Small (Ultralytics)

Framework: Kaggle Networks with PyTorch, Ultralytics, OpenCV

The YOLOv11 architecture supports both object detection and image classification. The variant YOLOv11s (the small variant) is faster, lightweight, and efficient — ideal for real-time emotion recognition tasks. Using Kaggle and Colab Notebooks provides a convenient environment that allows direct access to datasets and seamless GPU acceleration for faster model training and testing.

Dataset

Source: AffectNet

Size: Over 1 million images

Labels: Anger, Contempt, Disgust, Fear, Happy, Neutral, Sad, Surprise

Link: https://www.kaggle.com/datasets/fatihkgg/affectnet-yolo-format

Success Metrics

Primary Metric: Accuracy

Target: 70% accuracy

Secondary Metric: Speed

Week-by-Week Plan
Week	Focus
10	Proposal Stage
11	Implementation Begins
12	Testing & Improvement
13	Demo Creation
14	Final Polish
15	Final Presentation Day
Resources Needed

Compute: Google Colab Pro (NVIDIA A100 GPU, switched from T4 GPU) / Kaggle

Cost: $0

APIs: No paid APIs

Environment and Hardware

Platform: Google Colab

Hardware Accelerator: NVIDIA A100 GPU (switched from T4 GPU)

CUDA Version: 12.4

Frameworks: PyTorch 2.8.0, Ultralytics 8.3.225

Dataset Source: fatihkgg/affectnet-yolo-format (YOLO detection, 8 classes)
