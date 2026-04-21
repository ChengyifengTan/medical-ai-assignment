# Medical AI Course - Hands-on Practice Notebooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

[中文](README.md) | English

**Medical AI Course Hands-on Practice Materials**

This project provides teaching-friendly Jupyter Notebook practice materials for the "Medical Artificial Intelligence" course, designed primarily for medical students with little or no programming background.

## Overview

This repository contains a series of carefully designed Jupyter Notebooks covering core AI topics in medicine, from data processing to deep learning. Each Notebook is grounded in realistic medical scenarios, helping students build intuitive understanding through case-driven learning.

### Design Principles

- **Accessibility > Mathematical Rigor**: Avoid complex formula derivations, use analogies and intuitive explanations
- **Case-Driven > Abstract Theory**: Introduce concepts through medical application scenarios
- **Step-by-Step > All-at-Once**: Break down concepts to prevent students from falling behind
- **Runnable > Optimal**: Keep code simple and easy to understand, ensuring students can successfully execute it

### Target Audience

- Medical students (no programming background or weak programming skills)
- Medical researchers interested in AI fundamentals
- Beginners interested in medical AI

## Course Content

| No. | Topic | Overview | Medical Application |
|-----|-------|----------|---------------------|
| 1 | Data Processing & Clustering | Data cleaning, standardization, K-Means clustering | Patient stratification (high/low risk) |
| 2 | Regression Analysis | Linear regression, model evaluation | Diabetes progression prediction |
| 3 | Classification | Logistic regression, decision tree, random forest, SVM | Heart disease prediction |
| 4 | Neural Networks | PyTorch basics, MLP, training pipeline | Diabetes risk classification |
| 5 | Convolutional Neural Networks (CNN) | CNN principles, image classification | Medical imaging diagnosis |
| 6 | Large Language Models | API calls, prompt engineering, information extraction | Medical record structuring |

## Project Structure

```
final/
├── README.md                                    # Documentation (Chinese)
├── README_EN.md                                 # Documentation (English)
├── CLAUDE.md                                    # Course design guidelines
├── 1_Data_Processing_and_Clustering/            # Data Processing & Clustering
│   ├── data_process_and_cluster.ipynb           # Student version
│   ├── data_process_and_cluster_answer.ipynb    # Teacher version
│   └── heart.csv                                # Heart disease dataset
├── 2_Regression/                                # Regression Analysis
│   ├── regression.ipynb                         # Student version
│   └── regression_answer.ipynb                  # Teacher version
├── 3_Classification/                            # Classification
│   ├── classification.ipynb                     # Student version
│   ├── classification_answer.ipynb              # Teacher version
│   └── heart.csv                                # Heart disease dataset
├── 4_Neural_Network/                            # Neural Networks
│   ├── neural_network.ipynb                     # Student version
│   └── neural_network_answer.ipynb              # Teacher version
├── 5_CNN/                                       # CNN
│   ├── CNN_classification.ipynb                 # Student version
│   └── CNN_classification_answer.ipynb          # Teacher version
└── 6_LLM_Application/                           # LLM Application
    ├── 大模型在医学中的应用入门.ipynb             # LLM introduction
    ├── 糖尿病诊断.md                             # Reference materials
    ├── 中国糖尿病流行的影响因素.md                # Reference materials
    ├── 中国糖尿病防治指南（2024版）- 节选.md      # Reference materials
    ├── 中国糖尿病防治指南（2024版）.md            # Reference materials
    └── 病例结构化结果.csv                        # Sample output
```

## Quick Start

### Requirements

- Python 3.8+
- Jupyter Notebook / Jupyter Lab

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/medical-ai-course.git
cd medical-ai-course/final
```

2. **Create virtual environment (recommended)**

```bash
conda create -n aimedicine python=3.9
conda activate aimedicine
```

3. **Install dependencies**

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
pip install jupyter

# For Neural Networks module
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

# For LLM Application module
pip install openai python-dotenv
```

4. **Start Jupyter Notebook**

```bash
jupyter notebook
```

### LLM Application Setup

The LLM practice requires an API Key:

1. Register and obtain an API Key (SiliconFlow recommended)
2. Create a `.env` file in the `6_LLM_Application/` directory
3. Add the following content:

```
OPENAI_API_KEY=your_api_key_here
BASE_URL=https://api.siliconflow.cn/v1
```

**Note**: Never commit your actual API Key to a public repository!

## Notebook Features

### 1. Teaching-Friendly Structure

Each Notebook includes:

- **Medical Background**: Realistic medical application scenarios
- **Method Explanation**: Analogies and intuitive explanations, avoiding complex formulas
- **Data Preparation**: Data fields with medical meaningful names
- **Code Walkthrough**: TODOs and hints at key positions
- **Result Analysis**: Interpretation from a doctor's perspective
- **Exercises**: Fill-in-the-blank and open-ended questions

### 2. Time Management

- Lecture + Practice time ≈ 30 minutes
- Lines of code: 50 ~ 120

### 3. Dual Versions

- **Student Version**: Contains TODO fill-in-the-blanks, suitable for classroom practice
- **Answer Version**: Complete code for teacher reference or self-study

## Topic Details

### 1. Data Processing & Clustering

Learn data cleaning, standardization, and K-Means clustering to automatically group heart disease patients into high and low risk groups.

**Key Concepts**:
- Data preprocessing (missing value handling, standardization)
- Unsupervised learning and clustering
- K-Means algorithm principles

### 2. Regression Analysis

Use linear regression to predict numerical diabetes progression values.

**Key Concepts**:
- Difference between regression and classification
- Linear regression principles
- Model evaluation (MSE, R²)

### 3. Classification

Build heart disease prediction models, comparing logistic regression, decision trees, random forests, SVM, and other algorithms.

**Key Concepts**:
- Nature of classification tasks
- Comparison of multiple classification algorithms
- Evaluation metrics (accuracy, precision, recall, F1, AUC)

### 4. Neural Networks

Use PyTorch to build simple Multi-Layer Perceptrons (MLP) for regression and classification tasks.

**Key Concepts**:
- Neural network fundamentals
- Forward and backward propagation
- PyTorch basics

### 5. Convolutional Neural Networks (CNN)

Learn CNN fundamentals applied to medical image classification tasks.

**Key Concepts**:
- Convolution and pooling operations
- CNN architecture design
- Image feature extraction

### 6. Large Language Models

Learn LLM API calls, prompt engineering, and extracting structured information from medical records.

**Key Concepts**:
- Token, Embedding, LLM principles
- Temperature, Top-p parameters
- System Prompt design
- RAG (Retrieval-Augmented Generation) concept

## Usage Recommendations

### For Teachers

1. Review the answer version before class
2. Use the student version for classroom teaching
3. Allow time for students to complete TODO exercises
4. Release answer version after class for review

### For Students

1. Study topics in order, as content builds progressively
2. Run complete code first, observe outputs
3. Attempt to complete TODO fill-in-the-blanks
4. Think through practice questions

### For Self-Learners

1. Study one topic at a time
2. Practice with student version first, then compare with answer version
3. Try modifying parameters to observe changes
4. Complete extension exercises to deepen understanding

## Datasets

| Dataset | Source | Usage |
|---------|--------|-------|
| heart.csv | Kaggle Heart Disease Dataset | Data Processing & Clustering / Classification |
| sklearn diabetes | sklearn built-in dataset | Regression / Neural Networks |

## Contributing

Contributions are welcome:

1. Fork this repository
2. Create a Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to Branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## Support

For questions or suggestions, please submit an [Issue](https://github.com/your-username/medical-ai-course/issues).


---

**Note**: This project is for educational purposes only. The models and predictions should not be used for actual medical decision-making.
