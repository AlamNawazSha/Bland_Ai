# SpatialVision AI — Monocular Object Distance & Voice Estimator

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![TensorFlow.js](https://img.shields.io/badge/AI-TensorFlow.js%20%2F%20COCO--SSD-FF6F00?logo=tensorflow)
![JavaScript](https://img.shields.io/badge/Frontend-Vanilla%20JS%20%2F%20HTML5-F7DF1E?logo=javascript)
![Web Speech API](https://img.shields.io/badge/Audio-Web%20Speech%20API-00f2fe)

A high-performance, mobile-first Web Application for real-time monocular distance estimation, step counting, directional spatial awareness, and audio voice announcements using computer vision in the browser.

---

## 🌟 Key Features

- **Real-Time AI Object Detection**: Powered by TensorFlow.js and COCO-SSD (`lite_mobilenet_v2`).
- **Monocular Pinhole Distance Estimation**: Calculates physical real-world object distances without needing depth cameras or LIDAR hardware.
- **Human Step Estimation**: Converts physical distances directly to estimated walking steps based on configurable stride lengths.
- **Directional Spatial Awareness**: Classifies object orientation as `LEFT`, `RIGHT`, or `STRAIGHT AHEAD`.
- **Audio Voice Announcements**: Real-time Text-To-Speech guidance (e.g. *"Person detected, 3 steps, 2.2 meters on your left."*) with configurable cooldown interval.
- **Optical Focal Length Calibration**: Integrated wizard to calibrate any smartphone or webcam sensor optics.
- **Responsive HUD Design**: Dark mode glassmorphism UI with animated corner reticles, metric cards, and camera controls.

---

## 📐 Distance Calculation Formula

$$\text{Distance (meters)} = \frac{\text{Real World Object Size (m)} \times \text{Focal Length (px)}}{\text{Bounding Box Bounding Dimension (px)}}$$

$$\text{Estimated Steps} = \text{Round}\left(\frac{\text{Distance (m)}}{\text{Stride Length (m)}}\right)$$

---

## 🚀 Live Demo & Deployment

This project is built as a single-file static web application (`index.html`) with zero backend dependencies. It can be hosted directly via:
- **GitHub Pages**
- **Vercel**
- **Netlify**

---

## 🛠️ Local Usage

Simply open `index.html` in any modern Web Browser (Chrome, Edge, Safari, Firefox) with camera permissions enabled.

---

## 📄 License
MIT License. Created by Alam Nawaz Sha.
