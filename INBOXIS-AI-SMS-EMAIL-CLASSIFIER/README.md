# **🚨 INBOXIS AI — Message Integrity Intelligence Console**

> **INBOXIS AI is a security-oriented message classification console designed to inspect, decode, and evaluate raw email and SMS streams using a production-styled ML engine and a high-fidelity interactive interface.**

> **Unlike traditional spam-filter demos, INBOXIS AI is architected to behave like an internal content-integrity system, mirroring how organizations monitor inbound communication, surface anomalies, and maintain user trust through transparency and system orchestration.**

---

## **Live Application**

**A fully deployed version of ***INBOXIS AI (v2.0)*** is available for interactive exploration.**

**Experience real-time spam detection, toxicity shielding, Bernoulli NB inference, and the full intelligence dashboard directly in your browser.**

[![🔗 Visit Live App](https://img.shields.io/badge/🔗%20Visit%20Live%20App-000000?style=for-the-badge&logo=safari&logoColor=white)](https://inboxis-ai.onrender.com)

---

## **Dataset Source:**

```bash
https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset

```

> **This project utilizes the SMS Spam Collection Dataset made available on Kaggle. Full credit goes to the original dataset creators for collecting and publishing this corpus of SMS messages labeled as spam or legitimate. The availability of this dataset enabled the training, evaluation, and demonstration of the Inboxis AI system presented in this project.**

---

## **📌 System Context Note**

> **INBOXIS AI operates entirely on client-side intelligence, local ML inference, and stream-level UI simulation.**

- **No external APIs.**

- **No cloud dependencies.**

- **No user data collection.**

> **The intent is to recreate a realistic inbox-classification environment while keeping the system private, portable, and deterministic.**


---

## **🧩 Overview**

### **INBOXIS AI classifies messages into:**

- **Spam**

- **Safe (Ham)**

- **Profanity-Flagged** 

### **The system integrates classical ML classification with a fully engineered console experience that emphasizes:**

- **Interpretability**

- **Stream realism**

- **Controlled behaviours**

- **User trust**

- **System observability**

> **Every interaction is intentionally crafted to feel like a **security subsystem**, not a casual ML demo.**

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

### **1. Email & SMS Classification Engine**

- **TF-IDF textual feature encoding**

- **Bernoulli Naive Bayes for interpretable classification**

- **Confidence scoring derived from probability distributions**

- **Automatic context detection (Email vs SMS)**

- **Visual behaviour tied directly to model output**

---

# ## **2. Profanity & Toxicity Simulation Layer**

> **To recreate real-world inbox disruptions, INBOXIS AI includes a ***controlled profanity-flagging*** pipeline:**

- **Random profanity message injections (30–40% probability)**

- **Red alert terminal sequence**

- **Toxic-state textarea behaviour**

- **Automatic quarantining**

- **Auto-clean & safe-message regeneration**

> **This creates a realistic demonstration of how integrity systems ***detect, block, and recover*** from offensive content.**

--- 

## **3. High-Fidelity Interactive Console**

### **The UI is engineered to behave like a live security system:**

- **Animated terminal-style stream initialization**

- **SMS & Email dual visualization zones**

- **Dynamic envelope / junking animation**

- **Bubble-shield blocking for SMS threats**

- **Confidence bars with smooth transitions**

- **Result card with adaptive colour & tone**

- **Full desktop + mobile responsiveness**

> **The interface avoids randomness that reduces trust and instead uses ***structured, governed behaviours***.**

---


## **4. Local Logging & Intelligence Archive**

### **Without needing a backend database, INBOXIS AI maintains:**

- **Timestamped inference history**

- **Source-type metadata (Email/SMS)**

- **Snippet storage**

- **Result + confidence logging**

- **Local retention window**

- **Full-screen log explorer**

- **Export-friendly structure**

> **All history remains on the user's device only.**

---


## **5. Controlled Email Injection System**

### **A structured sample-injection system simulates:**

- **Real recruiter emails**

- **Fake job scams**

- **Internshala-style mass emails**

- **Fake HR updates**

- **Genuine communication samples**

> **This supports ***consistent evaluation and meaningful testing***, not uncontrolled message randomness.**

---

## **6. Transparent System Architecture Note**

### **A visible architecture note reflects:**

- **System scope**

- **Model decisions**

- **Operational boundaries**

> **This mirrors enterprise-grade systems where architectural context is discoverable inside the platform.**

---

## 🧠 Model & Architecture Context

> **INBOXIS AI began as a simple classifier and evolved into a fully-realized system.**

### **Current Architecture Prioritizes:**

- **Deterministic classification**

- **Fast inference**

- **Interpretability**

- **UI-state synchronization**

- **Client-side persistence**

- **Offline operation**

---

### **Why Not Transformers?**

> **Transformer-based classifiers were intentionally excluded:**

- **Unnecessary overhead for short messages**

- **Excessive latency**

- **Reduced interpretability for a demo console**

- **No clear UX benefit in this context**

### **TF-IDF + BernoulliNB remains:**

- **Lightweight**

- **High-precision**

- **Highly interpretable**

- **Perfect for inbox-level text filtering**

> **The architecture supports future upgrades without interface changes.**

---

## **📂 Project Structure**

| File / Folder | Description |
|---------------|-------------|
| `Data/` | Dataset directory used by the system |
| ├── `Samples/` | Contains curated CSV samples for testing |
| │   ├── `sample.csv` | Sample dataset for UI/testing |
| │   └── `spam.csv` | Spam classification dataset |
| `Models/` | Serialized ML model artifacts |
| ├── `model.pkl` | Trained classification model |
| └── `vectorizer.pkl` | Fitted vectorizer used by the model |
| `Output/` | Generated assets and preview files |
| └── `UI.png` | Screenshot of the interface |
| `static/` | Static resource directory |
| └── `samples.json` | Predefined sample inputs for UI consumption |
| `Streamlit/` | Early prototype UI built using Streamlit |
| └── `app.py` | Streamlit application file |
| `templates/` | HTML templates for the Flask web interface |
| ├── `index.html` | Primary UI template |
| └── `original.html` | Initial version of the UI template |
| `app.py` | Main Flask backend handling routes and inference |
| `Dockerfile` | Configuration for containerization |
| `LICENSE` | Project license file |
| `package_extractor.py` | Text processing and utility logic |
| `README.md` | Documentation for setup and usage |
| `requirements.txt` | Required Python dependencies |
| `Sms_Spam_Detection.ipynb` | Jupyter notebook for model development |


---

### **🔒 Privacy & Data Handling**

### **INBOXIS AI strictly enforces:**

- **No data uploads**

- **No cloud logging**
- **No backend storage**
- **No analytics tracking**

> **All logs remain in ***browser localStorage***.**

> **This tool provides ***probabilistic classification***, not factual verification.**

---

## **🛠 Tech Stack**

### **Backend**

- **Python**

- **Flask**

- **scikit-learn**

- **TF-IDF Vectorizer**

- **Bernoulli Naive Bayes**

- **Pickle-serialized models**

### **Frontend**

- **HTML5**

- **TailwindCSS**

- **Vanilla JavaScript**

- **GSAP (for micro-interactions)**

- **Smooth-scrolling (Lenis-style behaviour)**

- **Chart.js for dashboard analytics**

- **JetBrains Mono + Poppins UI typography**

---

# ⚙️ Inference Flow

- **Message text received**

- **Context detection (Email vs SMS)**

- **Text preprocessing**

- **TF-IDF transformation**

- **Spam/Ham probability inference**

- **Profanity trigger evaluation**

- **UI response orchestration**

- **Logging & dashboard update**

> **This mirrors real production messaging pipelines used in enterprise security tools.**

---


## **⚠️ Limitations**

- **Model is classical, not transformer-based**

- **English-only support**

- **Limited message domains**

- **Profanity classifier is rule-based, not learned**

- **Not a replacement for real email filtering systems**

> **These constraints are intentional and acknowledged.**

---


# 🖥 System Interface Preview

**INBOXIS AI Interface**
![Output](UI.png)  

---

## **🏁 Conclusion**

> **INBOXIS AI demonstrates how a classical ML model can be elevated into a **professional, intelligence-grade system** through disciplined design, controlled behaviour, and thoughtful user experience.**




## **📜 License**

This project is licensed under the **Apache License, Version 2.0**.
See the `LICENSE` file for details.

---

## **👤 Author**

**Nayan Darokar**

**Aspiring Data Scientist — Intelligent Interfaces & ML Systems Engineering**

> **Connect With Me Here:**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayan-darokar-468a85294/) 
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reachout.nayan@gmail.com)
[![Portfolio](https://img.shields.io/badge/-Portfolio-FFA500?style=for-the-badge&logo=google-chrome&logoColor=black)](https://nayan-portfolio-nine.vercel.app/)
