# Computer Vision Study Monitoring System

A real-time computer vision system designed to monitor smartphone usage during study sessions using classical image processing and object tracking techniques.

The system combines camera calibration, geometric pattern detection, visual sequence validation and real-time object tracking to estimate how frequently a smartphone is used during a study session.

---

## Overview

This project was developed as part of the **Computer Vision I** course within the Mathematical Engineering and Artificial Intelligence program at ICAI School of Engineering.

The objective was to design and implement a complete real-time computer vision pipeline using **Python and OpenCV**.

The system operates in two main stages:

1. A visual security mechanism detects and validates a predefined sequence of geometric patterns.
2. Once the sequence is successfully validated, the system activates a smartphone tracking module.

The tracker follows the smartphone within the video stream and records when the device appears or disappears from the scene, providing an approximate measure of interruptions during a study session.

---

## Key Features

- Real-time video processing
- Camera calibration and distortion correction
- Geometric pattern detection
- Visual sequence validation
- Smartphone object tracking
- Bounding-box visualization
- Smartphone usage event counting
- Real-time FPS monitoring
- Modular computer vision architecture

---

## Technologies

- **Python**
- **OpenCV**
- **NumPy**
- Computer Vision
- Image Processing
- Object Tracking
- Camera Calibration
- Real-Time Video Processing

---

## System Architecture

The computer vision pipeline follows the following sequence:

```text
Camera Input
     ↓
Camera Calibration
     ↓
Distortion Correction
     ↓
Geometric Pattern Detection
     ↓
Sequence Validation
     ↓
Smartphone Tracking
     ↓
Usage Event Detection
     ↓
Real-Time Visualization
```

The system remains locked until the correct sequence of visual patterns is detected.

After successful validation, the smartphone tracking module is activated and the system begins monitoring the device.

---

## Repository Structure

```text
.
├── Main.py
├── calibrate_camara.py
├── deteccion_funciones.py
├── secuencia_funciones.py
├── guardar_transformaciones.py
├── codigos previos/
├── VIDEO_DEMOSTRACIÓN.mp4
├── PROYECTO FINAL VISION.pptx
├── TRABAJO_FINAL_VISION (2).pdf
├── requirements.txt
└── README.md
```

---

## Main Components

### `Main.py`

Controls the complete execution pipeline and manages the real-time video processing workflow.

It integrates the different modules of the system and coordinates the transition between the security stage and the smartphone monitoring stage.

### `calibrate_camara.py`

Performs the camera calibration process.

The calibration parameters are used to correct lens distortion before the images are processed by the rest of the computer vision pipeline.

### `secuencia_funciones.py`

Implements the visual security mechanism.

It detects geometric patterns and verifies whether they appear in the predefined sequence required to unlock the monitoring system.

### `deteccion_funciones.py`

Implements the smartphone tracking module.

Once the security sequence has been validated, this module tracks the smartphone and monitors when the device appears or disappears from the scene.

### `guardar_transformaciones.py`

Contains utility functions used to save processed images and intermediate transformations.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/mariaromancanti/computer-vision-study-monitoring.git
```

Move into the project directory:

```bash
cd computer-vision-study-monitoring
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Before running the main system, the camera must be calibrated.

Run:

```bash
python calibrate_camara.py
```

The calibration process generates the parameters required for camera distortion correction.

Once the calibration has been completed, start the main application:

```bash
python Main.py
```

The system will open the camera feed and process the video stream in real time.

---

## System Workflow

### 1. Camera Acquisition

The system continuously captures frames from the camera.

### 2. Camera Correction

The previously obtained calibration parameters are applied to reduce lens distortion.

### 3. Visual Security System

The program detects predefined geometric patterns.

The user must provide the correct sequence before the system can continue.

### 4. Smartphone Tracking

After successful validation, the smartphone tracking module becomes active.

A bounding box is used to track the device across successive video frames.

### 5. Usage Monitoring

The system detects when the smartphone appears or disappears from the scene.

These events are counted as an approximate measure of smartphone usage during the study session.

### 6. Real-Time Visualization

The processed video stream is displayed together with relevant information about the system, including the current tracking state and FPS.

---

## Results

The project successfully integrates several classical computer vision techniques into a single real-time application.

The implemented system is capable of:

- detecting geometric visual patterns;
- validating a predefined visual sequence;
- controlling access to the monitoring system;
- tracking a smartphone in real time;
- displaying a bounding box around the tracked object;
- detecting smartphone appearance and disappearance events;
- estimating smartphone usage during study sessions;
- displaying real-time performance information.

The modular structure of the project also allows individual components to be modified or replaced independently.

---

## Demonstration

A demonstration video is included in the repository:

`VIDEO_DEMOSTRACIÓN.mp4`

The video shows the system operating in real time and demonstrates the interaction between the visual security mechanism and the smartphone tracking module.

---

## Possible Future Improvements

Several extensions could improve the capabilities of the system:

- Deep-learning-based smartphone detection
- Automatic smartphone detection without manual tracker initialization
- Multi-object tracking
- More robust tracking under changes in illumination
- Study-session analytics
- Usage statistics and visualization dashboards
- Automated generation of study-session reports
- Integration with a mobile or web application
- Cloud-based storage and analytics

A future version could replace the classical tracking approach with a deep-learning object detector to improve robustness and automate smartphone detection.

---

## Academic Context

This project was developed as a final project for the **Computer Vision I** course within the **Mathematical Engineering and Artificial Intelligence** program at **ICAI School of Engineering – Universidad Pontificia Comillas**.

The project focuses on applying computer vision concepts to a practical real-time monitoring problem.

---

## Author

**María Román Cantillana**

Mathematical Engineering & Artificial Intelligence  
ICAI School of Engineering – Universidad Pontificia Comillas

GitHub: [mariaromancanti](https://github.com/mariaromancanti)
