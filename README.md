# 🚢 Titanic Survival Prediction with Decision Trees

<p align="center">
  <img src="assets/titanic.gif" width="650">
</p>

> **Could a machine learning model learn who was more likely to survive the Titanic disaster?**

This project builds an interpretable **Decision Tree Classifier** to predict passenger survival using demographic, socioeconomic, and travel-related features from the Titanic dataset.

Rather than treating the model as a black box, the project visualizes the learned decision tree to show **how passenger characteristics lead to different survival predictions.**

---

## 🎯 Project Objective

Predict whether a Titanic passenger survived:

- **0 — Not Survived**
- **1 — Survived**

using features such as:

- Passenger class (`Pclass`)
- Sex
- Age
- Fare
- Number of siblings/spouses (`SibSp`)
- Number of parents/children (`Parch`)
- Port of embarkation (`Embarked`)

---

## 🧹 Data Preparation

Real-world datasets are rarely clean.

The preprocessing workflow includes:

- Detecting missing values
- Median imputation for missing `Age`
- Mode imputation for missing `Embarked`
- Removing `Cabin` due to extensive missingness
- One-hot encoding categorical variables
- Train/test splitting for model evaluation

---

## 🌳 Model

The project uses:

`DecisionTreeClassifier`

The tree depth is constrained to improve interpretability and reduce model complexity:

`max_depth = 3`

One major advantage of a Decision Tree is its **interpretability**: every prediction can be traced through a sequence of human-readable decisions.

---

## 🌳 What Did the Tree Learn?

The first split learned by the model is based on **sex**, indicating that this feature provides the strongest initial separation in the fitted tree.

From there, the model considers features including:

`Pclass → Age → Fare → SibSp`

to create increasingly specific passenger groups and ultimately predict survival.

---

## 🛠 Tech Stack

- Python
- Pandas
- Scikit-learn
- Matplotlib

---

## 📁 Repository Structure

titanic-survival-decision-tree/
│
├── assets/
│   ├── titanic.gif
│   └── decision_tree.png
│
├── data/
│   └── titanic.csv
│
├── notebooks/
│   └── titanic_decision_tree.ipynb
│
├── README.md
└── requirements.txt

#Created By Mohammad Hossein Darzi
