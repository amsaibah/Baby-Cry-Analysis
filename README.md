# 🍼 Baby Cry Sound Analysis Using Machine Learning

## 👶 Introduction

This project explores the classification of baby cries into emotional states such as **belly pain**, **burping**, **discomfort**, **hungry**, and **tired** using machine learning. The aim is to support caregivers and developers in building tools that respond more accurately to infant needs.

Since the dataset used is publicly available, I introduced **custom feature engineering**, **audio augmentation**, **model comparison**, and **explainability** to make this project original.

---

## 📂 Dataset

- **Source**: [DonateACry Dataset - Kaggle](https://www.kaggle.com/datasets/paultimothymooney/baby-cry)
- **Classes**: `belly_pain`, `burping`, `discomfort`, `hungry`, `tired`
- **Format**: WAV audio files
- **Challenge**: Difficult to collect original baby cry data

---

## 🧪 Feature Engineering

To enhance feature richness, I extracted:

- ✅ MFCCs (Mel-frequency cepstral coefficients)
- ✅ Delta MFCCs
- ✅ Delta-Delta MFCCs

These features helped capture time-based variations in the audio, providing more information to the model than MFCCs alone.

---

## 🔉 Audio Augmentation

To simulate real-world scenarios and improve model robustness, I used:

- ✅ **Time Shifting**
- ✅ **Pitch Shifting**
- ✅ **Noise Injection**

These were applied directly in the data loading pipeline to ensure diversity in training samples.

---

## ⚙️ Classification Models

I trained and compared the following classifiers:

| Classifier              | Status | Notes |
|-------------------------|--------|-------|
| Random Forest           | ✅     | Best performance |
| Support Vector Machine  | ✅     | Decent accuracy |
| K-Nearest Neighbors     | ✅     | Lower performance |
| Neural Network (MLP)    | ✅     | Competitive |

All models were evaluated using accuracy, precision, recall, F1-score, and confusion matrix.

---

## 📈 Evaluation

### Confusion Matrix
A confusion matrix was plotted to visually assess model performance across all classes, showing where misclassifications occurred.

### Performance Metrics

| Metric      | Value (Random Forest) |
|-------------|-----------------------|
| Accuracy    | 0.9563 (i.e., 95.63%) |

---

## 🧠 Explainability with SHAP

To interpret the model’s decisions, I used:

- ✅ **SHAP (SHapley Additive Explanations)**

It allowed me to visualize which features (MFCC coefficients) contributed the most to individual predictions, improving model transparency.

---

## ✅ What Makes This Project Unique?

| Enhancement                         | Included |
|-------------------------------------|----------|
| MFCC + Delta + Delta-Delta Features | ✅        |
| Audio Augmentation (Noise, Pitch, Shift) | ✅ |
| Multiple Classifier Comparison      | ✅        |
| SHAP Explainability                 | ✅        |

Despite using a Kaggle dataset, these additions make the project stand out as **original, well-engineered, and insightful**.

---

## 📌 Folder Structure

```bash
├── Baby_Cry_Analysis.ipynb    # Main Notebook
├── donateacry_corpus/         # Dataset (Kaggle)
├── images/                    # Plots and SHAP visuals
├── README.md                  # This blog
