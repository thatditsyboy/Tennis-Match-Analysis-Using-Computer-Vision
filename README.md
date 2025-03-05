# Tennis Match Analysis Project

## Overview
This project leverages **Computer Vision** techniques to analyze tennis match videos by detecting players and the ball, tracking their movements, and calculating various statistics. It utilizes **deep learning models**, including **YOLO** for object detection and **ResNet50** for court line detection. The system also provides a **mini-court representation** for better visualization.

## Features
- **Video Processing**: Read input video frames and save the processed output video.
- **Player and Ball Detection**: Detect players and the ball using YOLO models.
- **Court Line Detection**: Identify court lines and keypoints using a pre-trained **ResNet50 model**.
- **Mini-Court Representation**: Convert detected positions to a smaller court representation.
- **Statistics Calculation**: Compute player and ball speeds, shot speeds, and other match statistics.
- **Visualization**: Overlay bounding boxes, court keypoints, mini-court positions, and statistics on video frames.

## Directory Structure
```
TENNIS ANALYSIS
│── court_line_detector/      # Court line detection logic
│── input_videos/             # Folder for input match videos
│── mini_court/               # Code for mini-court conversion
│   ├── __init__.py
│   ├── mini_court.py
│── models/                   # Pre-trained models for detection
│   ├── keypoints_model.pth
│   ├── yolo5_best.pt
│── output_videos/            # Processed video outputs
│   ├── output_video.avi
│── tracker_stubs/            # Stub files for object tracking
│   ├── ball_detections.pkl
│   ├── player_detections.pkl
│── trackers/                 # Tracking algorithms
│── training/                 # Training scripts and datasets
│   ├── tennis-ball-detection-6/
│   ├── tennis_ball_detector_training.ipynb
│   ├── tennis_court_keypoints_training.ipynb
│── utils/                    # Utility functions
│── main.py                   # Entry point of the project
│── yolo_inference.py         # YOLO inference script
│── yolov8x.pt                # YOLOv8 model file
```

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- OpenCV
- PyTorch
- TensorFlow (if needed for additional models)
- YOLO dependencies (`ultralytics` for YOLOv8)

### Installation Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo-name/tennis-analysis.git
   cd tennis-analysis
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Place input videos in the `input_videos/` folder.
4. Run the main script:
   ```sh
   python main.py
   ```

## Usage
1. **Run `main.py`** to process a match video.
2. **Results**: The processed video with overlays will be saved in `output_videos/`.
3. **Training**: If needed, retrain the models using notebooks in `training/`.

## Model Details
- **YOLO** is used for **player and ball detection**.
- **ResNet50** is used for **court keypoint detection**.
- Tracking is implemented using **custom tracking algorithms**.

## Future Enhancements
- Improve player tracking accuracy with Kalman Filters.
- Add real-time processing capabilities.
- Implement a dashboard for match statistics visualization.

## Contributors
- **Abhishek Sarkar** - ML Enthusiast


## License
This project is licensed under the MIT License. See `LICENSE` for details.
