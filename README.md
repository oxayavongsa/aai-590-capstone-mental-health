# Mental Health Risk Predictor

This repository contains a machine learning pipeline and Gradio-based web interface for predicting mental health risk levels using various classification models. The project is part of a capstone assignment and leverages structured clinical and behavioral data to assess mental health risk categories: Low, Medium, and High.

## 🧠 Project Overview

The goal of this project is to explore and evaluate multiple classification models for multiclass mental health risk prediction. The models include:

- **Logistic Regression**
- **TabNet-Inspired Neural Network**
- **Soft Voting Ensemble**

Each model has been trained and evaluated using a cleaned and encoded version of the Mental Health Dataset. The evaluation metrics include Accuracy, F1-Score, AUC scores, and a confusion matrix to assess performance across risk categories.

---

## 📁 Project Structure

```
├── data-assets/                 # All CSV and PKL files for training/testing
│   ├── Mental Health Dataset.csv
│   ├── cleaned_mental_health_data.csv
│   ├── X_train.csv / X_test.csv
│   ├── y_train.csv / y_test.csv
│   └── Encoded + Scaled variants (.pkl / .csv)
│
├── images/                      # Visuals used for reporting and evaluation
│
├── notebook-pipeline/          
│   ├── models/
│   │   ├── logistic-regression/
│   │   │   └── logistic_regression_model.ipynb
│   │   ├── tab-neural-network/
│   │   │   └── tabular_neural_network_hypertuned.ipynb
│   │   └── soft-voting/
│   │       └── soft_voting_model.ipynb
│   ├── clean_filtered_eda.ipynb
│   └── split_preprocessing.ipynb
│
├── user-interface/
│   ├── mental_health_risk_predictor.ipynb         # Logistic/Ensemble UI
│   ├── mental_health_risk_predictor_TNN.ipynb     # TabNet Neural Net UI
│   └── gradio interface.pdf
│
└── README.md
```

---

## 🚀 How to Run

1. **Clone the Repository**
   ```bash
   git clone https://github.com/oxayavongsa/aai-590-capstone-mental-health.git
   cd aai-590-capstone-mental-health
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Notebooks**
   Launch any of the model training notebooks or the Gradio UI:
   - `notebook-pipeline/models/logistic-regression/logistic_regression_model.ipynb`
   - `notebook-pipeline/models/tab-neural-network/tabular_neural_network_hypertuned.ipynb`
   - `user-interface/mental_health_risk_predictor.ipynb` (for live predictions using Gradio)

---

## 📊 Model Performance Highlights

| Model                | Accuracy | Macro F1 | ROC AUC (Micro) | Generalization |
|---------------------|----------|----------|------------------|----------------|
| Logistic Regression | 0.73     | 0.73     | 0.84             | Good           |
| TabNet-Inspired     | 0.79     | 0.78     | 0.94             | Very Good      |
| Soft Voting         | 0.78     | 0.78     | 0.93             | Excellent      |

---

## 🎯 Key Features

- **Multiclass Classification** of mental health risks (Low, Medium, High)
- **Advanced Feature Engineering** using clinical and behavioral indicators
- **Interactive Gradio Interface** for real-time prediction
- **Model Interpretability** included with feature importance analysis

---

## 📌 Dependencies

See [`requirements.txt`](./requirements.txt) for a complete list.

---

## 📚 License

This project is licensed under the [MIT License](./LICENSE).

---

## 🙌 Acknowledgements

- This capstone was completed as part of the AAI-590 course.
- Credit to all contributors and team members involved in model development and UI implementation.