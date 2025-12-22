# **🚀 RiskFlow v2.0 — Enterprise-Grade Customer Churn Intelligence & Risk Evaluation Console**

> **RiskFlow v2.0 is a high-fidelity, enterprise-styled churn intelligence platform designed to simulate how modern financial analytics systems ingest structured customer attributes, evaluate churn risk, and surface interpretable insights through controlled, system-oriented workflows.**

> **The project intentionally transcends notebook-level experimentation by presenting a full decision-support console that integrates machine learning inference, analytical visualization, session logging, and report-style interpretation.**

> **RiskFlow is not positioned as a product demo, but as a system design artifact — reflecting how churn intelligence tools are architected, reviewed, and reasoned about inside real organizations.**

---

# 🚀 RiskFlow v2.0 — Enterprise-Grade Customer Churn Intelligence

> [!TIP]
> **In a hurry?** For a high-level overview of the optimization logic, churn metrics, and engineering highlights, please refer to the **[Executive Summary (README.md)](./README.md)**.

---

## **Live Application**
**The operational deployment of RiskFlow v2.0 is available for interactive risk evaluation.**

**Test probabilistic churn forecasting, geographic segmentation, and the "TensorFlow-less" optimized inference engine.**

[![🔗 Visit Live App](https://img.shields.io/badge/🔗%20Visit%20Live%20App-000000?style=for-the-badge&logo=safari&logoColor=white)](https://riskflow.onrender.com/)

---

## **📌 System Classification & Intent Disclosure**

> **RiskFlow v2.0 is an educational and portfolio-focused simulation created to demonstrate applied machine learning, system architecture thinking, and enterprise-style analytical UI design.**

> **All customer profiles, predictions, probabilities, logs, and dashboards are simulated for demonstration purposes only.**

> **The system does not connect to any financial institution, does not ingest real customer data, and must not be interpreted as a production banking or risk management platform.**

> **The objective of this project is realism in system behavior, transparency in interpretation, and discipline in presentation — not business deployment.**

---

## **🧩 Overview**

#### **RiskFlow evaluates customer churn likelihood using structured banking-style attributes, including but not limited to:**

- **Credit score and financial stability indicators**  

- **Demographic context**  

- **Account tenure and activity signals**  

- **Balance and salary-related features**  

- **Geographic segmentation**  

> **Rather than exposing a single prediction, the system contextualizes churn risk through a ***multi-layer analytical console*** featuring:**

- **Probabilistic risk gauges**  

- **Confidence-driven classification states**  

- **Risk factor summaries**  

- **Session analytics dashboards**  

- **Persistent historical logs**  

- **Per-customer analytical breakdowns**  

> **This approach reflects how churn predictions are ***operationalized within decision-support environments***, not merely computed.**

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

## **🧠 Functional Capabilities**

#### **Churn Prediction Engine**

- **Gradient Boosting–based binary classifier**  

- **Outputs: EXIT or STAY**  

- **Probability-calibrated confidence scoring**  

- **Feature normalization using a pretrained StandardScaler**  

---

#### **Risk Visualization Layer**

- **Semi-circular probability gauge**  

- **Animated inference feedback for system realism**  

- **Dynamic labeling for stability vs churn risk states**  

---

#### **Controlled Simulation Framework**

- **Deterministic probability orchestration with bounded variance**  

- **Enables consistent demonstrations without external dependencies**  

- **Decouples UI behavior from live backend constraints**  

---

#### **Session Analytics Dashboard**

- **Aggregate churn vs safe distribution**  

- **Geographic segmentation analysis**  

- **Total inference counters**  

- **Live-updating session summaries**  

---

#### **Persistent Client-Side Logging**

- **Local session storage using browser `localStorage`**  

- **Timestamped prediction records**  

- **User-level overwrite and update logic**  

- **Zero server-side data persistence**  

---

#### **Analytical Report Inspection**

- **Click-through access to historical records**  

- **Per-customer analytical modal**  

- **Confidence bars and structured reasoning summaries**  

- **Explicit churn vs safe status indicators**  

---

## **🧠 Model & System Architecture**

#### **Predictive Pipeline**

- **StandardScaler for feature normalization**

- **Gradient Boosting Classifier for churn inference**  

- **Serialized model artifacts using `joblib`**  

[!IMPORTANT]

## **⚡ Architectural Optimization Note**

> **Production Choice: While this system includes a Deep Learning (ANN) implementation, the live console leverages a Gradient Boosting Engine to maintain a strict <500MB RAM footprint (optimized for Render Free Tier).**

> **The Decision: To ensure 100% stability and sub-millisecond inference, I opted for a lean ML framework over a heavy DL stack, successfully prototyping a "TensorFlow-less" inference method using raw NumPy weight extraction (see Models/Optimization/) to minimize server-side overhead.**

---

#### Backend Responsibilities (Flask)

- **Input ingestion and validation**  

- **Feature transformation**  

- **Model inference**  

- **Probability extraction**  

---

#### **Frontend Responsibilities**

- **User interaction orchestration**  

- **Risk simulation logic**  

- **Visualization rendering**  

- **Session logging and updates**  

- **Analytical reporting**  

> **The system is intentionally ***modular***, allowing future model or feature upgrades without requiring interface redesign.**

---

## **🔒 Privacy, Ethics & Data Boundaries**

#### **RiskFlow enforces strict data isolation principles:**

- **No server-side databases**  

- **No cloud persistence**  

- **No third-party analytics**  

- **No external APIs**  

- **No real customer data**  

> **All data remains local to the user’s browser and can be fully cleared through the interface.**

> **Predictions represent probabilistic analytical signals, not factual determinations.**

---

## **🛠 Technology Stack**

#### **Backend**

- **Python 3**  
- **Flask**  
- **NumPy**  
- **Joblib**  
- **Gradient Boosting Classifier**  
- **StandardScaler**  

### Frontend

- **HTML5**  
- **TailwindCSS (custom configuration)**  
- **Vanilla JavaScript (ES6+)**  
- **Chart.js with DataLabels plugin**  
- **Lucide Icons**  
- **Google Fonts (Poppins, Bebas Neue, Zen Dots, Italianno)**  

---

## **Persistence**
- **Browser-based `localStorage` (session-level simulation)**

---
## **📂 Project Structure**

| File / Folder                              | Description                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| `Data/`                                   | Dataset directory                                                     |
| └── `Churn_Modelling.csv`                 | Customer churn dataset used for modeling                              |
|                                           |                                                                      |
| `DL_Version/`                             | Deep Learning–based implementation                                    |
| └── `Churn_Prediction_DL.ipynb`           | Deep Learning notebook for churn prediction                           |
|                                           |                                                                      |
| `ML_Version/`                             | Machine Learning–based implementation                                 |
| └── `Bank_Customer_Churn.ipynb`           | ML notebook for customer churn analysis                                |
|                                           |                                                                      |
| `Models/`                                 | Saved and serialized trained models                                    |
| ├── `DL_models/`                          | Deep Learning trained models                                           |
| │   ├── `model.keras`                    | Saved Keras deep learning model                                        |
| │   └── `model_weights.npz`              | Numpy file containing model weights                                    |
| ├── `ML_models/`                          | Machine Learning trained models                                        |
| │   ├── `gbc_model.pkl`                  | Gradient Boosting Classifier trained model                              |
| │   └── `scaler.pkl`                     | Scaler used for feature preprocessing                                  |
| └── `Optimization/`                      | Model optimization utilities                                           |
|     └── `export_weights.py`              | Script to export / manage model weights                                 |
|                                           |                                                                      |
| `Output/`                                 | Generated outputs and assets                                           |
| └── `UI.png`                             | Screenshot of the application user interface                            |
|                                           |                                                                      |
| `templates/`                              | Frontend HTML templates                                                |
| └── `index.html`                         | Main UI template                                                       |
|                                           |                                                                      |
| `app.py`                                  | Flask backend handling routing and inference                            |
| `Dockerfile`                              | Docker configuration for containerized deployment                      |
| `requirements.txt`                        | Python dependencies for the complete project                            |
| `readme.md`                               | Project-level documentation                                            |

---

## **⚙️ End-to-End Inference Flow**

- **User inputs customer attributes**  

- **Feature vector assembled and normalized**  

- **Model generates churn classification**  

- **Probability extracted from model output**  

- **Visualization layer renders**:
   - **Risk gauge**  
   - **Confidence score**  
   - **Status indicators** 
    
- **Session data logged locally**  

- **Dashboards update dynamically**  

- **Detailed analysis available via modal inspection**  

> **This layered separation mirrors ***production-grade ML pipelines***, isolating inference, presentation, and observability concerns.**

---

## **⚠️ Known Constraints & Limitations**

- **Predictions are simulated for demonstration realism**  

- **No real banking integration**  

- **No external validation pipelines**  

- **Model performance reflects training data quality**  

- **Not suitable for operational financial decision-making**  

> **These constraints are explicit, intentional, and documented by design**.

---

## **🖥 Interface & Interaction Summary**

#### **RiskFlow v2.0 includes:**

- **Console-style prediction interface**  

- **Analytical dashboards**  

- **Master archive and log viewer**  

- **Glassmorphism-based modal dialogs**  

- **Embedded system notices and disclaimers**  

> **The interface emphasizes ***clarity, restraint, and credibility*** over decorative complexity.**

---

## 🖥 System Interface

> **RiskFlow v2.0 is designed as an analytical console — not a consumer-facing banking application.**

**Primary Analysis Interface**

![RiskFlow – Churn Risk Analysis Console](./Assets/UI.png)

> **The interface demonstrates structured data input, probability-based risk visualization, session analytics, and historical log inspection.**

> **Visual hierarchy, interaction pacing, state transitions, and feedback behavior are intentionally governed to support interpretation and review rather than speed or automation.**


---

## **🏁 Conclusion**

- **RiskFlow v2.0 demonstrates how classical churn prediction models can be elevated into **credible, enterprise-style intelligence systems** through disciplined system design, transparent modeling, and professional UI execution.**

---

## **📜 License**

**Licensed under the Apache License 2.0. See the LICENSE file for full terms.**

---


# **👤 Author:  Nayan Darokar** 
> **Data Scientist (Aspiring) | Intelligent Systems & Applied ML Engineering**

---

> **Connect With Me Here:**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayan-darokar-468a85294/) 
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reachout.nayan@gmail.com)
[![Portfolio](https://img.shields.io/badge/-Portfolio-FFA500?style=for-the-badge&logo=google-chrome&logoColor=black)](https://nayan-portfolio-nine.vercel.app/)

---

