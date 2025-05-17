# hand_gesture🔊 Hand Gesture Volume Control using OpenCV & MediaPipe

This project uses computer vision to control the system volume with hand gestures. Using the distance between your thumb and index finger, it dynamically adjusts the system's master volume. A real-time webcam feed shows the finger tracking, gesture detection, and volume bar.
🧠 Features

    Real-time hand tracking using MediaPipe

    Volume control via the distance between thumb and index finger

    Visual feedback: Drawn circles, lines, and a volume bar

    Works with Windows OS using pycaw to access and manipulate system audio

📦 Requirements

Install the following Python libraries:

pip install opencv-python mediapipe numpy pycaw comtypes

🚀 How It Works

    Captures video feed from your webcam.

    Detects your hand and extracts landmark points (joints).

    Measures the distance between your thumb tip (id 4) and index finger tip (id 8).

    Maps this distance to a system volume range.

    Adjusts the system volume and displays a visual volume bar and percentage.

🎯 Usage

    Run the script:

    python volume_control.py

    Show your right hand to the camera.

    Move your thumb and index finger apart or closer to change the volume.

    Press the spacebar to exit the program.

🖼️ UI Elements

    Blue circles: Tips of thumb and index finger

    Blue line: Connection between the two

    Red bar: Volume level (moves with finger distance)

    Green text: Current volume percentage

⚠️ Notes

    Works only on Windows, due to pycaw dependency.

    Make sure your webcam is properly connected.

    Uses camera index 0 (default camera). Change it in cv2.VideoCapture(0) if needed.