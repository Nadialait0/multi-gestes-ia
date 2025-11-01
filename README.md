# 🤖 AI Webcam Recognition — Hands + Face Enhanced

A real-time **AI-powered web application** that detects **hand gestures** and **facial expressions** through your webcam.  
Built using **Google MediaPipe**, it showcases how modern browser-based AI can interpret human movement and emotion — directly on the client side.

---

## 🌟 Features

- 🖐️ Detects multiple **hand gestures** (👋 wave, 👍 thumbs up, ✌️ victory)  
- 😴 Recognizes **facial states** (eyes closed, mouth open)  
- 🎨 Reacts with dynamic background color and emoji  
- 🔊 Optional sound feedback for detected gestures  
- 🧠 All AI processing is **local** — no data is sent to any server  

---

## 🧠 Powered by Artificial Intelligence

This project uses **MediaPipe’s pre-trained machine learning models** for human motion and face analysis.

### 🤲 Hand Recognition (MediaPipe Hands)
- Detects **21 landmarks per hand** in real time  
- Custom gesture recognition logic based on landmark distances  
- Adjustable **sensitivity slider** for fine-tuning detection  

### 😊 Face Recognition (MediaPipe FaceMesh)
- Analyzes **468 facial landmarks**
- Detects small changes in eyelid and lip distance to identify:
  - 😴 Closed eyes
  - 😮 Open mouth  

### ⚡ Real-Time AI Flow
```plaintext
Webcam → CameraUtils → MediaPipe Models (Hands + FaceMesh)
      ↓
Landmarks → AI Analysis → Gesture/Expression Recognition → UI Reaction
💻 User Interface
The web app provides a simple and interactive layout:

Section	Description
Viewer	Live webcam feed + AI landmark overlay
Control Panel	Start/Stop buttons, sensitivity control, sound toggle

✨ Visual Feedbacks
Gesture	Meaning	UI Effect
👋	Wave	Soft green gradient
👍	Thumbs up	Deep green gradient
✌️	Victory	Purple gradient
😴	Eyes closed	Midnight blue gradient
😮	Mouth open	Deep red gradient

⚙️ Parameters
Setting	Element	Function
Sensitivity	#sensitivity	Adjusts AI detection tolerance
Sound	#enableSound	Plays a sound when gesture detected
Start / Stop	#startBtn, #stopBtn	Controls camera and AI models

🧱 Code Structure
php-template
Copier le code
ai-webcam-recognition.html
│
├── <style>      → Dark, responsive UI with gradient themes
├── <video>      → Webcam feed
├── <canvas>     → AI overlay for landmarks
├── <script>     → Core AI logic
│    ├── setupHands() / setupFace() → Initialize AI models
│    ├── detectGesture() / detectFaceStates() → Interpret AI output
│    ├── react() → Visual + audio reactions
│    └── startCamera() → Real-time processing loop
🔒 Privacy & Data Ethics
🧩 100% local inference — all video processing stays on your device.

🚫 No images, videos, or biometric data are uploaded or stored.

💡 Runs entirely in your browser, even offline once models are loaded.

🧭 Future Improvements
✋ Add more gesture types (🤙, 🤟, ✋)

🧩 Integrate TensorFlow.js for advanced custom models

🧪 Train a personalized gesture recognition model

⚙️ Implement adaptive sensitivity or calibration modes

👩‍💻 Author & Credits
Developer: Nadia
AI Framework: MediaPipe by Google Research
Version: 3.0 — Multi-Gesture + Face Enhanced
License: MIT

🖼️ Preview
"AI meets human interaction — all in your browser."


🪄 How to Run
Clone or download the repository

Open ai-webcam-recognition.html in your browser

Allow webcam access and click Start

Move your hand or face — and watch the AI react ✨