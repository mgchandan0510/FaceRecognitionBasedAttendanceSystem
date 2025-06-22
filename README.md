Here's a `README.md` file for your **Face Recognition Attendance System** project:

---

```markdown
# 👁️‍🗨️ Face Recognition-Based Attendance System

A real-time face recognition-based attendance system built using **Python**, **OpenCV**, **Flask**, and **K-Nearest Neighbors (KNN)**. This system captures facial data, trains a model, and marks attendance through live webcam video feed. It also logs attendance with timestamp and prevents duplicate entries.

---

## 🚀 Features

- 📷 Real-time Face Detection and Recognition
- 🧠 KNN-based Face Classifier (retrainable anytime)
- 🗂️ CSV-based attendance logging with date-wise records
- 🔔 Beep sound for successful recognition
- 🌐 Web Interface using Flask
- 👤 Add new users with automatic model retraining

---

## 📁 Folder Structure

```

project/
│
├── Attendance/                  # Stores attendance CSV files
├── static/
│   ├── faces/                  # Stores registered user images
│   ├── test\_faces/            # (Optional) Test data for accuracy checking
│   └── face\_recognition\_model.pkl  # Trained KNN model
├── templates/
│   └── home.html               # Frontend HTML template
├── haarcascade\_frontalface\_default.xml  # Face detection model
├── app.py                      # Main Flask application
└── README.md                   # Project Documentation

````

---

## ⚙️ Requirements

- Python 3.x
- OpenCV
- Flask
- NumPy
- scikit-learn
- pandas
- joblib

Install all dependencies:
```bash
pip install opencv-python flask numpy scikit-learn pandas joblib
````

> 🔔 **Note**: For Windows, `winsound` is used for beep notifications. If you're on Linux/Mac, replace it with an equivalent.

---

## 🧪 How It Works

1. **Register New User**

   * Go to `/add` route via the web app.
   * Enter name and ID → 50 images are captured via webcam.
   * Model is automatically retrained.

2. **Start Attendance**

   * Click on "Take Attendance".
   * Recognizes faces in real-time.
   * Plays beep sound and logs attendance.

3. **Attendance Logs**

   * Stored as `Attendance/Attendance-DD_MM_YY.csv`
   * Format: `Name, Roll, Time`

4. **Accuracy Checking**

   * Automatically prints model accuracy during startup if `static/test_faces/` is provided.

---

## 🖥️ Running the Project

```bash
python app.py
```

Then open:
👉 [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser

---

## 📈 Model Used

* Face images are resized to `50x50` pixels and flattened.
* KNN (K-Nearest Neighbors) is used for classification.
* Model saved as `face_recognition_model.pkl` using `joblib`.

---

## 🔒 Limitations

* Basic KNN model; may not perform well under varied lighting or with occlusions.
* No deep learning used — not as accurate as DNN-based systems.
* Designed for small-scale/local usage.

---

## 📌 To-Do / Future Improvements

* Add face recognition using deep learning (e.g., FaceNet or Dlib).
* Integrate database (e.g., SQLite/MySQL) instead of CSV.
* Add admin panel to manage attendance records.
* Deploy to cloud (Heroku, AWS, etc.)

---

## 🧑‍💻 Author

**Chandan Kumar**
GitHub: [@mgchandan0510](https://github.com/mgchandan0510)

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

```

---

Let me know if you want:
- A `home.html` template
- A GitHub action to auto-deploy
- Dockerfile or installation script

I can also generate a PDF version of this `README` if needed.
```
