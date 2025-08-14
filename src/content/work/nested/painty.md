---
title: Inbetweening for Painterly Animation
publishDate: 2020-03-04 00:00:00
img: /assets/painty/Interface.PNG
img_alt: User Interface of Painty
description: |
  A research-driven pipeline for generating intermediate frames in hand-painted 2D animation.
tags:
  - Animation
  - C++
  - Research
---

### Context

During my 2-month internship in the STORM research team at IRIT (Toulouse), I worked on **Painty**, a C++ application for generating **intermediate frames (inbetweens)** in hand-painted 2D animations. The goal was to preserve the visual style of artists while automating the creation of intermediate strokes between two keyframes, based on a motion field (from 3D renders or sketches).

This work builds on the research paper _“Automatic Inbetweening for Stroke-Based Painterly Animation”_ (Barroso et al., 2024), and is part of a larger ANR-funded project.

---

### Tasks and Contributions

#### 1. Environment Setup
- Compiled and configured [Radium Engine](https://github.com/STORM-IRIT/Radium-Engine) & Painty under Windows (Visual Studio, Ninja, CMake).
- Solved dependency issues (GLFW, Qt, DLLs, headless builds).
- Integrated Blender 4.5 to export motion vector files (.exr).

#### 2. Core Development
- **Refactored the pipeline** to unify frame generation logic.
- **Improved UI (Qt):** introduced dynamic propagation modes (rigid, advected, blended, optimized).
- **Created a new optimizer** bypassing Bézier curves, increasing stability and speed.

#### 3. Algorithmic Enhancements
- Implemented a **genetic algorithm** for candidate stroke selection (vs greedy).
- Measured and compared performance: up to 10× faster on complex scenes.

#### 4. Testing & Visualization
- Validated Blender exports; built full pipelines for EXR → .png/.mkv video generation.
- Documented usage and prepared test scenes (fluid, rigid body, noise).
- Automated checks to discard invalid strokes/frames during rendering.

---

### Results

- The tool is now **more robust, modular, and user-configurable**.
- Rendering pipeline was stabilized, with **significantly improved frame speed generation**.
- Artists can now easily switch propagation modes and visualize stroke behavior.
- Final deliverables included test videos, reusable Blender scenes, and code improvements.

<p align="center">
  <img src="/assets/painty/walk_blender_short.gif" alt="Demo 1" width="30%">
  <img src="/assets/painty/walk_motion_short.gif" alt="Demo 2" width="30%">
  <img src="/assets/painty/walk_painty.gif" alt="Demo 3" width="30%">
</p>


---

### Skills Gained

- C++ / Qt / OpenGL / Visual Studio / Git 
- Blender 4.5
- Real-time graphics, procedural animation, algorithm design

---

_This internship strengthened my skills at the crossroads of graphics, animation, and software engineering, and confirmed my interest in image processing and stylized rendering for creative applications._

---
### Example Use Case: Artistic Short Film

The software **Painty** was used in the production of an artistic short film. This demonstrates its creative potential and validates the research and development work done on the inbetweening engine.

#####  Film: *Indigestion* (2022)
[Watch here](https://www.youtube.com/watch?v=AO4SS77w4Ig) 

#####  Film: *LOIN* (2024)
[Watch here](https://www.youtube.com/watch?v=nKbf4W2dg8I)

> _This use case highlights how Painty can support real-world artistic production, combining digital tools with painterly aesthetics._

