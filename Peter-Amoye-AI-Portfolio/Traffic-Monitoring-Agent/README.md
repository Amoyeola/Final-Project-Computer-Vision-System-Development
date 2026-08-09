# SmartFlow: Multi-Agent Traffic Monitoring and Zone Analytics

## Problem Statement

Traffic-monitoring teams need timely information about vehicle movement, congestion, and activity in defined road zones. Manual review is slow, inconsistent, and difficult to audit across multiple recordings. SmartFlow converts roadway video into repeatable traffic reports with saved evidence explaining every decision.

## Approach

SmartFlow uses three agents for perception, analysis, and reporting. YOLO11 detects vehicles, ByteTrack maintains identities, and transparent thresholds classify traffic as LOW, MODERATE, or HIGH. The reporting stage saves annotated video, a text report, CSV frame observations, and a JSON trace of agent handoffs.

## Technologies Used

- Python and Google Colab
- Ultralytics YOLO11
- OpenCV
- ByteTrack multi-object tracking
- Python dataclasses
- CSV and JSON reporting
- Jupyter Notebook

## Dataset

The project evaluates four original traffic videos plus six robustness variants covering blur, darkness, grayscale, low resolution, center-block occlusion, and a short clip. Large source and result videos should only be uploaded when GitHub size limits and redistribution rights permit it.

## Results

- All 10 of 10 pipeline scenarios completed.
- The original `IMG_8257` recording produced 74 tracks and 29 crossings and was classified HIGH.
- The original `IMG_8259` recording produced 50 tracks and 20 crossings and was classified HIGH.
- Center-block occlusion reduced 50 tracks to 14 and 20 crossings to 6.
- Low resolution increased the same scene from 50 to 62 tracks because pixelation fragmented identities.
- Mean processing speed was approximately 37 processed frames per second on a Colab T4 GPU.

## Key Findings

- Video-orientation metadata must be handled correctly; rotating the MOV input resolved a zero-detection failure.
- Explainable thresholds make each traffic classification and selected action auditable.
- Occlusion causes missed detections, while low resolution can fragment tracks and inflate counts.
- Responsible deployment requires privacy controls, limited retention, and future face and license-plate blurring.

## How to Run

1. Open `SmartFlow_03_demo.ipynb` in Google Colab.
2. Select a GPU runtime if available.
3. Run all cells from top to bottom.
4. Upload or download the demonstration video when prompted.
5. Review the generated detections, tracks, and analytics.

## Repository Files to Add

- `SmartFlow_03_demo.ipynb` — completed capstone notebook with visible outputs
- `SmartFlow_Final_Presentation.pdf` — 12-slide capstone presentation
- `results/detection_sample.png`
- `results/tracking_sample.png`
- `results/analytics_result.png`
