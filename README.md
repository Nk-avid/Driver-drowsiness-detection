# Driver-drowsiness-detection

### README for Driver Drowsiness Detection System

```
# Driver Drowsiness Detection System

## Overview
The Driver Drowsiness Detection System aims to enhance road safety by providing timely alerts to drivers exhibiting signs of drowsiness. This project employs traditional computer vision techniques along with pre-trained models to accurately monitor driver behavior and detect drowsiness.

## Table of Contents
- [Features](#features)
- [Installation Instructions](#installation-instructions)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [Contact Information](#contact-information)

## Features
- Real-time detection of drowsiness through facial landmark tracking.
- Alerts for yawning and eye closure using eye aspect ratio (EAR) calculations.
- User-friendly interface with real-time feedback.

## Installation Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/driver-drowsiness-detection.git
   ```
2. Navigate to the project directory:
   ```bash
   cd driver-drowsiness-detection
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
```python
import cv2
from drowsiness_detector import DrowsinessDetector

detector = DrowsinessDetector()
video_capture = cv2.VideoCapture(0)

while True:
    ret, frame = video_capture.read()
    if not ret:
        break
    alert = detector.detect(frame)
    if alert:
        print("Drowsiness Detected! Please take a break.")
    cv2.imshow("Drowsiness Detection", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

video_capture.release()
cv2.destroyAllWindows()
```

## Technologies Used
- OpenCV for real-time image processing.
- Dlib for facial landmark detection.
- Python for implementing the drowsiness detection algorithm.

## Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request.

## Acknowledgements
- [Dlib](http://dlib.net/) for the facial landmark detection model.
- OpenCV for image processing functionalities.

## Contact Information
For inquiries, please reach out to Naveen Kumar at naveenavid.nk@gmail.com
```
