# RLHF Evaluation Analysis with a Synthetic LLM Preference Dataset

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-150458?logo=pandas)


## Overview

This project explores the evaluation of **Large Language Models (LLMs)** using a synthetic **Reinforcement Learning from Human Feedback (RLHF)** dataset. Rather than training or fine-tuning a language model, this notebook focuses on understanding how modern LLMs are evaluated through reward models, human preferences, and alignment-related metrics.

The dataset consists of **120 synthetic preference pairs** generated for educational purposes. Although the dataset is not collected from real human annotations, it is designed to resemble the structure of an RLHF evaluation dataset used in research and production systems.

The goal of this project is to gain practical experience with reward model evaluation and to analyze policy improvements across different model versions.

---

## Objectives

- Understand the structure of an RLHF preference dataset
- Analyze reward model performance using pairwise preference data
- Compare different policy versions (Baseline → SFT → RLHF)
- Evaluate alignment-related metrics
- Explore task-specific and time-based model performance
- Practice LLM evaluation workflows commonly used in industry

---

## Dataset

The synthetic dataset contains **120 preference pairs**.

Each sample includes:

- Prompt
- Response A
- Response B
- Human preferred response
- Human evaluation scores
- Reward model scores
- Hallucination labels
- Safety violation labels
- Bias labels
- Latency
- Token counts
- Policy version
- Task type
- Annotation metadata

Policy versions:

- Baseline
- SFT (Supervised Fine-Tuning)
- RLHF v1
- RLHF v2

Task categories include:

- Reasoning
- Coding
- Summarization
- Translation
- Truthfulness
- Safety
- Refusal Quality
- Medical Caution
- Helpfulness
- Bias

---

## Evaluation Metrics

This notebook analyzes multiple aspects of LLM quality.

### Human Evaluation

- Helpfulness
- Refusal Quality
- Human Preference (Chosen Response)

### Reward Model Evaluation

- Reward Model Score
- Reward Margin
- Absolute Reward Margin
- Pairwise Reward Model Accuracy

### Alignment Metrics

- Hallucination Rate
- Safety Violation Rate
- Bias Rate

### Efficiency Metrics

- Response Latency
- Token Count

---

## Analysis Performed

The notebook includes the following analyses.

### Policy-Level Analysis

Comparison of

- Baseline
- SFT
- RLHF v1
- RLHF v2

using

- Reward model accuracy
- Helpfulness
- Hallucination
- Safety
- Bias
- Latency

---

### Task-Based Analysis

Performance comparison across different task categories.

Examples:

- Reasoning
- Coding
- Translation
- Summarization
- Truthfulness
- Safety

---

### Time-Based Analysis

Performance trends grouped by evaluation date.

Metrics include

- Reward model accuracy
- Helpfulness
- Hallucination rate

---

### Annotator Analysis

Comparison of annotator behavior using

- Reward model agreement
- Preferred response distribution
- Average helpfulness
- Annotation latency

---

### Reward Model Analysis

Evaluation of

- Pairwise accuracy
- Reward score distribution
- Reward margins
- Confidence analysis

---

## Key Findings

- RLHF models generally reduced hallucination compared with the Baseline and SFT models.
- SFT achieved the highest average helpfulness score but exhibited higher hallucination rates than the RLHF models.
- RLHF v2 achieved the lowest hallucination rate while maintaining competitive helpfulness and the highest pairwise reward model accuracy.
- Helpfulness alone was insufficient for comparing model quality; hallucination, safety, and reward model accuracy provided complementary insights.
- Different evaluation metrics revealed different strengths and weaknesses of each policy version, highlighting the importance of multi-dimensional LLM evaluation.

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Limitations

This project uses a **synthetic dataset** generated for educational purposes.

Therefore,

- results should not be interpreted as benchmark performance,
- statistical conclusions are limited by the dataset size,
- the notebook focuses on evaluation methodology rather than model training.

---

## Future Improvements

Possible extensions include:

- Inter-annotator agreement (Cohen's κ / Fleiss' κ)
- Calibration analysis for reward models
- Precision, Recall, and F1 for hallucination detection
- Confidence calibration using reward margins
- Visualization dashboards
- Evaluation using public datasets

---

## Disclaimer

The dataset used in this repository is synthetically generated for learning purposes and does not represent real human annotation data or production LLM evaluation results.
