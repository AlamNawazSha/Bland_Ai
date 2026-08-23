# SpatialVision AI — Monocular Object Distance & AI Collision Avoidance Engine

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![TensorFlow.js](https://img.shields.io/badge/AI-TensorFlow.js%20%2F%20COCO--SSD-FF6F00?logo=tensorflow)
![JavaScript](https://img.shields.io/badge/Frontend-Vanilla%20JS%20%2F%20HTML5-F7DF1E?logo=javascript)
![Web Speech API](https://img.shields.io/badge/Audio-Web%20Speech%20API-00f2fe)

A high-performance, mobile-first Web Application for real-time monocular distance estimation, step counting, active **AI Collision Avoidance Guidance**, mobile haptic vibration alerts, and voice directional steering assistance using browser computer vision.

---

## 🌟 Key Features

- **Real-Time AI Object Detection**: Powered by TensorFlow.js and COCO-SSD (`lite_mobilenet_v2`).
- **Mobile-First Tap-to-Start Guidance**: Solves iOS Safari & Android Chrome autoplay/audio gesture restrictions.
- **Active AI Obstacle & Collision Avoidance**:
  - Classifies screen view into 3 walking corridors (**LEFT**, **CENTER**, **RIGHT**).
  - Detects imminent collision risks in the user's direct walking path (`< 1.25 meters` / `<= 2 steps`).
  - Gives urgent audio alerts (*"WARNING! Chair 1 step straight ahead! Steer right!"*) with automatic priority audio interrupts.
  - Recommends actionable steering directions (`⬅ STEER LEFT`, `STEER RIGHT ➔`, `🛑 STOP`).
- **Mobile Haptic Vibration Feedback**: Distinct vibration patterns for Danger (multi-pulse pattern), Caution, and UI feedback.
- **Visual Danger HUD Alerts**: Full-screen edge flashing alert borders (Red for Danger, Amber for Caution, Emerald Green for Clear Path).
- **Monocular Pinhole Distance Estimation**: Calculates physical real-world object distances without depth cameras or LIDAR hardware.
- **Human Step Estimation**: Converts physical distances directly to estimated walking steps based on configurable stride lengths.
- **Optical Focal Length Calibration Wizard**: Built-in interactive wizard to calibrate any smartphone camera sensor optics.

---

## 📐 Distance Calculation & Collision Math

$$\text{Distance (meters)} = \frac{\text{Real World Object Size (m)} \times \text{Focal Length (px)}}{\text{Bounding Box Bounding Dimension (px)}}$$

$$\text{Estimated Steps} = \text{Round}\left(\frac{\text{Distance (m)}}{\text{Stride Length (m)}}\right)$$

---

## 📱 Mobile Setup & HTTPS Requirement

Modern mobile browsers (iOS Safari & Chrome Android) require **HTTPS** (or `localhost`) to grant camera access (`getUserMedia`).

### Recommended Hosting Options (Zero-Config):
1. **GitHub Pages**: Push code to a GitHub repository, enable GitHub Pages in repo settings.
2. **Vercel / Netlify**: Drag & drop `index.html` or connect repo for instant HTTPS link.
3. **Local Network Testing**: Run a local SSL tunnel (e.g. `npx localtunnel --port 8000` or `ngrok http 8000`).

---

## 🛠️ Local Usage

Simply open `index.html` in any web browser with camera permissions enabled. Tap **"START GUIDANCE SYSTEM"** on the splash screen to unlock camera stream, speech synthesis, and haptics.

---

## 📄 License
MIT License. Created by Alam Nawaz Sha.
