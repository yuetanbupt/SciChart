# 📊 SciChart
## 👋 Introduction

Charts play a pivotal role in scientific research, offering a concise and visual way to present complex data. For Multimodal Large Language Models (MLLMs), the ability to comprehend charts is critical, as it requires both visual perception and reasoning that bridges graphical and textual information. Chart Question Answering (Chart QA) serves as a specialized application of Information Retrieval (IR), where the goal is to extract relevant insights from visual data representations contextually. However, existing Chart QA datasets are monolingual with simple questions, making current evaluation benchmarks inadequate for the rapid advancements in MLLM performance. Therefore, we propose a multilingual scientific spectral Chart QA dataset, termed SciChart. We design two tasks, basic question answering (BasicQA) and reasoning-based question answering (ReaQA), to evaluate the models' ability to 1) directly extract information from charts, and 2) understand the textual and visual information for reasoning. We build 1,100 ReaQA and over 10,000 BasicQA samples. All samples are manually curated and annotated by human experts. We also conduct extensive experiments with state-of-the-art models to establish SciChart benchmarks. Experimental results show a huge gap between the performance of existing models (GPT-4o 44.68%) and humans (83.84%). Further retrieval-augmented generation experiment shows the RAG-based GPT-4o model only has marginal improvements in the ReaQA task, with challenges in retrieving relevant chart features for complex reasoning. Language differences also impact performance, highlighting the need for better multilingual reasoning.

<div align=center>
<img src="example_image/charts.png">
</div>

<div align=center>
<img src="example_image/examples.png" >
</div>

## Image Data
Please download image data to **data/img** from link: https://drive.google.com/file/d/1M3kzYqLK26KLHJIeHx9EjdhId-RFvUig/view?usp=drive_link

## Requirements
* Python 3.8+
* PyTorch 2.0+
* CUDA 11.4+ (★ Required for GPU acceleration)
* API for GPT services
<br>

## 🛠️ Quick Start
### 1. Environment Setup
```bash
# Install dependencies
pip install -r requirements.txt

# Set API key (in ~/.bashrc or system environment)
export API_KEY="your_api_key_here"
```
### 2. Main Module
#### 2.1 Chart Question Answering (Proprietary Models)
```bash
python API.py
```
**Workflow:**  
1. Select dataset from **data/**  
2. Configure task-specific instructions in instructions.py
3. Modify the API in designated configuration section
4. Results output to **output/**
#### 2.2 GPT-acc Evaluation
```bash
python eval_gptacc.py
```
**Workflow:**  
1. Select dataset from **output/** when conducted
2. Evaluation results are displayed directly and saved
#### 2.3 Relaxed-acc Evaluation
```bash
python eval_relaxedacc.py
```
**Workflow:** 
1. Select dataset from **output/** when conducted
2. Evaluation results are displayed directly and saved
#### 2.4 instructions
```bash
vim instructions.py
```

## Contact Us

Email to yuetan@pku.edu.cn
