# People Tracking with YOLOv8 and ByteTrack
*This project uses YOLOv8 for person detection and ByteTrack for multi-object tracking to count people entering and exiting through the frame boundaries or specific zones in a video.*

[DEMO.webm](https://github.com/user-attachments/assets/4404b66a-b1cc-451f-a46b-46df98dd15a2)


## ~How It Works
- YOLOv8 detects people in the frame.
- ByteTrack assigns unique IDs to each person.
- Zone logic and side-boundary logic track movement across zones and frame edges.
- utils.py provides helper functions like drawing boxes, checking positions, and updating counts.

## Features
- Detects and tracks people in real-time using YOLOv8 and ByteTrack.
- Counts entries and exits through all 4 sides: top, bottom, left, right.
- Counts entries and exits through custom-defined zones (e.g., doors).
- Draws bounding boxes with ID and FPS overlay.
- Saves the output to a video file.

## Requirements

Before running the project, ensure that you have the following libraries installed:

### Dependencies

- Python (3.8 or higher)
- `opencv-python` – For video processing.
- `torch` – For running YOLOv8.
- `numpy` – For handling arrays and computations.
- `matplotlib` – For visualizing results (optional).
- `ByteTrack` – For object tracking.
-  **Maybe some of the dependencies are missing but you can install it by yourself**

## 🚀 Running the App
Run the script using:
```
python main.py
```
Press q to quit the display window.

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/PeopleTracking.git
cd PeopleTracking
```
Create a Virtual Environment (Optional but Recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

## Install dependencies:
Install the required Python libraries:
```bash
pip install -r requirements.txt
pip install opencv-python torch numpy matplotlib
```

## Download YOLOv8 Weights:
```bash
pip install ultralytics
```

## 📂 Project Structure
```
plaintext
project_root/
├── main.py               # Main script for running detection, tracking, and counting
├── config.py             # Configurations such as video source, resolution, zone positions
├── utils.py              # Helper functions: draw boxes, update counts, zone checks
├── output/               # Output folder where processed video will be saved
│   └── people_outputnew2.mp4
└── data/
    └── people.mp4        # Input video for testing
```

