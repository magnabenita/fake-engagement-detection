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
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/b4990730-5c5e-4b3d-b491-8e644aaa9be7" />



This plot shows how users are distributed across risk categories. Most users are classified as Authentic, while suspicious accounts are selectively flagged, demonstrating a cautious and realistic detection strategy.

---

### 2. Bot Probability by True Label
<img width="630" height="454" alt="image" src="https://github.com/user-attachments/assets/237d5bb1-e71a-44c6-899c-1e528d2f3a78" />



Bot probability scores are clearly separated across organic users, bots, and coordinated bots, validating the effectiveness of behavioural feature engineering and hybrid scoring.

---

### 3. Behaviour Map: Timing Regularity vs Coordination
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/59f75841-054e-48f4-959a-6f026afa9e13" />


This behaviour map reveals three distinct groups: organic users, random bots with regular timing, and coordinated bots with high co-engagement activity.

---

### 4. Suspicion Space: Anomaly Score vs Text Repetition
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/520dca2a-65bc-466b-bf28-fddc317b4623" />


Accounts exhibiting both behavioural anomalies and repeated text patterns appear in the high-risk region, indicating automated or coordinated manipulation.

---

### 5. Coordination Clusters (DBSCAN)
<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/d0ba9c19-4f5f-47a9-9c93-a10e588fbca8" />


DBSCAN clustering identifies dense groups of users with consistently high co-engagement activity, uncovering coordinated bot rings.

---

### 6. Coordination Network Graph
<img width="989" height="790" alt="image" src="https://github.com/user-attachments/assets/c4a973a2-39bb-4a3c-ab0c-261ee7b4605b" />


This network graph visualizes strong co-engagement links between users. Dense subgraphs represent coordinated engagement campaigns, while organic users remain largely isolated.

---

### 7. Case Study: Engagement Timelines
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/f93cf961-f90f-4c62-bd27-dffa6e3cb64a" />
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/47f79de0-b21c-43eb-ae41-05f710c523c4" />
<img width="984" height="290" alt="image" src="https://github.com/user-attachments/assets/f6733c0d-9f51-41ed-880b-49efe791cfc6" />



Engagement timelines of flagged users show burst-based and synchronized activity patterns, reinforcing the presence of automated or coordinated behaviour.

- **ROC-AUC:** 0.926
- <img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/3b1b8f36-2538-44e3-b187-b360d61eee4d" />


- Strong separation between organic users, bots, and coordinated bot rings
- Clear detection of group-level manipulation not visible at individual level

---
