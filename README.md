# Driver-Drowsiness-Detection-System

🧠 Overview
This project is a Driver Drowsiness Detection System built using Python and key deep learning and multimedia libraries like Keras, TensorFlow, OpenCV, and Pygame.
The system monitors the driver's eyes in real-time using a webcam feed, and triggers an alarm if it detects signs of drowsiness.

🎯 Objective
The primary goal of this project is to detect driver drowsiness in real time and produce an audible alarm to alert the driver, thereby helping to prevent accidents due to fatigue or microsleep.

🛠️ Technologies Used
Python

TensorFlow – For deep learning model backend

Keras – For building and training the CNN model

OpenCV – For image capture and processing

Pygame – For playing alarm sound

🧰 Features
Real-time video capture from webcam

Eye detection using Haar cascade classifiers

Drowsiness detection using a trained deep learning model (CNN)

Alarm activation using Pygame when drowsiness is detected

Project Structure

Driver-Drowsiness-Detection/
│
├── Haar_Cascade_Files/              # Folder containing Haar cascade classifiers
│   ├── haarcascade_frontalface_alt.xml
│   ├── haarcascade_lefteye_2splits.xml
│   └── haarcascade_righteye_2splits.xml
│
├── models/                          # Folder containing trained model
│   └── cnnCat2.h5                   # Pre-trained CNN model for eye state classification
│
├── alarm.wav                        # Alarm sound file played on drowsiness detection
├── drowsiness detection.py          # Main script to run the detection system
├── model.py                         # Script used to train the CNN model
└── README.md                        # Project documentation

⚙️ How It Works
Face and eye detection is done using Haar cascade classifiers from OpenCV.

Captured eye regions are fed into a trained CNN model to determine if the eyes are open or closed.

If the system detects that the driver’s eyes remain closed beyond a threshold duration, an alarm is played to wake the driver.

📊 Model Details
Model Type: Convolutional Neural Network (CNN)

Input: Eye region images (grayscale, resized)

Output: Binary classification – Open (1) or Closed (0)

🔔 Alarm System
When drowsiness is detected, a sound alert is triggered using pygame.mixer.

You can replace the alarm.wav file with any custom sound.

🧪 Testing
To test the system:

Sit in front of your webcam.

Slowly close your eyes for a few seconds.

You should hear the alarm if your eyes stay closed long enough.

