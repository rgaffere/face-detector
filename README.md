# 👁️ Embedded Face Detection System (EFDS)

A resource-constrained face detection system built entirely from scratch for embedded hardware using the **Viola–Jones algorithm**, developed in **C++** without OpenCV or external libraries.

> ⚠️ Status: **Incomplete – ran out of time before full system integration**
> Core components were implemented and validated individually, but full integration and end-to-end face detection on the Raspberry Pi was not achieved before the deadline.

---

## 🎯 Project Objective

Design and implement an **Embedded Face Detection System (EFDS)** that processes grayscale images in real time, classifies sub-windows using a cascade of boosted classifiers, and outputs true/false detections — all within the memory and processing constraints of a Raspberry Pi.

---

## 🛠️ System Overview

- **Platform**: Raspberry Pi (cross-compiled via UMD's ENEE408M servers)
- **Detection Algorithm**: Viola–Jones cascade with configurable classifiers
- **Architecture**: Dataflow-based using Welter-C++
- **Training**: Offline training module outputs configuration files for classifiers
- **Input**: Indexed grayscale image sub-windows

---

## 🧩 Components Built

✅ Classifier actor structure (5-mode state machine: configure, read, classify, true, false)  
✅ Token types for image sub-windows and metadata  
✅ Custom Haar feature pipeline  
✅ Boosting-based strong classifier training (offline module)  
✅ Modular design for tuning number of classifiers/features  
✅ Bash scripts to automate training/testing

---

## 🚧 Why It Wasn’t Completed

While major parts of the system were implemented, the full pipeline could not be integrated before the course deadline due to:
- Time constraints with final training and testing
- Limited availability for debugging embedded execution
- Complexity of integrating multiple classifiers with memory-safe runtime

---

## 📈 What We Learned

- How to implement computer vision pipelines without external libraries  
- Trade-offs between detection rate, false positives, and latency  
- The challenges of real-time embedded systems development  
- Structuring code for portability, configurability, and pipeline design

---

## 📚 References

- Viola & Jones, *Robust Real-Time Face Detection*, IJCV 2004  
- [ENEE 408M Project Specification](project-specification-v-031925-1803.pdf)

---

Course: **ENEE 408M – Embedded Systems Projects**  
University of Maryland – Spring 2025  
Prof. Shuvra S. Bhattacharyya

---

> This project laid the groundwork for a working EFDS, and though it wasn’t completed, it taught us a lot about embedded CV pipelines, structured code design, and system-level debugging under pressure.
