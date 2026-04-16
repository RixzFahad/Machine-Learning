# 🤖 Machine Learning & Linear Regression Fundamentals

Welcome to the Machine Learning Introduction and Simple Linear Regression playground! This repository serves as a foundational guide to understanding core AI concepts and implementing a predictive model from scratch.

---

## 📖 Overview

Machine learning is a subset of artificial intelligence that allows systems to learn from data to make predictions and decisions, rather than relying on hard-coded rules. 

This project is divided into two main parts:
1.  **Theoretical Foundations:** A breakdown of ML terminology, workflows, and algorithms.
2.  **Practical Application:** Building a Simple Linear Regression model to predict student scores based on study hours.

---

## 🧠 Part 1: Machine Learning Basics

### 🔹 Learning Approaches
* **Supervised Learning:** Works with labeled data to predict outcomes.
* **Unsupervised Learning:** Finds hidden structures and patterns in unlabeled data.
* **Reinforcement Learning:** Learns optimal actions through a system of rewards.

### 🔹 The ML Pipeline
Building a robust model requires a systematic workflow:
1.  **Data Collection:** Gathering the dataset.
2.  **Data Cleaning:** Preparing and formatting the data.
3.  **Model Training:** The learning phase where the algorithm finds patterns.
4.  **Evaluation:** Testing the model's performance using metrics like Accuracy, Precision, Recall, and F1 score.
5.  **Deployment:** Putting the model into production.

### 🔹 Model Generalization
A core goal in ML is to build a balanced model that generalizes well to new data.
* **Overfitting:** The model memorizes the training data but fails completely on new, unseen data.
* **Underfitting:** The model is too simple and cannot learn the underlying patterns of the data.

---

## 📈 Part 2: Predicting Student Scores (Linear Regression)

### 🎯 Objective
To build a supervised Machine Learning model that predicts a student's percentage score based on the number of hours they studied.

### 🛠️ Data Preparation (Data Jar)
Before training, the data was thoroughly inspected and cleaned:
* **Dataset Structure:** The dataset consists of two numerical columns: `Hours` (float) and `Scores` (int), with exactly 25 rows and no categorical variables.
* **Quality Checks:** Verified that there are zero null values and zero duplicated rows.
* **Outlier Detection:** Calculated the Interquartile Range ($IQR = 4.7$) to find extreme values. With a Lower Limit of -4.35 and an Upper Limit of 14.45, it was confirmed that no outliers were present in the `Hours` feature.

### ⚙️ Model Building (Model Jar)
The algorithm relies on the mathematical concept of a straight line, represented as $Y = mx + c$.
* **Assumptions:** Visualizations and correlation matrices (0.976) confirmed a strong straight-line relationship between hours and scores, meaning no mathematical transformation of the data was required.
* **Data Splitting:** The data was divided using `train_test_split`, allocating 75% for training and 25% for testing.
* **Training:** Applied `sklearn.linear_model.LinearRegression` to fit the model to the training data.
* **Equation Components:** The model learned an intercept ($c$) of approximately 1.93 and a slope/coefficient ($m$) of roughly 9.94.

### 📊 Evaluation (Evaluation Jar)
* **Performance:** The model achieved an $R^2$ evaluation score of roughly 0.93.
* **Conclusion:** The Linear regression model predicts roughly 92% of values correctly. As a general rule, if a model's evaluation score is greater than 75%, it is considered a good model.

---

## 📦 Technologies & Libraries Used
The practical implementation relies on the following Python libraries:
* `pandas`
* `numpy`
* `matplotlib.pyplot`
* `seaborn`
* `scikit-learn` (`LinearRegression`, `train_test_split`, `metrics`)
