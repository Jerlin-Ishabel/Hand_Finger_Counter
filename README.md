

## 🖐️ Hand Finger Counter using MediaPipe & OpenCV

### 🔍 Project Overview

This project is a real-time **hand gesture recognition system** built using **Python**, **MediaPipe**, and **OpenCV**. It detects **one or two hands** from a webcam feed and **counts the number of fingers** being held up — from 0 to 10.

It uses **MediaPipe Hands**, a powerful hand tracking solution by Google, to detect hand landmarks, and **OpenCV** to process the video and display the results.

---

### 🎯 Key Features

* 👋 Detects and tracks **both hands**
* ✋ Accurately counts up to **10 fingers**
* 📷 Real-time webcam processing
* 🔧 Uses **21 hand landmarks** per hand
* ✅ Supports thumbs (based on horizontal position) and fingers (based on vertical landmarks)

---

### 🛠️ How It Works

* **MediaPipe** identifies 21 landmark points on each detected hand.
* The **tip landmarks** for each finger are compared with their preceding joints to determine if the finger is **up** or **down**.
* The **thumb** is detected using **x-axis comparison**, and the other fingers are based on the **y-axis**.
* A **total finger count** is displayed on the video feed.

---

### 📌 Technologies Used

* 🐍 Python 3.13
* 🖼️ OpenCV for video and drawing
* 🖐️ MediaPipe for hand detection and landmark tracking

---

### 🔢 Finger Landmark Logic

* **Thumb**: `tip (4)` compared with `landmark 3` (x-axis)
* **Other Fingers**: `tip (8, 12, 16, 20)` compared with `landmark - 2` (y-axis)

---

### 🧪 Run the Project

```bash
# Install required packages
pip install opencv-python mediapipe

# Run the script
python finger_counter.py
```

> Press `q` to quit the webcam window.

---

### 📸 Output

> ✅ Real-time video feed with detected hand landmarks
> ✅ Finger count displayed as: `Total Fingers: X`
> ✅ Counts up to 10 fingers across both hands

---
### 💡 Use Cases

* Educational tools for kids learning finger counting
* Gesture-controlled interfaces
* Interactive gaming or AR
* Sign language research

---


