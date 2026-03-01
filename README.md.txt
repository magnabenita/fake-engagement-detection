# 🔍 Fake & Coordinated Engagement Detection System

This project presents a machine learning–driven system to detect **fake engagement and coordinated manipulation** on social media platforms using **behavioural analytics, anomaly detection, and network analysis**.

Unlike traditional rule-based approaches, the system models **how users behave over time, what they say, and who they interact with**, enabling detection of both **individual bots** and **coordinated bot rings**.

---

## 🚀 Key Features

- Behaviour-based bot detection (no user metadata required)
- Detection of **coordinated engagement rings**
- Interpretable **bot probability & authenticity score**
- Human-readable anomaly explanations
- Visual analytics for validation and case studies

---

## 🧠 Methodology Overview

### 1. Data Simulation
A realistic synthetic dataset is generated to model:
- **Organic users** (irregular timing, diverse text)
- **Random bots** (regular timing, templated comments)
- **Coordinated bot rings** (synchronized engagement bursts)

### 2. Feature Engineering
Key behavioural features include:
- Timing regularity (CV of time gaps)
- Burstiness (hourly spike ratios)
- Engagement ratios (like/comment/share)
- Repeated post interactions
- Text repetition (TF-IDF similarity)
- Co-engagement counts (coordination signal)

### 3. Models Used
- **Isolation Forest** → individual behavioural anomalies  
- **DBSCAN clustering** → coordinated behaviour detection  
- **Network analysis** → visualization of bot rings

### 4. Hybrid Scoring
All signals are fused into:
- **Bot Probability (0–1)**
- **Authenticity Score (0–100)**
- Risk categories: `Authentic`, `Suspicious`, `Likely Bot`

---

## 📊 Visual Analytics

The project includes:
- Risk category distribution
- Bot probability separation by user type
- Behaviour maps (timing vs coordination)
- Anomaly vs text repetition plots
- DBSCAN cluster visualization
- Coordination network graphs
- Individual case-study timelines

These plots provide **intuitive and explainable evidence** of malicious behaviour.

---

## 📈 Results


## 📊 Visual Results & Analysis

### 1. Risk Category Distribution
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/677a4e90-65d1-4098-8952-f5ac34dafe62" />


This plot shows how users are distributed across risk categories. Most users are classified as Authentic, while suspicious accounts are selectively flagged, demonstrating a cautious and realistic detection strategy.

---

### 2. Bot Probability by True Label
<img width="630" height="454" alt="image" src="https://github.com/user-attachments/assets/d9b33ec6-a410-49a8-8a2c-fa3feb84bb6d" />


Bot probability scores are clearly separated across organic users, bots, and coordinated bots, validating the effectiveness of behavioural feature engineering and hybrid scoring.

---

### 3. Behaviour Map: Timing Regularity vs Coordination
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/be864f01-52ef-4ce8-9f91-f996f1c44a5b" />


This behaviour map reveals three distinct groups: organic users, random bots with regular timing, and coordinated bots with high co-engagement activity.

---

### 4. Suspicion Space: Anomaly Score vs Text Repetition
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/781e2ac7-7d98-43d8-a679-c77dd6e67194" />


Accounts exhibiting both behavioural anomalies and repeated text patterns appear in the high-risk region, indicating automated or coordinated manipulation.

---

### 5. Coordination Clusters (DBSCAN)
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/338d8ea9-793d-4299-9db8-6b96ed71d436" />


DBSCAN clustering identifies dense groups of users with consistently high co-engagement activity, uncovering coordinated bot rings.

---

### 6. Coordination Network Graph
<img width="989" height="790" alt="image" src="https://github.com/user-attachments/assets/f3966c31-9cb5-4046-8e78-ba3703bd803c" />


This network graph visualizes strong co-engagement links between users. Dense subgraphs represent coordinated engagement campaigns, while organic users remain largely isolated.

---

### 7. Case Study: Engagement Timelines
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/034fce46-9852-41fa-b8d1-ac43e214a827" />
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/1d8c996c-fb6a-4e6c-ba44-6cba9100f18c" />
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/2945152d-3f09-4b22-8852-2421a916ca94" />


Engagement timelines of flagged users show burst-based and synchronized activity patterns, reinforcing the presence of automated or coordinated behaviour.

- **ROC-AUC:** 0.926
- <img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/a8fe5c23-ad47-4839-93f1-51deaf519697" />

- Strong separation between organic users, bots, and coordinated bot rings
- Clear detection of group-level manipulation not visible at individual level

---
