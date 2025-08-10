# Mental Health Risk Predictor

[![Watch Presentation](https://img.shields.io/badge/Watch-YouTube-red)](https://youtu.be/VCkYcj3GoHY)
[![Dataset (Kaggle)](https://img.shields.io/badge/Dataset-Kaggle-blue)](https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset)

---

This repository contains a machine learning pipeline and Gradio-based web interface for predicting mental health risk levels using various classification models. The project is part of a capstone assignment and leverages structured clinical and behavioral data to assess mental health risk categories: Low, Medium, and High.

## 🧠 Project Overview

We evaluate three classification approaches for multiclass risk prediction:

- **Logistic Regression** — interpretable baseline  
- **TabNet-inspired Tabular Neural Network** — non-linear pattern learning  
- **Soft Voting Ensemble** — stability via averaged probabilities

Key metrics include Accuracy, Macro F1, and ROC AUC. An interactive **Gradio** UI provides live predictions for demo purposes.

---

## 📁 Project Structure

```
├── data-assets/                                      # CSV and PKL files for training/testing
│   ├── Mental Health Dataset.csv
│   ├── cleaned_mental_health_data.csv
│   ├── X_train.csv / X_test.csv
│   ├── y_train.csv / y_test.csv
│   └── Encoded + Scaled variants (.pkl / .csv)
│
├── images/                                           # Visuals used for reporting and evaluation
│
├── notebook-pipeline/                                # Pipeline Order          
│   ├── clean_filtered_eda.ipynb
│   ├── split_preprocessing.ipynb
│   └── models/
│       ├── logistic-regression/
│       │   └── logistic_regression_model.ipynb
│       ├── tab-neural-network/
│       │   └── tabular_neural_network_hypertuned.ipynb
│       └── soft-voting/
│            └── soft_voting_model.ipynb
│
├── user-interface/
│   ├── mental_health_risk_predictor_logistic.ipynb    # Logistic/Ensemble UI
│   ├── mental_health_risk_predictor_TNN.ipynb         # TabNet Neural Net UI
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

3. **Run Notebooks**<br>
   Launch any of the model training notebooks:
   - `notebook-pipeline/models/logistic-regression/logistic_regression_model.ipynb` [![Open in Colab — Logistic Regression](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/oxayavongsa/aai-590-capstone-mental-health/blob/main/notebook-pipeline/models/logistic-regression/logistic_regression_model.ipynb "Open in Colab: Logistic Regression notebook")
   - `notebook-pipeline/models/soft-voting/soft_voting_model.ipynb`[![Open In Colab - Soft Voting](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/oxayavongsa/aai-590-capstone-mental-health/blob/main/notebook-pipeline/models/soft-voting/soft_voting_model.ipynb)
   - `notebook-pipeline/models/tab-neural-network/tabular_neural_network_hypertuned.ipynb` [![Open In Colab - TabNet](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/oxayavongsa/aai-590-capstone-mental-health/blob/main/notebook-pipeline/models/tab-neural-network/tabular_neural_network_hypertuned.ipynb)

   **Launch the demo Gradio** [![Watch Presentation](https://img.shields.io/badge/Watch-YouTube-red)](https://youtu.be/VCkYcj3GoHY?t=473)<br>
   Run one of the UI notebooks:
   - `user-interface/mental_health_risk_predictor_logistic.ipynb` 
   - `user-interface/mental_health_risk_predictor_TNN.ipynb`

---

## 📊 Model Performance Highlights

| Model                | Accuracy | Macro F1 | ROC AUC (Micro) | Generalization |
|---------------------|----------|----------|------------------|----------------|
| Logistic Regression | 0.73     | 0.73     | 0.84             | Good           |
| Soft Voting         | 0.78     | 0.78     | 0.93             | Very Good      |
| TabNet-Inspired     | 0.79     | 0.78     | 0.94             | Excellent      |

---

## 🎯 Key Features

- **Multiclass Classification** of mental health risks (Low, Medium, High)
- **Advanced Feature Engineering** using clinical and behavioral indicators
- **Interactive Gradio Interface** for real-time prediction
- **Model Interpretability** included with feature importance analysis

---

## Ethics & Intended Use
Ethics & intended use
All examples use **anonymous** data. The system supports professional judgment and should not be used to make medical diagnoses. For any real deployment, use informed consent, privacy safeguards, access control, and bias monitoring.

---

## 📌 Dependencies

See [`requirements.txt`](./requirements.txt) for a complete list.

---

## 📚 License

This project is licensed under the [Apache License](./LICENSE).

---

## 🙌 Acknowledgements

- This capstone was completed as part of the AAI-590 course.
- Credit to all contributors and team members involved in model development and UI implementation.
