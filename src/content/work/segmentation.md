---
title: Segmentation
publishDate: 2019-12-01 00:00:00
img: /assets/segmentation/texture8.png
img_alt: Segmented texture image
description: |
  Texture image segmentation using K-means and Mean-Shift algorithms. This C++/OpenCV project was developed at INP-ENSEEIHT, with evaluation metrics and visualizations.
tags:
  - Image Segmentation
  - C++
  - OpenCV
---

### Context

This project focused on **segmenting texture images** using the **K-means** and **Mean-Shift** clustering algorithms. The aim was to split each image into meaningful regions — either into a **foreground/background** binary segmentation or into **N semantic classes** — and to evaluate the results against ground-truth segmentation masks.

It was developed in **C** using **OpenCV**, as part of a computer vision lab at INP-ENSEEIHT.

---

### Tasks and Contributions

- Implemented both **K-means** and **Mean-Shift** segmentation in C using OpenCV.
- Developed a pipeline to load texture datasets, apply segmentation, and display results.
- Created performance metrics to compare segmentation outputs with reference masks.
- Built visualization tools to render segmentation maps side-by-side with input and ground truth.

---

### Results

- Demonstrated successful segmentation across a variety of texture images.
- Highlighted strengths and limitations of both methods:
  - **K-means** is fast and simple but requires predefined number of clusters.
  - **Mean-Shift** is adaptive but computationally more expensive.
- Validated segmentations through quantitative metrics and visual inspection.

---

### Skills Gained

- C++ / OpenCV programming for image processing.
- Understanding and implementation of unsupervised clustering algorithms.
- Development of evaluation tools for segmentation accuracy.
- Comparative analysis of segmentation techniques.

---

### Tools & Technologies

- C++
- OpenCV
- K-means clustering
- Mean-Shift algorithm

