# Classification Model Comparison

## 📝 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset Description](#-dataset-description)
- [Model Comparison](#-model-comparison)
- [Performance Metrics](#-performance-metrics)
- [Installation Guide](#-installation-guide)
- [Results Visualization](#-results-visualization)
- [Model Selection Strategy](#-model-selection-strategy)
- [License](#-license)
- [Contact Information](#-contact-information)

## 🌟 Project Overview
This project compares the performance of three classification algorithms on music genre prediction. The implemented models achieve up to **97.5% accuracy** on test data, demonstrating effective genre classification capabilities.

## 🚀 Key Features
- Comprehensive data preprocessing 
- StandardScaler feature normalization
- Cross-validation implementation
- Multiple classifier comparison
- Visual performance analysis

## 📊 Dataset Description
**File:** `music_clean.csv`  
**Samples:** 7 (sample shown)  
**Features:** 12 audio characteristics + genre label  

| Feature | Description | Range |
|---------|-------------|-------|
| `popularity` | Track popularity score | 0-100 |
| `acousticness` | Confidence measure of acoustic sound | 0.0-1.0 |
| `danceability` | Suitability for dancing | 0.0-1.0 |
| `duration_ms` | Track length in milliseconds | >0 |
| `energy` | Perceived intensity/activity | 0.0-1.0 |
| `instrumentalness` | Presence of vocal content | 0.0-1.0 |
| `liveness` | Presence of live audience | 0.0-1.0 |
| `loudness` | Overall loudness (dB) | -60-0 |
| `speechiness` | Presence of spoken words | 0.0-1.0 |
| `tempo` | Estimated beats per minute | >0 |
| `valence` | Musical positiveness | 0.0-1.0 |
| `genre` | Target classification label | Categorical |

## 🧠 Model Comparison
### Implemented Algorithms:
| Model | Type | Parameters |
|-------|------|------------|
| Logistic Regression | Linear | Default sklearn params |
| KNN | Instance-based | n_neighbors=5 |
| Decision Tree | Tree-based | Gini impurity, depth=None |

## 📈 Performance Metrics

### Model Evaluation Matrix
| Model | CV Accuracy (Mean) | Test Accuracy |
|-------|--------------------|---------------|
| Logistic Regression | 93% | 86% |
| KNN | 92% | 86% |
| Decision Tree | 100% | 97.5% |

## 📥 Installation Guide
1. Clone repository:
```bash
git clone https://github.com/barisgudul/Classification-Model-Selection.git
cd Classification-Model-Selection
```
2. Launch Jupyter:
```bash
jupyter notebook "Classification Model Comparison/main.ipynb"
```

## 📊 Results Visualization

### Cross-Validation Accuracy Distribution
![Cross-Validation Boxplot](Classification%20Model%20Comparison/boxplot.png)  
*Visual comparison of model stability across 6 folds - Decision Tree shows perfect consistency*

### Test Set Performance Comparison  
![Test Accuracy](Classification%20Model%20Comparison/barplot.png)  
*Final evaluation metrics comparison - Decision Tree achieves 97.5% test accuracy*

## 🔍 Critical Insights

### Model Behavior Analysis
- **Decision Tree Dominance**  
  🚩 Perfect 100% cross-validation accuracy suggests:  
  - Potential overfitting to training data  
  - High variance in model structure  
  - Possible need for pruning/regularization

- **Algorithm Consistency**  
  ✅ Stable performers:  
  - **KNN**: 92% → 86% (CV → Test)
  - **Logistic Regression**: 93% → 86%  
  - Minimal performance drop indicates good generalization
  - 

## 📚 Model Selection Strategy

| Algorithm Type       | Representative Model | Rationale                      | Key Characteristics                   |
|----------------------|----------------------|--------------------------------|---------------------------------------|
| 🧪 Linear Classifier  | Logistic Regression  | Baseline performance measurement | - Linear decision boundaries          |
| 🔎 Instance-Based     | KNN (k=5)            | Local pattern capture          | - Distance-based similarity           |
| 🌳 Non-Parametric     | Decision Tree        | Complex relationship modeling  | - Feature importance analysis         |


## 📄 License

**MIT License**  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Permissions:**  
✅ Free academic/research use  
✅ Modification and redistribution  
❌ Commercial use requires written consent  

Full license terms available in [LICENSE](LICENSE) file.

---

## 📧 Contact Information

**Project Maintainer**  
[![Author Badge](https://img.shields.io/badge/Author-barisgudul-blue.svg)]()  
[![Email](https://img.shields.io/badge/Email-mehmetbarisgudul@gmail.com-red.svg)](mailto:mehmetbarisgudul@gmail.com)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-informational.svg)](https://linkedin.com/in/mehmet-baris-gudul-1101bg)

**Contribution Guidelines:**  
We welcome collaborations! Please reach out via email before submitting PRs.
