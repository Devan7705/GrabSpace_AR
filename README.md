# 🤏 GrabSpace AR — 3D Hand-Tracked Object Interaction Lens

![Platform](https://img.shields.io/badge/platform-Snapchat-FFFC00?logo=snapchat&logoColor=black)
![Engine](https://img.shields.io/badge/Lens%20Studio-5.23.0-blue)
![Client](https://img.shields.io/badge/Client-Mobile%20%7C%20CameraKit-orange)
![Status](https://img.shields.io/badge/status-in%20development-yellow)

## 📖 Overview

**GrabSpace AR** is a Snapchat Lens built in **Lens Studio** that uses real-time **3D hand tracking** to let users interact with a virtual object in augmented reality. By pinching or closing their hand near a rendered 3D shape, the user can **grab it and move it freely in space**, driven entirely by hand-landmark tracking rather than touch input.

## ✋ Core Feature

- **Hand Tracking → Grab → Move**
  The lens tracks the user's hand in the camera feed and maps hand-landmark positions to 3D space. When the hand performs a grab gesture near the target shape, the shape attaches to the hand's tracked position and follows its movement until released.

## 🧾 Project Metadata

Extracted directly from `Default.esproj`:

| Property | Value |
|---|---|
| Lens Name | Hand Tracking |
| Target Platform | Snapchat |
| Lens Studio Version | 5.23.0 (build 26072806) |
| Client Compatibility | Mobile, CameraKit |
| Applicable Contexts | Live Camera, Reply Camera, Video Chat |
| Camera Facing | Front & Back |
| Activation Camera | Front |
| Template | Default |

## 🗂️ Project Structure

```
GrabSpace-AR/
├── Default.esproj      # Lens Studio project file (scene, metadata, platform config)
├── Assets/             # 3D shape asset(s), materials, textures
├── Scripts/            # Hand-tracking + grab/move interaction logic
└── README.md           # Project documentation
```
> Note: only `Default.esproj` was available at the time of writing; the `Assets/` and `Scripts/` folders above reflect the expected structure as the project is built out.

## 🛠️ Tech Stack

- **Lens Studio 5.23** — AR authoring environment
- **Hand Tracking module** — built-in Lens Studio hand-tracking component for landmark detection
- **JavaScript/TypeScript (Lens Scripting)** — grab-detection and object-follow logic
- **Snapchat Camera Kit** — deployment target for cross-app/mobile compatibility

## 🚀 Getting Started

1. Open `Default.esproj` in **Lens Studio 5.23+**.
2. Ensure the **Hand Tracking** template/module is enabled in the scene.
3. Preview using the Lens Studio simulator or push to a paired Snapchat mobile device for live testing.
4. Perform a pinch/grab gesture near the 3D shape to pick it up, and move your hand to reposition it in the scene.

## 📌 Roadmap Ideas

- [ ] Add release/drop physics when the grab gesture ends
- [ ] Support multiple grabbable shapes
- [ ] Add visual/haptic feedback on successful grab
- [ ] Two-hand scale/rotate gestures

---
*This README was generated based on the project's `Default.esproj` metadata.*
