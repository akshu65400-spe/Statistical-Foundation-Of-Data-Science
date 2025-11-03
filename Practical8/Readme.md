# 🌳 Decision Tree Classifier — Pima Indians Diabetes Dataset

## 🎯 Objective

The purpose of this experiment is to **predict diabetes occurrence** among individuals using the **Decision Tree classification algorithm**.
By analyzing clinical features such as **Glucose**, **BMI**, and **Age**, the model determines which health indicators most strongly influence the likelihood of diabetes.
Both **Entropy (Information Gain)** and **Gini Index** approaches are explored to compare model behavior and justify the choice of the root feature.

---

## 📂 Dataset Overview

The **`diabetes.csv`** dataset includes medical details for female patients from the Pima Indian community, aged 21 years and above.
The task is to use these attributes to classify whether a person is **diabetic (1)** or **non-diabetic (0)**.

| Feature                      | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| **Pregnancies**              | Number of times pregnant                        |
| **Glucose**                  | Plasma glucose concentration after 2 hours      |
| **BloodPressure**            | Diastolic blood pressure (mm Hg)                |
| **SkinThickness**            | Triceps skin fold thickness (mm)                |
| **Insulin**                  | 2-hour serum insulin level (μU/ml)              |
| **BMI**                      | Body Mass Index (weight in kg / height in m²)   |
| **DiabetesPedigreeFunction** | Genetic predisposition score for diabetes       |
| **Age**                      | Age of the individual (in years)                |
| **Outcome**                  | Target variable — 0 (No Diabetes), 1 (Diabetic) |

---

## 🧠 Tools and Libraries

| Library                      | Usage                                               |
| ---------------------------- | --------------------------------------------------- |
| **Python (v3.x)**            | Programming environment                             |
| **pandas**                   | Data reading, exploration, and cleaning             |
| **NumPy**                    | Mathematical computations                           |
| **scikit-learn**             | Model creation, training, and evaluation            |
| **Matplotlib**               | Visualization of decision tree and feature insights |
| **Jupyter Notebook / Colab** | Interactive environment for code execution          |

---

## ⚙️ Workflow

### 1️⃣ Data Exploration

* The dataset was loaded using `pandas`.
* A summary of the data, including basic statistics and missing values, was reviewed.

### 2️⃣ Variable Identification

* **Input features:** All columns except `Outcome`
* **Target variable:** `Outcome`

### 3️⃣ Data Splitting

* The dataset was divided into **training** and **testing** subsets using `train_test_split`.

### 4️⃣ Model Development

* Two Decision Tree models were trained with different impurity criteria:

```python
dt_entropy = DecisionTreeClassifier(criterion='entropy', max_depth=3, random_state=42)
dt_gini = DecisionTreeClassifier(criterion='gini', max_depth=3, random_state=42)
```

### 5️⃣ Visualization

* The trees were visualized to interpret feature splits and understand how classification decisions were made.

### 6️⃣ Theoretical Validation

* Entropy, Information Gain, and Gini Index were calculated manually for the feature **Glucose** to confirm why it appeared as the most significant root node.

---

## 📈 Experimental Results

| Metric         | Root Feature | Accuracy | Observation                       |
| -------------- | ------------ | -------- | --------------------------------- |
| **Entropy**    | Glucose      | ~75%     | Produced maximum Information Gain |
| **Gini Index** | Glucose      | ~75%     | Showed highest impurity reduction |

* Both evaluation metrics identified **Glucose** as the most influential variable.
* **BMI** and **Age** contributed to secondary levels of decision-making within the tree.

---

## 📚 Core Formulas

### 🔸 Entropy

Measures uncertainty or randomness in a dataset.

[
Entropy = - \sum (p_i \times \log_2(p_i))
]

### 🔸 Gini Index

Quantifies the degree of impurity in the dataset.

[
Gini = 1 - \sum (p_i^2)
]

### 🔸 Information Gain

Represents the reduction in entropy after splitting.

[
IG = Entropy(parent) - \sum \left( \frac{n_{child}}{n_{total}} \times Entropy(child) \right)


## 🏁 Conclusion

This experiment highlighted the application of **Decision Tree Classifiers** using both **Entropy** and **Gini Index** as splitting criteria.
In both approaches, **Glucose** emerged as the most influential variable for predicting diabetes.

The main takeaways from this exercise include:

* Gaining hands-on experience in constructing and analyzing Decision Trees.
* Understanding how **Entropy**, **Information Gain**, and **Gini Index** determine the best feature for splitting data.
* Interpreting tree-based visualizations to enhance transparency and understanding of model decisions.

Overall, the Decision Tree algorithm proved to be a powerful and interpretable method for predicting health outcomes, offering clear insight into how various attributes influence the likelihood of diabetes.

