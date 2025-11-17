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
- The small variant, YOLOv11s, is fast and lightweight, ideal for real-time emotion recognition.  
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

## Risks and Mitigation  

- **Risk 1: Training interruption or GPU timeout**  
  - *Mitigation:* Use Google Colab Pro with A100 GPU and save checkpoints to Google Drive after every 10 epochs using save_period=10.

- **Risk 2: Dataset size and limited compute time**  
  - *Mitigation:* Train on smaller image batches or subsets of AffectNet to verify performance before full-scale runs.

- **Risk 3: Model overfitting on limited facial variations**  
  - *Mitigation:* Apply data augmentation (blur, rotation, flip) and monitor validation accuracy to prevent overfitting.

- **Risk 4: Low detection accuracy across all emotions**  
  - *Mitigation:* Tune learning rate, increase epochs, and test alternate YOLO variants (e.g., YOLOv11m or YOLOv11n).

- **Risk 5: Runtime or dependency mismatch**  
  - *Mitigation:* Freeze library versions in requirements.txt and document environment setup in README for reproducibility.

## 📈 Model Results (Week 12)

After 100 epochs of training on the A100 GPU:

| Metric | Score |
|--------|-------|
| Precision (P) | 0.757 |
| Recall (R) | 0.773 |
| mAP@50 | 0.849 |
| mAP@50-95 | 0.849 |

| Class | mAP@50 |
|------|--------|
| Anger | 0.851 |
| Contempt | 0.864 |
| Disgust | 0.837 |
| Fear | 0.866 |
| Happy | 0.961 |
| Neutral | 0.752 |
| Sad | 0.798 |
| Surprise | 0.865 |

**Saved Artifacts**  
- `best.pt` → `/models/`
- `confusion_matrix.png` → `/results/`
- `results.png` → `/results/`

**Failure Case Notes**  
- Neutral faces are often misclassified as Sad or Contempt  
- Dim/low-contrast images reduce prediction accuracy  
- Occlusions (hands on face) can cause incorrect detection

**Improvement Made**  
- Switched training hardware from T4 → A100 GPU for faster convergence and higher mAP



