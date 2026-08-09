# YOLO Video Object Tracking: ByteTrack vs. BoT-SORT

## Problem Statement

Object detection can locate people in each video frame, but it does not preserve identity across time. This project examines how multi-object trackers assign persistent IDs and where those identities can fail.

## Approach

I used an Ultralytics YOLO detector with ByteTrack and BoT-SORT on the same video clip. I counted the real people manually, compared that number with each tracker's unique-ID count, and examined short tracks and likely identity switches.

## Technologies Used

- Python and Google Colab
- Ultralytics YOLO
- ByteTrack
- BoT-SORT
- OpenCV
- NumPy and Matplotlib

## Dataset

The notebook downloads the short demonstration video used in the course lab. The video itself should not be uploaded to the repository unless its license and size permit redistribution. The notebook should retain the download or access instructions.

## Results

| Measurement | ByteTrack | BoT-SORT |
|---|---:|---:|
| Unique track IDs | 79 | 74 |
| Short tracks | 24 | 21 |
| Longest track | 10.00 seconds | 10.00 seconds |

The manual count was **73 distinct people**. BoT-SORT was closer to the manual count, producing 74 unique IDs compared with ByteTrack's 79.

One likely identity switch occurred around frames 81–83: ID 19 disappeared and ID 135 appeared nearby after a two-frame gap at an estimated distance of 17.5 pixels.

## Key Findings

- Tracking adds temporal identity to frame-by-frame detections.
- A unique-ID count can overestimate the true number of people when one person receives multiple IDs.
- Short tracks may indicate brief visibility, missed detections, occlusion, or track fragmentation.
- Appearance cues can help BoT-SORT maintain identities in situations where motion alone is insufficient.

## How to Run

1. Open `ITAI1378_Lab10_Amoye.ipynb` in Google Colab.
2. Change the runtime to GPU if available.
3. Run all cells from top to bottom.
4. Confirm that the video outputs and tracker statistics are visible.

## Repository Files to Add

- `ITAI1378_Lab10_Amoye.ipynb` — completed notebook with visible outputs
- `results/bytetrack_result.png`
- `results/botsort_result.png`
