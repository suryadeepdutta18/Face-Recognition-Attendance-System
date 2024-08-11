**Project Overview:**

The Face Recognition Attendance System is a computer vision application designed to automate the process of attendance tracking using face recognition technology. The system captures real-time video from a webcam, detects faces, and recognizes individuals to mark their attendance. It saves the attendance records in a CSV file, including timestamps and recognized names.

**Key Features:**

**Face Detection and Recognition:**

Utilizes OpenCV for real-time face detection and recognition.
Employs a K-Nearest Neighbors (KNN) classifier to identify individuals based on facial features.

**Attendance Management:**

Records attendance details in a CSV file with timestamps.
Handles both new and existing records by appending to or creating new CSV files as necessary.

**User Interaction:**

Provides real-time feedback and notifications through voice prompts using the win32com.client library.
Displays video feed with detected faces and recognized names.

**Data Handling:**

Manages face data and labels using pickle for serialization and deserialization.
Updates and maintains datasets for training and prediction.

**Technology Used:**

OpenCV: For video capture, face detection, and image processing.
K-Nearest Neighbors (KNN): For face recognition using the sklearn library.
Python Pickle: For saving and loading face data and labels.
CSV: For recording and managing attendance data.
win32com.client: For text-to-speech functionality to provide audio feedback.

**Files and Their Functions:**

**test.py:**

**Purpose:** Main script for real-time face recognition and attendance marking.
**Functions:**
Captures video from the webcam.
Detects faces and recognizes individuals.
Saves attendance data to a CSV file.
Provides audio feedback when attendance is marked.
Libraries Used: OpenCV, scikit-learn, pickle, CSV, datetime, win32com.

**add_faces.py:**

**Purpose:** Script for collecting and adding new facial data for training the model.
**Functions:**
Captures and processes face images from the webcam.
Adds new face data to existing datasets or creates new datasets if they don't exist.
Updates pickle files with new face data and names.
Libraries Used: OpenCV, NumPy, pickle, OS.

**Workflow:**
**Training:**

Run add_faces.py to capture and add new face data to the system.
Faces and names are stored in pickle files for later use in the recognition model.

**Attendance Taking:**

Run test.py to start the face recognition and attendance marking process.
The system detects faces, recognizes individuals, and logs their attendance in real-time.
Attendance records are updated in a CSV file, and audio feedback is provided for confirmation.
This system is ideal for environments where automated and reliable attendance tracking is needed, such as educational institutions or corporate offices.
