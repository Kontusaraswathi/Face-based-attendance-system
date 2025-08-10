# Face-based-attendance-system

## Overview
This project implements a **Face Recognition Based Attendance System** using Python, OpenCV, and SQLite.  
It allows adding new faces to the database, recognizing faces in real-time, and marking attendance automatically.

The system uses:
- **Haar Cascade Classifier** for face detection
- **LBPH Face Recognizer** (or similar algorithm) for face recognition
- **SQLite database** for storing attendance
- **Image dataset** for training and recognition

---

## 🚀 Features
- Add new faces and store them with a unique ID
- Train the model with captured face images
- Real-time face detection & recognition using webcam
- Automatic attendance marking in the database
- Sound alert (`siren.wav`) for specific events (optional)
- User-friendly modular code (`face_adder.py`, `face_recogniser.py`, `main.py`)

---

## 📂 Project Structure
Face Recognition based Attendance with sql/
│── pycache/ # Compiled Python files
│── train_images/ # Captured face images for training
│── atten # SQLite database file
│── face_adder.py # Script to add new faces
│── face_recogniser.py # Script to recognize faces & mark attendance
│── haarcascade_frontalface_default.xml # Haar Cascade model for face detection
│── main.py # Main entry point to run the system
│── requirements.txt # Python dependencies
│── siren.wav # Sound alert

## Install dependencies
pip install -r requirements.txt

## Usage
Step 1: Add New Face
python face_adder.py
Enter the ID and Name when prompted.
The system captures multiple images of the face and stores them in train_images/.

Step 2: Train the Model
Training may be part of face_recogniser.py or a separate function inside it.

Step 3: Recognize Faces & Mark Attendance
python face_recogniser.py
Opens webcam
Detects and recognizes faces
Marks attendance in atten SQLite DB

Step 4: View Attendance
You can use any SQLite viewer or Python script to view records from atten.

