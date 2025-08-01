# 🧠 Unmasking Demographic Bias in Large Language Models

**👩‍💻 Author:** Sai Siri Chittineni  
**🧑‍🏫 Advisor:** Dr. Ke Yang  
**🏫 Affiliation:** University of Texas at San Antonio  
**📅 Fellowship:** SDS Undergraduate Research Fellowship  
**📆 Timeline:** January – August 2025  

---

## 🔎 Overview

This project investigates **representation bias** in large language models (LLMs) when labeling **demographic information** from medical patient descriptions.

It introduces a **multi-stage labeling pipeline** that combines:

- 🔍 **Rule-based keyword matching**
- 💬 **GPT-4-powered question answering (QA)**
- 🤖 **Direct LLM-based labeling**

The final output is evaluated against known ground truth labels to uncover bias in demographic predictions across **15 distinct categories**.

---

## 🎯 Objective

> To design an **interpretable**, **accurate**, and **scalable** labeling pipeline and use it to analyze **demographic bias** in LLMs using synthetic medical descriptions.

---

## 🧪 Methodology

### 🗃️ Dataset

- **Type:** Synthetic patient descriptions
- **Includes:** Embedded demographic traits
- **Format:** `.csv` with free-text + structured ground-truth labels

---

### 🔁 Labeling Pipeline

| Stage | Component | Description |
|-------|-----------|-------------|
| 🧩 Step 1 | **Keyword Matching Agent** | Rule-based matcher using a nested keyword hierarchy |
| 🧠 Step 2 | **QA Agent (Fallback)** | Triggered when keyword output is `'n/a'`; asks GPT-4 directly |
| 🤖 Step 3 | **AI Matching Agent** | End-to-end GPT-4 agent that labels all categories |
| 🏷️ Step 4 | **Truth Generator** | Simulated ground-truth generator for benchmarking accuracy |

---

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

---

## 📊 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| ✅ **Pipeline Accuracy** | Accuracy of the combined keyword + QA approach |
| 🧠 **QA Accuracy** | Accuracy when GPT QA was triggered (fallback mode) |
| 🤖 **ChatGPT Accuracy** | Performance of GPT-4 when labeling directly without scaffolding |

---

## 🔍 Key Findings

- ✅ **High performance** in predicting:  
  `Gender`, `Education Level`, `Marital Status`

- ⚠️ **Low performance** in predicting:  
  `Household Income`, `Disability Status`  
  *→ These require subtle understanding or inference beyond surface-level cues.*

- 📈 **QA Agent** improved recall significantly in underrepresented or ambiguous cases.

- 🤖 **Direct GPT-4 agent** performed well but inconsistently, especially on nuanced categories.

---

## 📁 Project Structure

