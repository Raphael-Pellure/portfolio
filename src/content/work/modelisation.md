---
title: Medial Axis Extraction and 3D Meshing
publishDate: 2025-04-12
img: /assets/stock-1.jpg
img_alt: MAT pipeline steps
description: |
  MATLAB project for 3D shape reconstruction from multi-view images using superpixel segmentation, skeleton extraction, and surface meshing.
tags:
  - 3D Reconstruction
  - MATLAB
  - Image Processing
---

### Context

This project was developed as part of the **2nd-year course “Image, Modeling and Rendering”** at **INP-ENSEEIHT**, in collaboration with **Gabin Nobelet**. The objective was to reconstruct the **3D shape** of an object from a series of **multi-view 2D images** by extracting its **medial axis** and computing a **surface mesh**.

The data consisted of 37 images of a dinosaur on a blue background, along with **camera calibration matrices** and **2D point correspondences**.

---

### Tasks and Contributions

#### 1. Image Segmentation
- Implemented **SLIC superpixel segmentation** in MATLAB with configurable parameters.
- Applied **binary classification** (object/background) using color or shape heuristics.

#### 2. Skeleton Extraction
- Detected shape boundaries with `bwtraceboundary`.
- Computed **Voronoi diagrams** and **Delaunay triangulations**.
- Extracted and filtered **internal medial axis points** (skeleton) of the object.

#### 3. 3D Point Cloud Reconstruction
- Used calibration data to project 2D matched points into a 3D space.
- Built a **Delaunay tetrahedralization** of the reconstructed point cloud.
- Filtered tetrahedra using **multi-view binary masks** to retain only those inside the object.

#### 4. Surface Mesh Generation
- Extracted surface triangle faces from the valid tetrahedra.
- Generated and visualized a consistent **3D surface mesh** of the dinosaur.

---

### Results

- Accurate **medial skeleton** and **surface mesh** reconstruction from raw 2D images.
- End-to-end MATLAB pipeline demonstrating segmentation, geometry, and 3D modeling.
- Clean filtering of invalid tetrahedra using camera projections and object masks.

---

### Tools & Technologies

- **MATLAB**
- Superpixel Segmentation (SLIC)
- Binary image classification
- Voronoi and Delaunay geometry
- 3D projection and mesh generation

---

### Skills Gained

- Superpixel segmentation and binary classification
- Skeleton extraction using Voronoi/Delaunay structures
- 3D reconstruction from calibrated images
- Mesh generation and geometric filtering in MATLAB

---

_This project deepened my understanding of geometric image analysis and 3D modeling from multi-view data, and improved my ability to design structured scientific code in MATLAB._
