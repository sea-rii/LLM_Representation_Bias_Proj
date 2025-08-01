# 🧠 Unmasking Demographic Bias in Large Language Models

**👩‍💻 Author:** Sai Siri Chittineni  
**🧑‍🏫 Advisor:** Dr. Ke Yang  
**🏫 Affiliation:** University of Texas at San Antonio  
**📅 Fellowship:** SDS Undergraduate Research Fellowship  
**📆 Timeline:** January – August 2025  


## 🔎 Overview

This project investigates **representation bias** in large language models (LLMs) when labeling **demographic information** from medical patient descriptions.

It introduces a **multi-stage labeling pipeline** that combines:

- 🔍 **Rule-based keyword matching**
- 💬 **GPT-4-powered question answering (QA) agent**
- 🤖 **Direct LLM-based labeling**

The final output is evaluated against known ground truth labels to uncover bias in demographic predictions across **15 distinct categories**.



## 🎯 Objective

> To design an **interpretable**, **accurate**, and **scalable** labeling pipeline and use it to analyze **demographic bias** in LLMs using synthetic medical descriptions.



## 🧪 Methodology

### 🗃️ Dataset

- **Type:** Synthetic patient descriptions
- **Includes:** Embedded demographic traits
- **Format:** `.csv` with free-text + structured ground-truth labels



### 🔁 Labeling Pipeline

| Component | Description |
|-----------|-------------|
| **Keyword Matching Agent** | Rule-based matcher using a nested keyword hierarchy |
| **QA Agent (Fallback)** | Triggered when keyword output is `'n/a'`; asks GPT-4 directly |
| **AI Matching Agent** | End-to-end GPT-4 agent that labels all categories |
| **Truth Generator** | Simulated ground-truth generator for benchmarking accuracy |



### 🧬 Demographic Categories (15)

- 🧑 Gender  
- 🎂 Age  
- ♿ Disability Status  
- 🌍 Race  
- 🗺️ Country  
- 🏙️ State  
- 🧭 Region  
- 🗣️ Languages Spoken  
- 🎓 Education Level  
- 📱 Social Media Usage  
- 🕊️ Religion  
- 💍 Marital Status  
- 👩‍🔧 Profession  
- 💵 Household Income Classification  
- 🏡 Housing Situation  



## 📊 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| ✅ **Pipeline Accuracy** | Accuracy of the combined keyword + QA approach |
| 🧠 **QA Accuracy** | Accuracy when GPT QA was triggered (fallback mode) |
| 🤖 **ChatGPT Accuracy** | Performance of GPT-4 when labeling directly without scaffolding |



## 🔍 Key Findings

- ✅ **Two-stage pipeline**
    - high performance*: household income, marital status, education level
    - low performance*: country, race


- 📈 **QA Agent** 100% accuracy in state and 86.8% in education—but had limited overall impact due to infrequent triggering.

- 🤖 **Direct GPT-4 agent** 100% accuracy in gender, state, and social media usage, though it struggled with disability status.


