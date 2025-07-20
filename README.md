
# 🧠 Real-Time Face Detection using OpenCV

This project uses **Python** and **OpenCV** to perform real-time face detection through a webcam. It uses Haar Cascade, a pre-trained classifier provided by OpenCV, to identify faces in each video frame and draws rectangles around them.

---

## 📸 Preview

- Real-time face detection using your webcam
- Green rectangles highlight detected faces
- Press **`q`** to exit the webcam window

---

## 📂 Project Structure

```

face-detection/
│
├── face\_detection.py        # Main Python script for detection
├── README.md                # Project documentation

````

---

## 🛠️ Technologies Used

- Python 3.x
- OpenCV (cv2)
- Haar Cascade Classifier

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/face-detection.git
cd face-detection
````

### 2. Install Dependencies

```bash
pip install opencv-python
```

### 3. Run the App

```bash
python face_detection.py
```

> ✅ Make sure your webcam is connected and not used by another application.

---

## 💡 How It Works

1. Loads Haar Cascade face detection model from OpenCV.
2. Captures frames from your webcam.
3. Converts each frame to grayscale.
4. Detects faces using `detectMultiScale()`.
5. Draws green rectangles around detected faces.
6. Displays the annotated frame.

---

## 🔍 Sample Code Snippet

```python
faces = face_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5)
for (x, y, w, h) in faces:
    cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)
```

---

## ❓ FAQ

* **Q:** How do I stop the program?

  * **A:** Press `q` on the keyboard in the video window.
* **Q:** What if I get an error loading the cascade?

  * **A:** Ensure OpenCV is correctly installed and has access to `haarcascade_frontalface_default.xml` via `cv2.data.haarcascades`.

