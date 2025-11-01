# 🤖 AI Webcam Recognition — Hands + Face Enhanced

A real-time **AI-powered web application** that detects **hand gestures** and **facial expressions** directly from your webcam.  
Built using **Google MediaPipe**, it showcases how modern browser-based AI can interpret human movement and emotion — entirely **on the client side**.

---

## 🌟 Features

- 🖐️ Detects multiple **hand gestures** (👋 wave, 👍 thumbs up, ✌️ victory)  
- 😴 Recognizes **facial states** (eyes closed, mouth open)  
- 🎨 Reacts with **dynamic background color** and emoji feedback  
- 🔊 Optional **sound feedback** for detected gestures  
- 🧠 All AI processing is **local** — no data is sent to any server  

---

## 🧠 Powered by Artificial Intelligence

This project uses **MediaPipe’s pre-trained ML models** for **hand** and **face** analysis.

### ✋ Hand Recognition (MediaPipe Hands)
- Detects **21 landmarks per hand** in real time  
- Includes **custom gesture logic** based on landmark distances  
- Adjustable **sensitivity slider** for detection fine-tuning  

### 🙂 Face Recognition (MediaPipe FaceMesh)
- Analyzes **468 facial landmarks**  
- Detects micro-movements to identify:
  - 😴 Closed eyes  
  - 😮 Open mouth  

---

## ⚡ Real-Time AI Flow

```plaintext
Webcam → CameraUtils → MediaPipe Models (Hands + FaceMesh)
      ↓
Landmarks → AI Analysis → Gesture/Expression Recognition → UI Reaction
💻 User Interface
Section	Description
Viewer	Live webcam feed + AI landmark overlay
Control Panel	Start/Stop buttons, sensitivity control, sound toggle

✨ Visual Feedback
Gesture	Meaning	UI Effect
👋	Wave	Soft green gradient
👍	Thumbs up	Deep green gradient
✌️	Victory	Purple gradient
😴	Eyes closed	Midnight blue gradient
😮	Mouth open	Deep red gradient

⚙️ Parameters
Setting	Element	Function
Sensitivity	#sensitivity	Adjusts AI detection tolerance
Sound	#enableSound	Plays sound when gesture detected
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
🧩 100% local inference — all processing stays on your device

🚫 No data collected or stored (no images, videos, or biometric info)

💡 Works entirely in your browser — even offline after model loading

🧭 Future Improvements
✋ Add more gesture types (🤙, 🤟, ✋)

🧩 Integrate TensorFlow.js for custom AI models

🧪 Train personalized gesture recognition models

⚙️ Implement adaptive sensitivity calibration

👩‍💻 Author & Credits
Developer: Nadia


🖼️ Preview
“AI meets human interaction — all in your browser.”


Allow webcam access and click Start

Move your hand or face — and watch the AI react ✨
