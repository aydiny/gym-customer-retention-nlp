# AI-Driven Customer Retention: Advanced NLP on Gym Reviews 🏋️‍♂️

> **Leveraging BERTopic, Emotion AI, and Local LLMs (Phi4) to uncover operational failures and churn drivers.**

![Status](https://img.shields.io/badge/Status-Research_Prototype-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![LLM](https://img.shields.io/badge/GenAI-Phi4_Mini-purple.svg)

## 📄 Project Overview
This project applies advanced Natural Language Processing (NLP) to over **40,000 customer reviews** (Google & Trustpilot) for a major fitness operator. The goal was to move beyond simple "Star Ratings" to identify specific, localized infrastructure failures that drive customer churn.

Using a combination of **BERTopic** for clustering and **Local LLMs (Phi4 via Ollama)** for reasoning, the analysis successfully pinpointed "Red Alert" locations requiring immediate intervention.

## 🔍 Key Business Insights
The analysis revealed a critical need to balance chain-wide standardization with targeted crisis management. The pipeline successfully categorized issues into **"Red Alert" Hotspots** (tactical, localized failures) and **Global Standards** (strategic, systemic improvements).

### 1. "Red Alert" Hotspots Detected
The model identified severe, localized infrastructure failures that required immediate physical intervention:
*   **Critical Utility Failures:** Pinpointed specific branches facing severe hot water outages and negative staff sentiment, triggering immediate deployment of emergency maintenance teams.
*   **HVAC Control Failures:** Distinguished effectively between general "hot weather" complaints and specific "control system failures" at premium locations, leading to targeted HVAC upgrades.
*   **Security Vulnerabilities:** Detected niche clusters of security-related keywords at specific urban sites, prompting recommendations for real-time CCTV monitoring enhancements.

### 2. Strategic "Global Standard" Recommendations
Beyond local fires, the analysis drove long-term operational strategy:
*   **Hygiene Standardization:** Identified systemic gaps in cleaning protocols, driving a recommendation for a uniform preventive maintenance plan across the network.
*   **Revenue Operations:** Highlighted friction points regarding parking fees and capacity management, supporting the business case for tiered fee systems and improved peak-time booking logic.

## 🛠️ Methodology & Tech Stack
The analysis is contained in a Jupyter Notebook implementing the following pipeline:

1.  **Data Preprocessing:** Cleaning and lemmatization of noisy UGC (User Generated Content).
2.  **Topic Modelling (BERTopic):** 
    *   Utilized **UMAP** for dimensionality reduction and **HDBSCAN** for clustering.
    *   Refined 61 initial topics down to core operational themes (Hygiene, HVAC, Staff, App, etc.)
3.  **Emotion Analysis:** 
    *   Applied the **Savani** model (DistilBERT-based) to isolate "Anger" and "Fear" from general dissatisfaction.
4.  **Generative AI Integration (RAG-style):**
    *   **Model:** Phi4-mini (3.8 billion parameters) running locally via **Ollama**.
    *   **Task:** Fed cluster keywords and representative documents to the LLM to generate executive summaries and maintenance tickets automatically.
---
*Author: Ali Aydin Yildiz*
