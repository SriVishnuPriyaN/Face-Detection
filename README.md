🧠 Real-Time Face Detection with OpenCV
This project uses OpenCV and Haar Cascade to detect human faces from webcam input in real-time.

📸 Preview
✅ The webcam opens and detects faces, drawing green rectangles around them.
❌ Press q to exit the window.

📂 Project Structure
bash
Copy
Edit
face-detection/
│
├── face_detection.py        # Your main detection script
├── README.md                # Project info
🛠️ Technologies Used
Python 3.x

OpenCV (cv2)

Haar Cascade (Pre-trained classifier)

🔧 Setup Instructions
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/face-detection.git
cd face-detection
2. Install Dependencies
bash
Copy
Edit
pip install opencv-python
3. Run the App
bash
Copy
Edit
python face_detection.py
✅ Make sure your webcam is connected and accessible.

💡 How It Works
Loads the pre-trained Haar Cascade face detection model.

Captures live frames from the webcam.

Converts the frame to grayscale.

Detects faces using detectMultiScale().

Draws green rectangles around detected faces.

Displays output in a window.

🧠 Algorithm Used
Haar Cascade Classifier from OpenCV:

Detects features in grayscale images.

Parameters like scaleFactor and minNeighbors help control accuracy and performance.

🖼️ Sample Code Highlights
python
Copy
Edit
faces = face_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5)
for (x, y, w, h) in faces:
    cv2.rectangle(frame, (x, y), (x + w, y + h), (0, 255, 0), 2)
❓ FAQ
Q: How do I stop the program?
A: Press q in the window displaying the webcam.

Q: What if I see “Error loading face cascade”?
A: Make sure haarcascade_frontalface_default.xml is accessible via OpenCV's cv2.data.haarcascades.

📄 License
MIT License. Free to use and modify.

✍️ Author
Vishnu Priya

