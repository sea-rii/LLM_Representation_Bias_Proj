# 🧠 Unmaskind Demographic Bias in Large Language Models

**Author:** Sai Siri Chittineni  
**Advisor:** Dr. Ke Yang  
**Affiliation:** University of Texas at San Antonio
**Fellowship:** SDS Undergraduate Research Fellowship  
**Timeline:** January - August 2025



## 📌 Overview

This repository presents my research on identifying and evaluating **representation bias in large language models (LLMs)** when labeling demographic information from medical patient descriptions.

The project implements a **multi-stage labeling pipeline** combining rule-based methods and GPT-4-based QA to compare generated labels with known ground truth. The goal is to assess how well LLMs represent diverse demographic attributes across 15 categories and to expose patterns of bias or misrepresentation.



## 🎯 Objective

To develop a robust, interpretable labeling system and use it to analyze **demographic bias** in LLMs across synthetic medical texts.



## 🧪 Methodology

### 📁 Dataset

- **Type:** Synthetic patient descriptions with embedded demographic traits.
- **Format:** CSV files with free-text descriptions and corresponding ground-truth demographic labels.

### 🛠️ Labeling Pipeline Components

- **Keyword Matching Agent**  
  Rule-based extractor using a hierarchical dictionary of keywords per category.

- **QA Agent (Fallback)**  
  Invoked only when keyword matching returns `'n/a'`. Prompts GPT-4 to answer questions about missing demographic attributes.

- **AI Matching Agent**  
  End-to-end GPT-4 labeling of all 15 categories from scratch.

- **Truth Generator**  
  Generates ground truth labels for each patient description for benchmarking.

### 🧬 Demographic Categories (15)

- Gender  
- Age  
- Disability Status  
- Race
- Country 
- State
- Region 
- Languages spoken
- Education level
- Social media usage 
- Religion
- Marital status 
- Profession
- Household income classification
- Housing situation



## 📊 Evaluation Metrics

- **Pipeline Accuracy:** Final accuracy of keyword + QA system.
- **QA Accuracy:** Accuracy when the fallback GPT QA was triggered.
- **ChatGPT Accuracy:** Performance of GPT-4 when used standalone to extract all labels.


## 🔍 Key Findings

- ✅ Highest performance in labeling **gender**, **education level**, and **marital status**.
- ⚠️ Lowest performance in **income** and **disability status**, suggesting GPT struggles with nuance or implicit references.
- 📈 The QA Agent significantly improved recall, especially for underrepresented categories.
- 🤖 Direct GPT-4 (AI Matching Agent) showed strong performance but was inconsistent across sensitive categories.

