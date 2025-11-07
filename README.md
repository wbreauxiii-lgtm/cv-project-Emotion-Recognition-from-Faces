## Emotion Recognition from Faces  

- **Author:** Willie Lee Breaux III  

---

## Tier 2 Model  

- I chose this project because I am interested in robotics and integrating artificial intelligence into robotics.  
- Building an emotion recognition model allows me to explore the human-machine connection.  
- Having natural interaction and adaptive robots that teach machines to understand human emotion is essential.  

---

## Problem Statement  

- In real-world applications, machines can recognize objects and faces but fail to understand human emotions.  
- This lack of emotional awareness limits how technology interacts with people.  
- For example, learning platforms cannot sense confusion, and customer service systems cannot detect frustration.  

---

## Solution Overview  

- This project uses a YOLO-based emotion recognition model trained on a Kaggle facial expression dataset.  
- The model is GPU-accelerated for faster processing and emotion classification.  
- It can be applied in areas such as customer sentiment analysis and human–AI interaction, where understanding emotions helps machines respond naturally and accurately.  

---

## Technical Approach  

- **CV Technique:** Object Detection / Classification  
- **Model:** YOLOv11 Small (Ultralytics)  
- **Frameworks:** PyTorch, Ultralytics, OpenCV (on Kaggle/Colab)  
- The YOLOv11 architecture supports both detection and classification.  
- The small variant, YOLOv11s, is fast and lightweight — ideal for real-time emotion recognition.  
- Using Kaggle and Colab notebooks provides dataset access and GPU acceleration for efficient training.  

---

## Dataset  

- **Source:** AffectNet  
- **Size:** Over 1 million images  
- **Labels:** Anger, Contempt, Disgust, Fear, Happy, Neutral, Sad, Surprise  
- **Link:** https://www.kaggle.com/datasets/fatihkgg/affectnet-yolo-format  

---

## Success Metrics  

- **Primary Metric:** Accuracy (Target: 70%)  
- **Secondary Metric:** Speed / Real-time performance  

---

## Week-by-Week Plan  

- **Week 10:** Proposal Stage  
- **Week 11:** Implementation Begins  
- **Week 12:** Testing & Improvement  
- **Week 13:** Demo Creation  
- **Week 14:** Final Polish  
- **Week 15:** Final Presentation Day  

---

## Resources Needed  

- **Compute:** Google Colab Pro NVIDIA A100 GPU (switched from T4 GPU) / Kaggle  
- **Cost:** $0  
- **APIs:** No paid APIs  

---

## Environment and Hardware  

- **Platform:** Google Colab  
- **Hardware Accelerator:** NVIDIA A100 GPU (switched from T4 GPU)  
- **CUDA Version:** 12.4  
- **Frameworks:** PyTorch 2.8.0, Ultralytics 8.3.225  
- **Dataset Source:** fatihkgg/affectnet-yolo-format (YOLO detection, 8 classes)  
