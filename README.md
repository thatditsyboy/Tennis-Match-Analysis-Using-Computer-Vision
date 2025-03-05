# 🎾 Tennis Match Analysis Project

## 📌 Overview
This project focuses on analyzing tennis match videos using **Computer Vision** techniques. It leverages deep learning models to detect players, track the ball, and extract key statistics such as shot speed and player movements. The system also maps real-world positions to a **mini-court representation** for enhanced visualization.

## ✨ Key Features
- **🎥 Video Processing**: Reads input video frames and saves processed output.
- **🤖 Computer Vision-based Detection**:
  - Player and ball detection using **YOLOv5**.
  - Court line detection via a **ResNet50-based model**.
- **🏆 Mini-Court Representation**: Converts player and ball positions into a scaled-down mini-court visualization.
- **📊 Statistics Calculation**:
  - Shot speed calculation.
  - Player movement tracking & speed estimation.
  - Aggregated match statistics.
- **📌 Visual Enhancements**:
  - Bounding boxes for players & ball.
  - Court keypoint annotations.
  - Mini-court overlay visualization.

## 🏗️ Project Structure
```
TENNIS ANALYSIS
│── court_line_detector/         # Court line detection module
│── input_videos/                # Folder to store input videos
│── mini_court/                  # Mini-court representation
│   │── __init__.py
│   │── mini_court.py
│── models/                      # Pre-trained models
│   │── keypoints_model.pth       # Court keypoints model
│   │── yolo5_best.pt             # YOLOv5 trained model
│── output_videos/               # Processed video outputs
│   │── output_video.avi
│── tracker_stubs/               # Detection outputs
│   │── ball_detections.pkl
│   │── player_detections.pkl
│── trackers/                    # Object tracking utilities
│── training/                     # Training scripts & notebooks
│── utils/                        # Utility scripts
│── main.py                       # Entry point of the application
│── yolo_inference.py             # YOLO inference script
│── yolov8x.pt                    # YOLOv8 model (optional)
```

## 📦 Dependencies
To run this project, install the required Python packages:
```bash
pip install -r requirements.txt
```

## 🚀 Usage
Run the main script to analyze an input tennis match video:
```bash
python main.py --input input_videos/match.mp4 --output output_videos/output.mp4
```

## 📂 Dataset & Pre-trained Models
### 🎾 Roboflow Tennis Dataset
This project uses the **Roboflow Tennis Ball Detection Dataset**:
🔗 [Roboflow Dataset Link](https://universe.roboflow.com/viren-dhanwani/tennis-ball-detection)

### 🏆 Pre-trained Models
1. **Trained YOLOv5 Model** for Player & Ball Detection  
   🔗 [Download YOLOv5 Model](https://drive.google.com/file/d/1UZwiG1jkWgce9lNhxJ2L0NVjX1vGM05U/view?usp=sharing)

2. **Trained Court Keypoints Model**  
   🔗 [Download Keypoints Model](https://drive.google.com/file/d/1QrTOF1ToQ4plsSZbkBs3zOLkVt3MBlta/view?usp=sharing)

## Output Video  
![Output Video](output_videos/output_video.mp4)



## 📜 License
This project is open-source and available under the **MIT License**.

---
🚀 **Developed with Computer Vision & Deep Learning for Tennis Analysis!** 🎾
