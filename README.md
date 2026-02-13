# potato-disease-classification

# Cylinder Counting from Moving Truck (Top View)

## Overview
This project implements an automated system to detect and count gas cylinders from a top-view video of a moving truck using OpenCV. The solution avoids double counting and is robust to motion, noise, and partial occlusions.

---

## Features
- Cylinder detection using Hough Circle Transform
- Automatic truck presence detection
- Robust median-based counting
- Annotated output video
- CSV logs for analysis
- Evaluation metrics (MAE, MAPE, Accuracy)

---

## Tech Stack
- Python 3
- OpenCV
- NumPy

---

## Approach
1. Extract a fixed Region of Interest (ROI) where the truck appears
2. Preprocess ROI (resize, grayscale, blur)
3. Detect cylinders using circle detection
4. Track truck presence based on cylinder count
5. Use median value across frames for final count
6. Save results and metrics

---

## How to Run

### 1. Open Google Colab
Go to: https://colab.research.google.com/
- Upload the provided .ipynb file to Google Colab
- Open it

### 2. Install Dependencies
pip install opencv-python numpy

### 3. Upload Input Video (Drag & Drop)
Task.mp4

### 4. Run All Cells
- Click Runtime → Run all
- The notebook will:
    - Process the video
    - Detect and count cylinders
    - Identify trucks
    - Generate annotated output

### 5. Output Files Generated
After execution, these files will be created:
| File Name          | Description                             |
| ------------------ | --------------------------------------- |
| `output.mp4`       | Annotated video with detected cylinders |
| `truck_counts.csv` | Final cylinder count per truck          |
| `frame_log.csv`    | Frame-wise detection log                |


### 6. Download Output Files

## Expected Output
- Total cylinder count per truck
- Annotated video showing:
    - Detected cylinders (green circles)
    - Stable counting per truck
    - CSV report with final counts

---

## Evaluation Metrics

MAE (Mean Absolute Error)

MAPE (Mean Absolute Percentage Error)

Counting Accuracy

Stability Score (Standard Deviation)

---

## Sample Result
Truck 1: 139 cylinders
Truck 2: 116 cylinders
Accuracy: 85%

---

## Assumptions

- Video is captured from top view

- Cylinders appear approximately circular

- Truck passes fully through ROI

---

## Future Work

- YOLO-based truck detection

- Multi-truck simultaneous tracking

- Real-time optimization
