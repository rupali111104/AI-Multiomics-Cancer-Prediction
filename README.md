# 🧬 AI Multi-Omics Cancer Prediction

## Overview

This project presents an AI-based framework for cancer prediction using multi-omics biological data. It integrates genomic, RNA expression, mutation, and clinical information to improve cancer outcome prediction using machine learning and deep learning techniques.

## Features

- **Multi-omics data integration** (RNA, Mutations, Clinical data)
- **Data preprocessing and feature selection**
- **Random Forest baseline model**
- **Deep Encoder Network**
- **Attention-based Fusion Network**
- **Graph Neural Network (GNN)**
- **Cancer survival prediction and evaluation**

## Tech Stack

- Python
- Pandas & NumPy
- Scikit-learn
- PyTorch & PyTorch Geometric
- Matplotlib & Seaborn
- Jupyter Notebook

## Project Workflow

```
Raw Multi-Omics Data
        ↓
Data Preprocessing (Quality Control, Missing Value Imputation)
        ↓
Feature Extraction & Embedding
        ↓
Attention-Based Fusion Layer (Cross-Omics Attention)
        ↓
Graph Neural Network (GNN)
        ↓
Cancer Prediction & Classification
```

## Model Architecture

The project implements multiple deep learning models:

### 1. **Random Forest Classifier**
- Baseline model for comparison
- Accuracy: ~95%

### 2. **Deep Encoder Network**
- 3-layer encoder: 1024 → 512 → 256 dimensions
- Classification head for binary output
- Accuracy: ~98%

### 3. **Attention-Based Fusion Network**
- Separate RNA and Mutation encoders
- Cross-omics attention mechanism
- Feature fusion with softmax attention weights
- Accuracy: ~80.4%

### 4. **Graph Neural Network (GNN)**
- GCN layers for feature propagation
- Graph-based feature interaction learning
- Pathway and biomarker learning
- Accuracy: ~80.5%

## Results

- **Model Comparison**: Random Forest (95%), Encoder (98%), Attention (80.4%), GNN (80.5%)
- **Confusion Matrix**: Detailed True Positives, True Negatives, False Positives, False Negatives
- **Training Accuracy**: Stable convergence over 100 epochs
- **Training Loss**: Decreasing loss trajectory
- **Feature Correlation Heatmap**: Top 50 features analysis

## Repository Structure

```
AI-Multiomics-Cancer-Prediction/
│
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── LICENSE                            # MIT License
│
├── src/
│   ├── ai_model_for_cancer_prediction.py      # Model implementations
│   └── multiomics_full_pipeline.py            # Data preprocessing pipeline
│
└── images/
    ├── architecture.png               # Project architecture diagram
    ├── confusion_matrix.png           # Model evaluation confusion matrix
    ├── training_accuracy.png          # Training accuracy curve
    ├── training_loss.png              # Training loss curve
    └── feature_correlation.png        # Feature correlation heatmap
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/rupali111104/AI-Multiomics-Cancer-Prediction.git
cd AI-Multiomics-Cancer-Prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run notebooks in Jupyter:
```bash
jupyter notebook
```

## Usage

### Data Preprocessing
Run the preprocessing pipeline:
```python
python src/multiomics_full_pipeline.py
```

### Model Training
Run the model training script:
```python
python src/ai_model_for_cancer_prediction.py
```

## Key Findings

1. **Data Integration**: Successfully merged RNA expression, mutation, and clinical data
2. **Feature Selection**: Selected top 500 RNA features and 500 mutation features by variance
3. **Model Performance**: Encoder network achieved 98% accuracy on test set
4. **Attention Mechanism**: Successfully learned cross-omics feature interactions
5. **GNN Learning**: Graph-based models effectively capture biomarker relationships

## Future Improvements

- [ ] Implement Transformer-based models
- [ ] Add Explainable AI (SHAP/LIME) for feature interpretation
- [ ] Deploy web interface with Streamlit
- [ ] Perform hyperparameter optimization with Optuna
- [ ] Add cross-validation and ensemble methods
- [ ] Implement survival analysis with Cox regression
- [ ] Create real-time prediction API

## References

- Multi-omics data integration in cancer genomics
- Attention mechanisms in deep learning
- Graph Neural Networks for biological networks
- PyTorch and PyTorch Geometric documentation

## License

MIT License - See LICENSE file for details

## Author

**Rupa Kandimalla**

---

**Last Updated**: 2026-07-03
