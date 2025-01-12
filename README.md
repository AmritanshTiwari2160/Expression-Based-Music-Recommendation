# Emotion-Based Music Recommendation AI System

This project integrates computer vision, deep learning, and a user-friendly web interface to recommend songs based on the user's emotions. The system uses facial landmark detection and hand gesture recognition to analyze emotional states in real-time and provides personalized song recommendations.

## Features
- **Real-Time Emotion Detection**: Utilizes facial landmarks and hand gestures for precise emotion recognition.
- **Customizable Recommendations**: Allows users to specify preferences for language and singer.
- **Web Interface**: Built using **Streamlit** with a live video stream for capturing emotions and generating recommendations.
- **Music Search Automation**: Automatically searches for music on YouTube based on detected emotion and user preferences.

## Technologies and Tools Used
1. **Python**: Core programming language for implementing the system.
2. **Mediapipe**: For facial landmark and hand gesture detection.
3. **OpenCV**: For video capturing and preprocessing.
4. **NumPy**: For data manipulation and handling.
5. **TensorFlow/Keras**: For building and training the deep learning model.
6. **Streamlit**: For creating an interactive web-based user interface.
7. **Streamlit-WebRTC**: For real-time video processing in the web app.
8. **AV**: For handling video frames during WebRTC streaming.
9. **YouTube Integration**: Directs users to music recommendations on YouTube using **webbrowser**.

## How the project works?
1. **Data Collection**:
   - The system captures facial and hand landmarks using a webcam.
   - Landmark data is preprocessed and stored in `.npy` files for training.

2. **Model Training**:
   - A fully connected neural network is built using Keras with layers optimized for emotion classification.
   - The model is trained on the collected landmark data and labels.

3. **Emotion Detection**:
   - The trained model predicts emotions in real-time based on facial and hand landmarks captured via webcam.

4. **Music Recommendation**:
   - The detected emotion is combined with user inputs (language and singer preferences).
   - The system searches YouTube for suitable songs and opens the results in a browser.

## Technical Highlights
- **Facial Landmark Detection**: Utilizes Mediapipe's **Holistic API** for precise detection of facial and hand landmarks.
- **Data Handling**: Stores and processes real-time data using **NumPy**.
- **Deep Learning Model**: The neural network architecture is designed to classify emotions effectively using input landmark data.
- **Real-Time Streaming**: Implements live video processing with **Streamlit-WebRTC** for an interactive user experience.

## Prerequisites
- Python 3.7 or higher
- Libraries: Mediapipe, OpenCV, TensorFlow, Keras, NumPy, Streamlit, Streamlit-WebRTC, AV
