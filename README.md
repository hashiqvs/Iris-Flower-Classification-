# Iris Flower Species Classification

## Project Objective
The goal of this assessment is to apply supervised learning techniques to classify Iris flowers into three species: **Setosa**, **Versicolor**, and **Virginica**. The project involves a full pipeline including data preprocessing, Exploratory Data Analysis (EDA), and a comparative study of three classification algorithms.

## 1. Data Loading and Preprocessing
The dataset used is the built-in Iris dataset from `sklearn`.

### Steps Performed:
* **Loading:** Data was imported and converted into a structured format for analysis.
* **Missing Value Check:** Verified that there are no null entries, ensuring data quality.
* **Cleaning & Handling Duplicates:** Removed any redundant entries to prevent bias in the model.
* **Outlier Detection:** Used Z-scores and visualizations to identify data points that deviate significantly from the norm.
* **Feature Scaling:** Applied `StandardScaler` to normalize measurements, which is critical for distance-based models like k-NN.

## 2. Exploratory Data Analysis (EDA)
EDA was performed to understand the relationships and distributions within the features:
* **Pairplots:** Visualized pairwise relationships; this revealed that Petal Length and Petal Width are the strongest indicators for species separation.
* **Boxplots:** Used to observe the spread of data and identify outliers in features like Sepal Width.
* **Skewness Check:** Analyzed the distribution of each feature to ensure the data is suitable for linear modeling.
* **Correlation Heatmap:** Used to find high-correlation features that impact the classification performance.

## 3. Model Building
I implemented three distinct algorithms to compare their predictive power:

| Algorithm | How it Works | Why it is Used |
| :--- | :--- | :--- |
| **Logistic Regression** | Models the probability of class membership using a sigmoid function. | Highly efficient and works exceptionally well when classes are linearly separable. |
| **Decision Tree** | Splits the data into branches based on feature thresholds to create a "decision map." | Excellent for interpretability and identifying which specific measurements (like Petal Length) matter most. |
| **K-Nearest Neighbors** | Predicts the label of a point based on the majority class of its 'k' closest neighbors. | Ideal for this dataset as similar flower species tend to cluster together geographically. |

## 4. Model Evaluation
Models were evaluated using a 20/80 test-train split.

* **Accuracy Score:** Measures the overall correctness of the model.
* **Confusion Matrix:** Provides a breakdown of correct vs. incorrect classifications for each specific species.
* **Best Performer:** Based on the results, **Logistic Regression/k-NN** achieved near-perfect accuracy, proving to be the most robust for this dataset.

## 5. Conclusion
In simple words, this project demonstrates that we can identify flower species with extremely high accuracy using just four physical measurements. The analysis showed that **petal measurements** are far more useful than sepal measurements for distinguishing between species. By combining clean data, thorough exploration, and the right algorithms, we built a model that can reliably assist in biological classification.

---
