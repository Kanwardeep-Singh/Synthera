# 🧠 Synthera: Generative AI for Synthetic Tabular Data

## 🚀 Introduction
Welcome! 👋 **Synthera** is a project focused on generating high-quality synthetic tabular datasets using generative AI. It explores how synthetic data can be used to train privacy-aware machine learning models and investigates fairness and bias in comparison to real data. We also integrate Hugging Face Transformer models — like BERT, RoBERTa, and DistilBERT — to evaluate model performance across real and synthetic datasets.

## 📁 Project Structure

```
📁 Synthera
├── generate_data.py # Script to create synthetic tabular data
├── privacy_preserving.py # Train models using differential privacy techniques
├── bias_detection.py # Detect fairness issues and evaluate distributional shifts
├── huggingface_integration.py # Fine-tune Hugging Face models on real and synthetic data
├── requirements.txt # Required dependencies and libraries
├── real_data.csv # Original dataset
├── synthetic_data.csv # Generated synthetic dataset
├── README.md # Project documentation
```

## 🔧 Setup Instructions
First things first, get your environment ready:
```bash
pip install -r requirements.txt
```
You’ll need packages like `SDV`, `Opacus`, `FairLearn`, and `transformers`. Make sure they install properly.

## 📌 Usage Guide
Each script in Synthera is modular. Run them independently or chain them together:

### 1. Generate Synthetic Data
```bash
python generate_data.py
```
This will generate `synthetic_data.csv` based on the structure and distribution of your original dataset.

### 2. Train with Differential Privacy
```bash
python privacy_preserving.py
```
This trains a neural network model with differential privacy, producing a privacy-aware model artifact.

### 3. Perform Fairness & Bias Checks
```bash
python bias_detection.py
```
This evaluates the similarity between real and synthetic data, and checks for biases using fairness metrics like demographic parity.

### 4. Evaluate with Hugging Face Models
```bash
python huggingface_integration.py
```
This script compares model performance (`BERT`, `RoBERTa`, `DistilBERT`) across real vs. synthetic datasets to assess data fidelity and model generalizability.

## 📊 Evaluation Results
| Model      | Accuracy on Real Data               | Accuracy on Synthetic Data |
|------------|--------------------|-------------------------|
| BERT       | 0.47               | 0.522                   |
| RoBERTa    | 0.47               | 0.522                   |
| DistilBERT | 0.53               | 0.478                   |

While DistilBERT performs better on real data, BERT and RoBERTa show improved performance on synthetic data. The results suggest synthetic data has strong potential when used correctly.

## 💡 Future Enhancements
- Experiment with advanced model architectures
- Extend bias analysis with additional fairness metrics
- Compare private vs. non-private training pipelines
- Integrate the process into an end-to-end automated workflow


