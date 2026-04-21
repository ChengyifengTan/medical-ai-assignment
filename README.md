# Medical AI Course - Hands-on Practice Notebooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

**医学人工智能课程随堂实践 Notebook 教学材料** | Medical AI Course Hands-on Practice Materials

本项目为《医学人工智能》课程设计的教学友好型 Jupyter Notebook 随堂实践脚本，主要面向无编程背景或编程基础较弱的医学生。

## 项目简介

本仓库包含一系列精心设计的 Jupyter Notebook，涵盖从数据处理到深度学习的医学人工智能核心内容。每个 Notebook 都以真实或拟真的医学场景为背景，通过案例驱动的方式帮助学生建立直观理解。

### 设计理念

- **通俗易懂 > 数学严谨**：避免复杂公式推导，使用类比和直觉解释
- **案例驱动 > 抽象理论**：以医学应用场景切入，增强学习动机
- **逐步引导 > 一步到位**：分步骤讲解，防止学生跟不上
- **可运行 > 复杂最优**：代码简洁易懂，确保学生能成功运行

### 教学对象

- 医学生（无编程背景或编程基础弱）
- 医学研究人员希望了解 AI 基础
- 对医学 AI 感兴趣的初学者

## 课程内容

| 序号 | 主题 | 内容概述 | 医学应用场景 |
|------|------|----------|--------------|
| 1 | 数据预处理与聚类 | 数据清洗、标准化、K-Means 聚类 | 患者分群（高风险/低风险） |
| 2 | 回归分析 | 线性回归、模型评估 | 糖尿病病情进展预测 |
| 3 | 分类算法 | 逻辑回归、决策树、随机森林、SVM | 心脏病预测模型 |
| 4 | 神经网络 | PyTorch 基础、MLP、训练流程 | 糖尿病风险分类 |
| 5 | 卷积神经网络 (CNN) | CNN 原理、图像分类 | 医学影像诊断 |
| 6 | 大语言模型 | API 调用、Prompt 工程、信息提取 | 病历文本结构化 |

## 项目结构

```
final/
├── README.md                                    # 项目说明文档
├── CLAUDE.md                                    # 课程设计指南
├── 1_Data_Processing_and_Clustering/            # 数据预处理与聚类
│   ├── data_process_and_cluster.ipynb                   # 学生练习版
│   ├── data_process_and_cluster_answer.ipynb            # 教师参考版
│   └── heart.csv                                        # 心脏病数据集
├── 2_Regression/                                # 回归分析
│   ├── regression.ipynb                                  # 学生练习版
│   └── regression_answer.ipynb                           # 教师参考版
├── 3_Classification/                            # 分类算法
│   ├── classification.ipynb                              # 学生练习版
│   ├── classification_answer.ipynb                       # 教师参考版
│   └── heart.csv                                        # 心脏病数据集
├── 4_Neural_Network/                            # 神经网络
│   ├── neural_network.ipynb                              # 学生练习版
│   └── neural_network_answer.ipynb                       # 教师参考版
├── 5_CNN/                                       # 卷积神经网络
│   ├── CNN_classification.ipynb                          # 学生练习版
│   └── CNN_classification_answer.ipynb                   # 教师参考版
└── 6_LLM_Application/                           # 大语言模型应用
    ├── 大模型在医学中的应用入门.ipynb                     # 大模型应用入门
    ├── 糖尿病诊断.md                                    # 参考资料
    ├── 中国糖尿病流行的影响因素.md                       # 参考资料
    ├── 中国糖尿病防治指南（2024版）- 节选.md             # 参考资料
    ├── 中国糖尿病防治指南（2024版）.md                   # 参考资料
    └── 病例结构化结果.csv                               # 示例输出
```

## 快速开始

### 环境要求

- Python 3.8+
- Jupyter Notebook / Jupyter Lab

### 安装步骤

1. **克隆仓库**

```bash
git clone https://github.com/your-username/medical-ai-course.git
cd medical-ai-course/final
```

2. **创建虚拟环境（推荐）**

```bash
conda create -n aimedicine python=3.9
conda activate aimedicine
```

3. **安装依赖**

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
pip install jupyter

# 神经网络需要安装 PyTorch
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

# 大模型应用需要安装
pip install openai python-dotenv
```

4. **启动 Jupyter Notebook**

```bash
jupyter notebook
```

### 大模型应用特别说明

大模型实践需要 API Key：

1. 注册并获取 API Key（推荐使用硅基流动 SiliconFlow）
2. 在 `6_LLM_Application/` 目录下创建 `.env` 文件
3. 填入以下内容：

```
OPENAI_API_KEY=your_api_key_here
BASE_URL=https://api.siliconflow.cn/v1
```

**注意**：请勿将真实的 API Key 提交到公开仓库！

## Notebook 特点

### 1. 教学友好的结构

每个 Notebook 都包含：

- **医学背景引入**：真实或拟真的医学应用场景
- **方法原理讲解**：使用类比和直觉解释，避免复杂公式
- **数据准备**：医学意义命名的数据字段
- **核心代码讲解**：关键位置的 TODO 和提示
- **结果分析**：医生视角的结果解释
- **小练习**：填空题和思考题

### 2. 时间控制

- 讲解 + 实践时间 ≈ 30 分钟
- 代码量：50 ~ 120 行

### 3. 双版本提供

- **学生版**：包含 TODO 填空，适合课堂练习
- **答案版**：完整代码，供教师参考或学生自学

## 各主题内容详解

### 1. 数据预处理与聚类

学习数据清洗、标准化、K-Means 聚类，将心脏病患者自动分为高风险和低风险组。

**核心概念**：
- 数据预处理（缺失值处理、标准化）
- 无监督学习与聚类
- K-Means 算法原理

### 2. 回归分析

使用线性回归预测糖尿病患者的病情进展数值。

**核心概念**：
- 回归 vs 分类的区别
- 线性回归原理
- 模型评估（MSE、R²）

### 3. 分类算法

构建心脏病预测模型，对比逻辑回归、决策树、随机森林、SVM 等算法。

**核心概念**：
- 分类任务的本质
- 多种分类算法对比
- 评估指标（准确率、精确率、召回率、F1、AUC）

### 4. 神经网络

使用 PyTorch 构建简单的多层感知机（MLP），完成回归和分类任务。

**核心概念**：
- 神经网络基本原理
- 前向传播与反向传播
- PyTorch 基础用法

### 5. 卷积神经网络 (CNN)

学习 CNN 基本原理，应用于医学影像分类任务。

**核心概念**：
- 卷积、池化操作
- CNN 结构设计
- 图像特征提取

### 6. 大语言模型

学习大模型 API 调用、Prompt 工程、从病历文本中提取结构化信息。

**核心概念**：
- Token、Embedding、LLM 原理
- Temperature、Top-p 等参数
- System Prompt 设计
- RAG（检索增强生成）概念

## 使用建议

### 教师使用

1. 课前阅读答案版 Notebook，熟悉代码流程
2. 课堂使用学生版 Notebook 进行教学
3. 留出时间让学生完成 TODO 练习
4. 课后发布答案版供学生复习

### 学生使用

1. 按主题顺序学习，内容有递进关系
2. 先运行完整代码，观察输出结果
3. 尝试完成 TODO 填空
4. 思考课后练习题

### 自学者使用

1. 建议每阶段学习一个主题
2. 先学生版练习，再看答案版对照
3. 尝试修改参数，观察结果变化
4. 完成扩展练习，加深理解

## 数据集说明

| 数据集 | 来源 | 用途 |
|--------|------|------|
| heart.csv | Kaggle Heart Disease Dataset | 数据预处理与聚类 / 分类 |
| sklearn diabetes | sklearn 自带数据集 | 回归 / 神经网络 |

## 贡献指南

欢迎对本项目提出建议或贡献代码：

1. Fork 本仓库
2. 创建新的 Feature Branch (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到 Branch (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 技术支持

如有问题或建议，欢迎提交 [Issue](https://github.com/your-username/medical-ai-course/issues)。


---

**注意**：本项目仅用于教学目的，相关模型和预测结果不应作为实际医疗决策的依据。
