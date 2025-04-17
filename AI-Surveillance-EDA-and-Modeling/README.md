# Global AI Surveillance Trends – Predictive Analysis

This project was developed as part of the **"Ethics and Regulations of Artificial Intelligence"** course of my Master’s in Applied Data Science and AI at OPIT.  
It analyzes the adoption of AI and big data surveillance technologies across countries using the **AI & Big Data Global Surveillance Index** dataset.

With a background in international policies and a personal interest in geopolitics and ethics, this project allowed me to explore the intersection between digital technologies, regime types, and civil liberties from both a technical and societal perspective.

## Objectives

The notebook fulfills three core objectives:
- Explore patterns in the global deployment of surveillance technologies (EDA)
- Predict the adoption of **social media surveillance** based on key governance and economic features
- Identify the **most influential predictors** using Random Forest and feature importance analysis

## Technologies Used

- Python (Jupyter Notebook)
- Pandas, Matplotlib, Seaborn
- scikit-learn
- SHAP (initial attempts)
- Google Colab

## Dataset

The dataset used is the [AI & Big Data Global Surveillance Index](https://data.mendeley.com/datasets/gjhf5y4xjp/1) by Carnegie Endowment for International Peace.  
It documents the presence of surveillance technologies in 77 countries from 2012–2020, along with regime type, internet freedom scores, military expenditure, and vendor origin.

## How to Use

1. Open the notebook in Jupyter or Google Colab.
2. Upload the dataset file `AI & Big Data Global Surveillance Index.csv` before executing any cells.
3. Run all cells in order.

## Modeling Approach

- Two models were implemented:
  - **Logistic Regression** for baseline performance
  - **Random Forest** with expanded feature set and hyperparameter tuning
- Evaluation metrics include accuracy, precision, recall, and F1-score
- Final insights were derived using `.feature_importances_` to assess which variables most impacted the model's decisions

## Key Findings

- Countries with higher **surveillance intensity**, **military expenditure**, and **lower democracy scores** were more likely to adopt social media surveillance.
- **Vendor origin** (China vs. US) had limited predictive power despite its geopolitical significance.
- More features did not always improve performance — highlighting the importance of **feature quality over quantity**.

## Author

Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)