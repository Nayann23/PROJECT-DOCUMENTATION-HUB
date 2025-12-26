# **🧠 Neurovia — High-Fidelity Brain Tumor Intelligence Console**

> **Neurovia is a production-styled, AI-powered diagnostic simulation system designed to demonstrate how deep learning–based medical imaging models can be exposed through a disciplined, system-oriented interface. The platform emphasizes **intentional system design**, **transparent inference**, and **user trust**, rather than raw model novelty.**

> **This project is architected as an **internal diagnostic intelligence console**, reflecting how experimental medical AI tools are typically explored, validated, and monitored inside applied research or early-stage HealthTech environments.**

---

> [!TIP]
> **In a hurry?** For a high-level overview of the hybrid security architecture, tech stack, and key detection layers, please refer to the **[Executive Summary (README.md)](./README.md)**.

---

## **📌 System Context Note**

> **Neurovia is not presented as a dataset-centric experiment.**

> **Instead of centering the system around dataset descriptions, this project is framed around **system behavior, inference flow, and interaction discipline**, acknowledging that in real-world ML systems, datasets are inputs to a broader operational pipeline rather than the product itself.**

#### **The trained CNN model is distributed in TensorFlow Lite (TFLite) format, emphasizing:**

- **Lightweight inference**

- **Edge-style deployment constraints**

- **Deterministic runtime behavior**

> **The system is designed to be **model-agnostic at the interface level**, allowing future upgrades without reworking the frontend or interaction logic.**

---

## **🧩 Overview**

> **Neurovia accepts MRI brain scan images and performs binary classification to determine whether a tumor is detected.** 

#### **The prediction result is delivered through a high-fidelity diagnostic interface that simulates:**

- **Controlled medical workflows**

- **Visual inference staging**

- **Confidence signaling**

- **System state awareness**

- **Responsible usage disclaimers**

> **Rather than presenting results as a simple label, Neurovia wraps inference inside a **diagnostic narrative**, reinforcing interpretability, restraint, and context.**

---

## **🎯 Design Intent & Project Philosophy**

> **In applied data science and machine learning, many projects often converge on the same datasets, models, and evaluation metrics.**  

> **While model performance remains important, real-world impact depends equally on how insights are communicated, explored, and trusted**.

> **The deliberate focus on a **polished, system-level UI** in this project was intentional.**

> **Beyond model accuracy, this project was an opportunity to go beyond standard implementations and invest additional effort into **presentation, interaction, and system completeness** — areas that are frequently underrepresented in academic or tutorial-style projects.**

### **The design choices were made to:**

> **Reflect how ML insights are consumed inside real organizations through dashboards and internal tools rather than notebooks.**

> **Demonstrate that applied data science involves **product thinking**, not only algorithm selection.**

> **Treat explainability and user trust as first-class concerns rather than optional additions.**

> **Elevate the project from a typical model demonstration to a complete, user-facing intelligence system.**

> **This philosophy aligns with the belief that **engineers who aim to grow beyond baseline implementations must be willing to invest extra effort where it meaningfully improves clarity, usability, and trust**, not only raw metrics.Production-facing ML systems succeed when interpretability, usability, and engineering discipline receive the same level of attention as accuracy.**

---

## **🧠 Core Capabilities**

#### **1. CNN-Based Medical Image Classification**

- **Binary tumor detection (Tumor / No Tumor)**

- **Pre-trained convolutional neural network**

- **Optimized inference via TFLite runtime**

- **Deterministic threshold-based decisioning**

---

#### **2. Structured Diagnostic Workflow**

- **Explicit “Run Diagnostics” action**

- **Staged scanning animations**

- **Clear separation between input, inference, and results**

- **Visual state transitions reinforcing system intelligence**

---

#### **3. High-Fidelity Visualization Layer**

- **Abstract standby state when idle**

- **Live feed visualization after image upload**

- **Simulated AI heatmap / localization overlay**

- **Color-governed status indicators (Safe vs Tumor)**

---

#### **4. Patient Metadata Association**

- **Optional name, age, and gender capture**

- **Metadata stored alongside prediction logs**

- **No identity enforcement or persistence beyond local logs**

---

#### **5. Diagnostic History & Reporting**

- **Timestamped prediction logs**

- **Exportable CSV-style logs**

- **Report inspection modal**

- **Individual record deletion**

- **Full history purge controls**

---

#### **6. Sample Image Injection**

- **Random sample MRI fetching**

- **Frontend-driven file injection**

- **Enables demonstration without manual uploads**

---

## **🧠 Model & Architecture Context**

#### **Model Characteristics**

- **Convolutional Neural Network (CNN)**

- **Exported to TensorFlow Lite format**

- **Single-image inference**

- **Float32 input tensors**

- **Binary sigmoid output**

---

#### **Architectural Decisions**

> **Why TFLite?**

- **Reduced memory footprint**

- **Faster cold-start inference**

- **Alignment with edge / constrained environments**

- **Predictable runtime behavior**

---

#### **Infrastructure-Driven Model Runtime Decision**

> **The decision to deploy the model using TensorFlow Lite (TFLite) was intentional and driven by real deployment constraints rather than theoretical preference.**

> **During early deployment attempts on Render free-tier infrastructure (512 MB RAM), it was observed that importing the full TensorFlow runtime alone consumed 300 MB+ of memory, leaving insufficient headroom for application execution, image preprocessing, and Flask server stability. This resulted in frequent worker restarts and unreliable behavior.**

> **To address this, the trained CNN model was initially developed using standard TensorFlow / Keras, and then converted into an optimized TensorFlow Lite artifact for inference-time usage.**

#### **This approach preserved:**

##### **Model accuracy**

- **Deterministic inference behavior**

- **Compatibility with existing preprocessing pipelines**

##### **While significantly reducing:**

- **Runtime memory footprint**

- **Cold-start latency**

- **Infrastructure instability on constrained environments**

> **This design choice reflects a system-level engineering mindset where deployment feasibility and operational reliability are treated as first-class concerns, rather than afterthoughts.**

---

#### **Why threshold-based classification?**

- **Deterministic decision boundaries**

- **Clear confidence signaling**

- **Reduced ambiguity in UI interpretation**

---

**Why no Grad-CAM or true heatmaps?**
- **Avoids misleading clinical interpretations**

- **Prevents false explainability claims**

- **Keeps visualization explicitly simulated and labeled as such**

> **The system intentionally avoids overstating model interpretability.**

---

## **🔒 Privacy & Data Handling**

> **Neurovia follows a privacy-minimal design approach.**

- **No external API calls**

- **No analytics trackers**

- **No cookies**

- **No user session persistence**

- **No cloud storage**

#### **All data handling is:**

- **Local**

- **File-based**

> **Patient metadata is optional and sanitized before logging to prevent delimiter injection or corruption.**

---

## **🛠 Tech Stack**

#### **Backend**

- **Python**
- **Flask**
- **NumPy**
- **OpenCV**
- **TensorFlow Lite Runtime**
- **Werkzeug (secure file handling)**

---

#### **Frontend**

- **HTML5**
- **Tailwind CSS**
- **Vanilla JavaScript**
- **Lucide Icons**
- **Custom animation & state logic**

---

#### **Model Runtime**

- **TensorFlow Lite (.tflite)**
- **CPU-based inference**

---

#### **Deployment**

- **Local / container-friendly**

- **No platform-specific coupling**

- **Ready for Docker or VPS environments**

---

## 📂 Project Structure


---

## **⚙️ Inference Flow**

- **User opens Neurovia console**

- **Optional patient metadata is entered**

- **MRI image is uploaded or fetched via sample loader**

- **Image is preprocessed:**
   - Read via OpenCV
   - RGB conversion
   - Resized to 128×128
   - Normalized to [0,1]
   - Expanded to batch tensor

- **Tensor passed to TFLite interpreter**

- **Model inference executed**

- **Sigmoid output interpreted**

- **Threshold applied (0.5)**

- **Result classified:**
   - Tumor Detected
   - No Tumor Detected

- **Confidence calculated**

- **Result logged locally**

- **UI transitions to diagnostic visualization**

- **Optional heatmap simulation rendered**

- **User may inspect reports or export logs**

> **Each step is intentionally separated to mirror real diagnostic pipelines.**

---

## **⚠️ Limitations**

- **Binary classification only**

- **No multi-class tumor typing**

- **No real medical explainability**

- **Visualization is illustrative, not clinical**

- **Dataset bias may exist**

- **Model accuracy depends on training data quality**

- **Not suitable for medical diagnosis**

- **No regulatory compliance (FDA / CE)**

> **All limitations are explicitly acknowledged by design.**

---

## **🖥 System Interface Preview**

> **Neurovia is designed as a diagnostic intelligence console, not a consumer health app.**

#### **Interface characteristics:**

- **Dark-mode, low-distraction layout**

- **Glassmorphism panels**

- **Controlled animation pacing**

- **Clear visual hierarchy**

- **System state indicators**

- **Persistent disclaimers**

#### **The UI reinforces the idea that:**

> **The system assists exploration — it does not replace professionals.**

---


## **Source Availiability**

> **The core source implementation for this project is maintained in a private repository.**

> **The code can be shared upon request for review or evaluation purposes.**

---
## **🏁 Conclusion**

> **Neurovia demonstrates how a deep learning model can be elevated into a credible, responsible, and system-aware diagnostic interface through disciplined engineering and intentional UX design.**

#### **Rather than chasing novelty, the project emphasizes:**

- **Trust**

- **Clarity**

- **Transparency**

- **Restraint**

- **Repeatability**

> **These qualities are essential in real-world ML systems—especially in healthcare.**

---

## **📜 License**

This project is open-source and licensed under the [Apache License 2.0](../LICENSE).
See the LICENSE file for full details.

---


## **👤 Author: Nayan Darokar**

#### **Aspiring Data Scientist — Intelligent Interfaces & ML Systems Engineering**

---

> **Connect With Me Here:**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayan-darokar-468a85294/) 
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reachout.nayan@gmail.com)


