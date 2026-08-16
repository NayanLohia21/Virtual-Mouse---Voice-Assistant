# Gesture-Controlled Virtual Mouse

A computer-vision based virtual mouse that lets users interact with a Windows computer using hand gestures. The project uses a webcam to track hand landmarks and translates recognized gestures into mouse actions such as cursor movement, clicking, scrolling, dragging, volume control, and brightness control.

## Overview

This project explores touch-free human-computer interaction using computer vision and hand tracking.

The main idea is simple:

**Webcam → Hand Tracking → Gesture Detection → Mouse/System Action**

No dedicated external hardware is required apart from a webcam.

## Key Features

### 🖱️ Cursor Control
Move the mouse cursor by positioning your hand in front of the webcam.

### 👆 Mouse Clicks
Gesture-based controls for:
- Left click
- Right click
- Double click

### 🖐️ Drag and Drop
Use a hand gesture to hold and move items between locations on the desktop.

### 📜 Scrolling
Control vertical and horizontal scrolling using dynamic hand movements.

### 🔊 Volume Control
Adjust system volume through hand movement.

### 💡 Brightness Control
Change the display brightness using gesture-based controls where supported by the system.

### 📂 Multiple Selection
Use gestures to select multiple desktop or file-system items.

### 🎙️ Voice Commands
The project can also provide voice-based computer interaction, including commands for:
- Starting and stopping gesture recognition
- Searching the web
- Opening locations in Google Maps
- Navigating files and directories
- Copy and paste operations
- Checking the current date and time
- Pausing and resuming voice interaction
- Exiting the assistant

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application development |
| OpenCV | Webcam capture and image processing |
| MediaPipe | Hand landmark detection |
| PyAutoGUI | Mouse and keyboard automation |
| Speech Recognition | Voice command processing |
| Windows APIs / utilities | System-level controls |
| NumPy | Numerical and coordinate processing |

## System Requirements

- Windows
- Python 3.x
- Working webcam
- Microphone for voice-command functionality
- Internet connection for web-based voice commands

> The exact Python/package versions should match the versions specified in `requirements.txt` for this project.

## Installation

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

**Windows CMD:**

```bash
.venv\Scripts\activate
```

**Windows PowerShell:**

```powershell
.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

If a package fails to install, check the package's documentation and the Python version required by the dependency.

## Running the Project

Run the main application from the project's source directory:

```bash
python <main_file>.py
```

If the repository contains separate gesture-recognition and voice-assistant entry points, run the appropriate module described by the source code.

## How It Works

### 1. Capture

The webcam continuously captures frames.

### 2. Hand Detection

The computer-vision pipeline identifies the user's hand and extracts landmark positions.

### 3. Gesture Analysis

Landmark coordinates are analyzed to determine the current hand state and movement.

### 4. Action Mapping

Recognized gestures are mapped to computer actions.

For example:

```text
Hand Movement
      ↓
Hand Landmarks
      ↓
Gesture Classification
      ↓
Action Mapping
      ↓
Mouse / Keyboard / System Action
```

## Project Structure

A typical structure for the project is:

```text
Gesture-Controlled-Virtual-Mouse/
│
├── src/
│   ├── Gesture_Controller.py
│   ├── Proton.py
│   └── ...
│
├── demo_media/
├── requirements.txt
├── README.md
└── ...
```

The exact files may vary depending on the implementation.

## Gesture Mapping

The gesture mapping can be customized according to the implementation. Typical controls include:

| Interaction | Gesture / Movement |
|---|---|
| Move cursor | Hand position |
| Left click | Click gesture |
| Right click | Alternate click gesture |
| Double click | Double-click gesture |
| Scroll | Pinch/movement gesture |
| Drag | Hold gesture + movement |
| Volume | Pinch distance / movement |
| Brightness | Pinch distance / movement |

## Configuration

Gesture thresholds, movement sensitivity, smoothing, and action mappings can be adjusted in the source code.

For a better user experience, consider exposing these values through a configuration file or settings interface.

## Performance Tips

For smoother tracking:

- Use adequate lighting.
- Keep the hand within the camera's field of view.
- Avoid highly cluttered backgrounds.
- Use a stable webcam position.
- Adjust cursor sensitivity and smoothing values when necessary.
- Close unnecessary applications if CPU usage becomes high.

## Limitations

- Performance depends on webcam quality and lighting.
- Fast hand movements can occasionally produce incorrect gesture detection.
- Some system-level controls are Windows-specific.
- Voice recognition accuracy depends on microphone quality and environmental noise.
- Different screen resolutions may require cursor-coordinate calibration.

## Future Improvements

Possible improvements include:

- Custom gesture configuration
- User-specific gesture profiles
- Better cursor smoothing
- Gesture calibration
- Multi-hand interaction
- Improved low-light detection
- Cross-platform support
- Graphical settings interface
- Performance monitoring
- Additional accessibility controls
- Custom voice-command configuration

## Responsible Use

This project is intended for experimentation, learning, accessibility, and human-computer interaction research.

Use automated mouse and keyboard actions carefully, especially when interacting with applications that can modify or delete important data.

## Credits and Licensing

This repository should retain or comply with the license and attribution requirements of any third-party code, models, libraries, or assets that are reused.

If you substantially modify or replace an existing implementation, document those changes clearly and follow the applicable licenses.

## Author

**Nayan Loya**

GitHub: https://github.com/NayanLohia21

---

### Project Status

🚧 **Active Development**

The project can be extended with additional gestures, configurable controls, improved tracking, and a dedicated user interface.
