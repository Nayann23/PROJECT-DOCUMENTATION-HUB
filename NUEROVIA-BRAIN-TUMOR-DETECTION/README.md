# **🧠 Neurovia — High-Fidelity Brain Tumor Intelligence Console**

> **Neurovia is a production-styled diagnostic simulation system designed to demonstrate how deep learning-based medical imaging models can be exposed through a disciplined, system-oriented interface. It utilizes an optimized TFLite CNN engine to bridge the gap between computer vision and clinical trust.**

---

## **Infrastructure-Driven Runtime Choice**

> **TensorFlow Lite (TFLite) was chosen intentionally due to real deployment constraints. On Render’s free tier (512 MB RAM), importing the full TensorFlow runtime alone consumed over 300 MB, causing frequent worker restarts and instability.**

> **To ensure reliable execution, the CNN model was trained using TensorFlow/Keras and then converted into an optimized TFLite artifact for inference. This preserved model behavior while significantly reducing memory usage, startup overhead, and infrastructure-related failures.**

> **This decision reflects a system-level focus on deployment feasibility and operational stability, not just model development.**

---

## **🎯 Objective**

> **To demonstrate a responsible HealthTech workflow that prioritizes trust-based UX, intentional system constraints, and lightweight edge deployment by wrapping a CNN-ResNet backbone in a professional diagnostic narrative.**

---

## **🛠 Tech Stack**

-  **ML Engine: CNN-ResNet Architecture exported to TensorFlow Lite for high-efficiency, deterministic binary classification.**

- **Intelligent UX: Visual Inference Staging with simulated heatmap overlays and color-governed status signaling (Safe vs. Tumor).**

- **Backend: Flask (Python) managing secure image preprocessing, tensor reshaping, and TFLite interpreter orchestration.**

- **Frontend: Vanilla JS and TailwindCSS featuring a Medical Console aesthetic with glassmorphism panels and staged transitions.**

- **DevOps: Containerized via Docker for cross-platform reliability and streamlined environment isolation.**

---

## **🚀 Implementation Highlights**

> **Trust-Oriented Design: Implements a mandatory "Usage Disclaimer" and explicit "I Understand" gateway, mirroring the regulatory and ethical discipline required in real-world medical AI platforms.**

> **Operational Visibility: Features a simulated Diagnostic Console with system-state indicators ("System Ready"), inference timers, and real-time confidence signaling to eliminate "black-box" ambiguity.**

> **Data Governance: Includes a local Diagnostic History & Reporting system with CSV export capabilities, allowing for the tracking and auditing of prediction logs and patient metadata.**

---

## **📖 Comprehensive Documentation**

#### **For a deep dive into the TFLite optimization, CNN architecture, and the ethical framework of the design:**

[👉 Read Technical Deep Dive](./Technical_Deep_Dive.md)

---

## **🖥 System Interface Preview**

Neurovia Diagnostic Intelligence Console

![System UI](./Assets/UI.png)

---

## **👤 Author: Nayan Darokar**

#### **Aspiring Data Scientist — Intelligent Interfaces & ML Systems Engineering**

---

> **Connect With Me Here:**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayan-darokar-468a85294/) 
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reachout.nayan@gmail.com)

