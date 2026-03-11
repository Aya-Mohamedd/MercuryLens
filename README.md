# 🐟 MercuryLens: Predictive Modeling of Chemical Contaminants in Ontario Fish

**MercuryLens** is an advanced machine learning framework designed to safeguard public health by predicting fish consumption advisory levels (Safe, Moderate, and High Risk) across Ontario's vast waterbodies. 

By transitioning from traditional descriptive lookup tables to an automated predictive system, this project provides a robust tool for Ontario residents, particularly vulnerable populations, to make informed decisions about food safety.

---

## 🚀 Project Overview
* **Domain:** Environmental Science / Public Health / Machine Learning
* **Data Source:** 2025 Ontario Fish Advisory Database (108,000+ records).
* **Objective:** Predict the safety level of fish consumption based on biological and geospatial data.
* **Key Achievement:** Achieved **83.25% Accuracy** using a Stacking Ensemble model.

---

## 📊 The Problem
Fishing is a $1.41B sector in Canada, yet bio-accumulative toxins like **Mercury** and **PCBs** pose significant health risks. Current systems rely on manual lookups which are not predictive for new or changing environmental conditions. **MercuryLens** fills this gap by providing data-driven, predictive insights.

## 🛠️ Tech Stack
* **Language:** Python
* **ML Models:** LightGBM, CatBoost, XGBoost, Random Forest, Stacking Classifier.
* **Data Analysis:** Pandas, NumPy, Scikit-learn.
* **Visualization:** Power BI (Project Dashboard), Seaborn, Matplotlib.

---

## 🧠 Machine Learning Pipeline

### 1. Data Engineering & Spatial Intelligence
* **Geospatial Scaling:** Developed a custom `Grid_ID` feature to group locations by coordinates, allowing the model to understand regional contamination patterns.
* **Biological Features:** Processed `Species`, `Length Category`, and engineered `Mean_Length` to capture bio-accumulation trends.
* **Class Balancing:** Utilized **Balanced Class Weights** to ensure the model accurately identifies "High Risk" cases, which are critical for public safety.

### 2. Model Architecture
After extensive iteration, the **Stacking Ensemble** was selected as the final model:
* **Base Models:** LightGBM, CatBoost, and Random Forest.
* **Meta-Model:** Logistic Regression.
* **Why Stacking?** This approach effectively minimized **False Negatives** (predicting a toxic fish as "Safe"), ensuring the highest level of reliability for health advisories.

---

## 📈 Results & Key Insights
| Metric | Score |
| :--- | :--- |
| **Accuracy** | 83.25% |
| **F1-Score (High Risk)** | 0.83 |
| **Primary Pollutant** | Mercury (86.1% of advisories) |

* **Feature Importance:** `Mean_Length` and `Grid_ID` were the top predictors. This confirms that a fish's **size (age)** and **exact location** are more critical than the species alone.

---

## 📂 Repository Structure
* `CSAI801-AI&ML.Team 36.Project Code.ipynb`: The complete Python implementation from EDA to Modeling.
* `CSAI801-AI&ML.Team 36.MercuryLens Project Dashboard.pbix`: Interactive Power BI dashboard.
* `CSAI801-AI&ML.Team 36.Project Report.pdf`: Detailed technical documentation.
* `Guide_to_Eating_Ontario_Fish_Advisory_Database_2025.csv`: The dataset used for training and testing.

---

## 🔮 Future Scope
* **Real-time Integration:** Incorporating water temperature and pH levels.
* **Industrial Proximity:** Adding proximity data to industrial sites to refine geospatial risk levels.
* **Deployment:** Developing a mobile-friendly API for real-time safety checks for anglers.

---

## 👥 Team (Group 36)
* **Aya Mohamed Mahmoud**
* **Fatma Ahmed Mansour**
* *Supervised by: Dr. Marwa ElSayed*

---
**Queen's University - CSAI 801: AI & Machine Learning**
