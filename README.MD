# Real-time Face and Hand Tracking Application

## Overview
This application provides real-time face mesh and hand landmark detection using your computer's webcam. It utilizes MediaPipe's machine learning models to detect and visualize facial features and hand movements in a live video feed.

## Features
- **Face Mesh Detection**: Tracks and displays 468 facial landmarks in real-time
  - Facial contours
  - Face mesh tessellation
  - Iris tracking
- **Hand Tracking**: Simultaneously tracks both hands (up to 2 hands)
  - 21 3D landmarks per hand
  - Hand skeleton visualization
- **Real-time Processing**: Provides live visualization of tracking results
- **Automatic Model Download**: Downloads required MediaPipe models on first run
- **Cross-platform Support**: Works on Windows, macOS, and Linux
- **Error Handling**: Comprehensive camera permission and access error messages

## Technical Requirements
- Python 3.7+
- OpenCV (cv2)
- MediaPipe
- NumPy
- Webcam/Camera device

## Required Libraries
Install the required packages using pip:

```bash
pip install opencv-python mediapipe numpy requests
```

## Usage
1. Run the script:
```bash
python facetracker.py
```
2. Allow camera permissions when prompted
3. A window will open showing the tracking visualization
4. Press 'q' to quit the application

## Camera Permissions
- **macOS**: System Preferences > Security & Privacy > Privacy > Camera
- **Windows**: Settings > Privacy > Camera
- **Linux**: Ensure user has necessary camera access permissions

## Output Visualization
- Face mesh is displayed with connected landmarks
- Hand landmarks are shown with skeletal connections
- All visualizations are rendered on a black background for clarity
- Output is scaled by 1.5x for better visibility

## Models
The application automatically downloads two MediaPipe models on first run:
- `face_landmarker.task`: For facial landmark detection
- `hand_landmarker.task`: For hand landmark detection

Models are stored in a local `models/` directory.

## Error Handling
- Camera access errors
- Frame capture failures
- Model loading issues
- Runtime exceptions

## Controls
- **Exit**: Press 'q' or close the window
- **Window**: Resizable window for custom viewing size

## Performance
- Real-time processing capability
- Optimized for standard webcam frame rates
- Uses MediaPipe's float16 models for efficient processing

## Limitations
- Requires good lighting conditions for optimal tracking
- Performance may vary based on hardware capabilities
- Maximum of 2 hands can be tracked simultaneously
