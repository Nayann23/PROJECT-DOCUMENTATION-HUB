# **🚀 INFERSIS AI — News Intelligence & Category Classification Console**

> **INFERSIS AI is an enterprise-styled news classification and intelligence console designed to inspect, categorize, and contextualize raw news content through a production-oriented ML pipeline and a high-fidelity operational UI.**

> **Rather than presenting classification as a standalone prediction task, INFERSIS AI is intentionally architected as an internal intelligence tool, mirroring how real-world content monitoring and media intelligence systems are built, observed, and interacted with inside organizations.**

---

## **Live Application**

**Access the production build of ***INFERSIS AI***, the enterprise-styled news taxanomy and content-intelligence system**

**Evaluate topic classification, sentiment context probability distributions, and the full operator console.**

[![🔗 Visit Live App](https://img.shields.io/badge/🔗%20Visit%20Live%20App-000000?style=for-the-badge&logo=safari&logoColor=white)](https://infersis-ai.onrender.com)

---

## **Dataset Source:**
```bash
https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset 

```
***This project utilizes the AG News Topic Classification dataset made available on Kaggle. Full credit goes to the original dataset creators for collecting and publishing the news corpus. This openly available dataset enabled the training, evaluation, and demonstration of the news classification system presented in this project.***

---

## **🧩 Overview**

**INFERSIS AI classifies news articles into high-level domains such as:**

- **World**

- **Sports**

- **Business**

- **Science & Technology**

> **The platform integrates classical NLP modeling with a system-centric frontend that emphasizes observability, traceability, and user trust.**

> **This project prioritizes system realism and delivery discipline over experimental novelty.**

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

#### **1. News Category Classification Engine**

- **TF-IDF vectorization for textual feature extraction**

- **Multinomial Naive Bayes for deterministic, interpretable classification**

- **Confidence scoring derived from class probability distributions**

- **Fast, low-latency inference suitable for repeated interactive use**

--- 

#### **2. Contextual Content Analysis**

## **In addition to category prediction:**

- **Sentiment analysis via TextBlob**

- **Keyword/entity extraction using frequency-based heuristics**

- **Word-count inspection for content density awareness**

> **These signals are surfaced to enrich interpretation without overloading the primary decision.**

---

#### **3. Interactive Intelligence Console (UI)**

**The frontend is designed to emulate an internal operator console rather than a public demo.**

## **Key characteristics:**

- **Analyzer-first workflow with explicit “Initialize Scan” control**

- **Visual category graph emphasizing classification pathways**

- **Probability distribution charts for transparency**

- **Live system status indicators (Idle → Scanning → Complete)**

- **Responsive layout optimized for desktop and mobile**


> **UI behavior intentionally includes staged animations and feedback to simulate real system orchestration.**
---

#### **4. Local Activity Logging & Analytics**

**To demonstrate production-grade observability without backend storage:**

- **Inference history persisted via browser localStorage**

- **Time-bounded retention policy (7 days)**

- **Inline recent activity table**

- **Full-screen log viewer with export capability**

- **Real-time dashboard charts for:**
    
    - **Category distribution**
    
    - **Sentiment trends**

> **No data leaves the client environment.**

---

#### **5. Sample Injection & Controlled Testing Flow**

**INFERSIS AI includes a sample-injection system backed by curated CSV data to:**

- **Support rapid evaluation**

- **Simulate ingestion from controlled sources**

- **Avoid randomness that undermines confidence**

> **Samples are fetched intentionally, reinforcing the idea of a governed pipeline.**

---

#### **6. Transparent Architecture Disclosure**

> **A floating System Architecture Note is included directly in the interface to clarify design scope and evolution.**

> **This reflects real-world documentation practices where architectural context is discoverable, not disruptive.**

---

## **🧠 Model & Architecture Context**

> **This system originated as an earlier experimental classifier and was later refined to be production-oriented.**

**The current iteration focuses on:**

- **Migrating from Streamlit to Flask for greater routing, state, and UI control**

- **Redesigning the interface using full-stack engineering patterns**

- **Preserving the existing model while modernizing the surrounding system**

> **Transformer models (e.g., BERT) were intentionally not introduced during this refinement cycle.For news taxonomy, TF-IDF + Multinomial Naive Bayes remains fast, interpretable, and sufficient.** 

> **The architecture is designed to support future model upgrades without requiring changes to logging, visualization, or delivery layers.**

---

## **🔒 Privacy & Data Handling**

- **No server-side storage**

- **No databases**

- **No external logging**

- **All inference history remains local to the user’s browser**

- **This tool produces probabilistic classifications, not factual assertions**

> **Clear boundaries are intentionally maintained.**

---

## **🛠 Tech Stack**

#### **Backend**

- **Python 3**

- **Flask**

- **Scikit-learn**

- **Pandas**

- **NumPy**

- **TextBlob**

- **Pickle-serialized models**

#### **Frontend**

- **HTML5**

- **Tailwind CSS (custom-configured)**

- **Vanilla JavaScript**

- **Chart.js**

- **Google Fonts (Oswald, Inter, Poppins, JetBrains Mono)**


---
## **📂 Project Structure**

| File / Folder | Description |
|---------------|-------------|
| `app.py` | Core Flask backend handling routing, ML inference, and API responses |
| `package_extractor.py` | Utility module for text processing, keyword extraction, and auxiliary logic |
| `requirements.txt` | Python dependencies required to run the system |
| `README.md` | Product-level documentation describing system design, intent, and usage |
| `LICENSE` | Apache License 2.0 defining usage and distribution terms |
| `News_Category_Classification.ipynb` | Jupyter notebook containing the original training and experimentation workflow |
| `Data/` | Dataset storage and sample injection sources |
| ├── `Sample/` | Curated sample data used for controlled UI testing |
| │   └── `samples.csv` | Sample news records for interactive injection |
| └── `train.csv` | Training dataset used during model development |
| `Models/` | Serialized machine learning artifacts |
| ├── `mnb_model.pkl` | Trained Multinomial Naive Bayes classification model |
| └── `tfidf_vectorizer.pkl` | TF-IDF vectorizer aligned with the trained model |
| `Streamlit/` | Experimental interface from the early prototyping phase |
| └── `streamlit_app.py` | Streamlit-based UI used before migration to Flask |
| `templates/` | Frontend HTML templates for the Flask application |
| ├── `index.html` | Primary production UI for the intelligence console |
| ├── `Refined_Original.html` | Polished reference version of the interface |
| └── `Original.html` | Initial design prototype retained for comparison |
| `Output/` | Generated output assets for documentation and preview |
| └── `UI.png` | System interface screenshot used in README |

---

## **⚙️ Inference Flow**

- **Raw news text input received**

- **Text cleaning & normalization**

- **TF-IDF feature transformation**

- **Category probability inference**

- **Confidence computation**

- **Sentiment & keyword extraction**

- **Local activity logging**

- **Interactive visualization rendered**

> **This layered flow mirrors real production pipelines that separate inference, analysis, and presentation.**

---


## **⚠️ Limitations**

- **Categories are fixed and domain-specific**

- **No multilingual support**

- **Sentiment analysis is lexical, not contextual**

- **Not intended for editorial decision automation**

> **These constraints are acknowledged by design.**


---

## **🖥 System Interface Preview**

[![INFERSIS AI Interface](./UI.png)](./UI.png)

---

## **🏁 Conclusion**

**INFERSIS AI is a demonstration of how even classical NLP models can be elevated into credible, enterprise-style intelligence systems through disciplined system design, transparent architecture, and intentional UX.**

**It is well-suited for:**

- **ML & NLP portfolio demonstrations**

- **Internal tooling simulations**

- **Educational explainability examples**

- **Product-oriented ML showcases**

> **This documentation reflects the seriousness of the system it represents.**

---

> **An earlier Streamlit-based interface is preserved under /Streamlit for reference.**

---



## **Source Availiability**

> **The core source implementation for this project is maintained in a private repository. The code can be shared upon request for review or evaluation purposes.**


---

## **📜 License**

This project is licensed under the **Apache License, Version 2.0  
See the [LICENSE](./LICENSE) file for full license text and terms

---



# **👤 Author:  Nayan Darokar** 
> **Data Scientist (Aspiring) | Intelligent Systems & Applied ML Engineering**

---

> **Connect With Me Here:**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nayan-darokar-468a85294/) 
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:reachout.nayan@gmail.com)
[![Portfolio](https://img.shields.io/badge/-Portfolio-FFA500?style=for-the-badge&logo=google-chrome&logoColor=black)](https://nayan-portfolio-nine.vercel.app/)


