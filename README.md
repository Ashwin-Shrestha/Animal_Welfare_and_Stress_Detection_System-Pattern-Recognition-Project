# Animal Welfare and Stress Detection System  

---

## 📌 Project Overview
This repository contains the complete source code and documentation for the **Animal Welfare and Stress Detection System**, 

The project implements a **vision-based animal welfare and stress-risk screening system** using the **Animals-10 dataset**.  
The system does **not diagnose physiological stress**; instead, it infers **visual indicators associated with potential stress or welfare compromise**, such as posture and uncertainty in visual recognition, and presents them through interpretable models and rule-based decision support.

---

## 👥 Group Members & Assigned Roles  
⚠ **Roles are explicitly stated, as required**

- **Ashwin Shrestha – Technical Lead**  
  - System design and architecture  
  - Model implementation (base learner, meta-learner, rule engine)  
  - Experiment orchestration  
  - Final submission on Microsoft Teams  

- **Arpan Rai – Figures, Tables & Presentation**  
  - Dataset loading and preprocessing  
  - Feature extraction and experimental execution  
  - Validation of results  

- **Ashwin Shrestha/Arpan Rai – Report & Storytelling**  
  - Writes the complete report using the provided **Overleaf template**  
  - Ensures a coherent narrative across sections  
  - Aligns methodology, results, and discussion
 

## ▶️ Instructions to Reproduce Results

1. Install **Anaconda (Python 3.10 recommended)**
2. Place `kaggle.json` in `~/.kaggle/`
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook

## 📂 Dataset
- **Dataset Name:** Animals-10  
- **Source:** Kaggle (`alessiocorrado99/animals10`)  
- **Description:** ~26,000 images across 10 animal species  
- **Note:** No ground-truth stress or physiological labels are provided

---

## 🧠 Model Architecture

### Base Learner
- **ResNet-18 (pretrained)**
- Frozen backbone, trainable classification head
- Task: Animal species classification

### Meta-Learner
- Logistic Regression
- Inputs:
  - Posture-based visual proxy features
  - CNN species probability vectors
- Task: Stress-risk proxy inference

### Rule Engine
- Interpretable rule-based layer
- Outputs:
  - Stress-risk level (Low / Moderate / High)
  - Human-review flag for uncertain predictions

---

## 🎯 Research Questions
The notebook addresses the following research questions:

- **RQ1:** Species recognition accuracy using CNNs  
- **RQ2:** Extraction of posture-related visual proxy features  
- **RQ3:** Performance gains from posture–appearance feature fusion  
- **RQ4:** Robustness under missing or noisy visual information  
- **RQ5:** Explainability and rule-based decision support for end users  

---


