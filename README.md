# ⚽ Football Analysis AI Backend

A powerful, AI-driven backend for analyzing football (soccer) matches. This system uses **YOLO object detection** and **K-Means clustering** to track players, identify teams based on jersey colors, and calculate possession percentages—all processed in real-time from uploaded videos.

---

## 🚀 Features

- **Object Detection**: Highly accurate tracking of players, referees, and the ball using YOLO.
- **Team Identification**: Automatic team classification using K-Means clustering to analyze jersey colors.
- **Possession Tracking**: Dynamic calculation of ball possession based on player-ball proximity.
- **Video Optimization**: Automated conversion to web-ready MP4 formats using FFmpeg.
- **SQLite Database**: Lightweight, zero-config data storage for processed videos and user records.

---

## 🛠 Tech Stack

- **Core**: Python 3.9+
- **Framework**: Flask
- **AI/CV**: Ultralytics (YOLO), OpenCV, Supervision
- **Database**: SQLite (via Flask-SQLAlchemy)
- **Video**: FFmpeg

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your machine:

1.  **Python 3.9+**: [Download here](https://www.python.org/downloads/)
2.  **FFmpeg**: Required for video processing and conversion.
    - **Mac (Homebrew)**: `brew install ffmpeg`
    - **Ubuntu/Debian**: `sudo apt install ffmpeg`
    - **Windows**: [Download here](https://ffmpeg.org/download.html)
3.  **Node.js & npm**: [Download here](https://nodejs.org/) (used to run the server script)

---

## 🛠 Installation

1.  **Clone the Repository** (if not already done):
    ```bash
    git clone https://github.com/HovSaintBrandon/football-analysis-backend--patched.git
    cd football-analysis-backend
    ```

2.  **Install Python Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Install Node Dependencies**:
    ```bash
    npm install
    ```

---

## 🏃 Running the Program

To start the backend server, simply run:

```bash
npm start
```

Your server will be running at `http://localhost:5000`.

---

## 📡 API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/register` | Register a new user with name, email, and password. |
| `POST` | `/login` | Authenticate user and receive credentials. |
| `POST` | `/process-video` | Upload a video and team colors for AI analysis. |
| `GET` | `/user-uploads/<user_id>` | List all processed videos for a specific user. |
| `DELETE` | `/delete-video/<video_id>` | Remove a processed video from the system. |

---

## ⚠️ Important Notes

> [!IMPORTANT]
> **YOLO Model**: Ensure the YOLO model file (`object.pt`) is present in the `models/` directory for the object detection to work.

> [!TIP]
> **Video Compatibility**: While the app handles several formats, uploading `.mp4` videos directly is recommended for the fastest processing speeds.

---

## 👨‍💻 Contributing

1. Fork the repo. 
2. Create your feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -m 'Add some NewFeature'`).
4. Push to the branch (`git push origin feature/NewFeature`).
5. Open a Pull Request.

---

*Powered by [Antigravity AI](https://github.com/HovSaintBrandon)*
