🎓 Teachers Rating Dataset Analysis
🧭 Objective

The aim of this practical is to explore relationships and differences within the Teachers’ Rating Dataset using regression analysis, ANOVA, and correlation tests.

These analyses help determine how factors such as gender, beauty, and age influence teaching evaluation scores and perceptions. All statistical methods were implemented in Python using the statsmodels library for quantitative interpretation.

📊 Dataset Description

The dataset (teachers_rating_data (1).csv) contains data about university professors and their corresponding teaching evaluation ratings. It includes demographic and professional details of instructors.

Column	Description
prof	Professor’s unique identifier
Gender	Gender of the professor (Male/Female)
Age	Age of the professor in years
Tenure	Indicates whether the professor is tenured (Yes/No)
Evaluation	Teaching evaluation score given by students
Students	Number of students who rated the professor
Beauty	Numerical score representing the perceived beauty of the professor
CourseLevel	Course type — lower or upper division
🧰 Tools & Libraries Used
Tool/Library	Purpose
Python (v3.x)	Programming environment
pandas	Data manipulation and preprocessing
statsmodels	Regression, T-test, and ANOVA analysis
scipy	Statistical hypothesis testing
Google Colab	Code execution and visualization environment
🧾 Results Summary

Statistical analyses were performed to answer three key questions, using a significance level of p < 0.05.

1️⃣ Gender & Evaluation (Regression T-test)

Question: Does gender affect teaching evaluation scores?

Model Output: F(1,198) = 0.06, p = 0.806, R² = 0.000

Result: ❌ No statistically significant difference in teaching evaluation ratings between male and female instructors.

Male instructors scored only 0.018 points higher on average than female instructors (β = 0.018, p = 0.806).

Gender explains virtually none (0%) of the variance in evaluation scores.

2️⃣ Age & Beauty (ANOVA)

Question: Does the beauty score differ across age groups?

Model Output: F(4,195) = 0.29, p = 0.886

Result: ❌ The results were not statistically significant, indicating that beauty scores do not significantly differ across age groups.

This suggests that age group is not a major factor influencing perceived beauty in this dataset.

3️⃣ Beauty & Evaluation (Regression / Correlation)

Question: Is teaching evaluation score correlated with beauty score?

Model Output: F(1,198) = 0.25, p = 0.619, R² = 0.001

Result: ❌ No significant relationship was found between beauty and evaluation ratings.

The coefficient for beauty (β = -0.027, p = 0.619) was not significant, showing that beauty has no meaningful impact on teaching evaluation scores.

🏁 Conclusion

This practical provided experience in:

Applying OLS regression to analyze variable relationships.

Conducting ANOVA to compare group means across categories.

Interpreting statistical significance and model fit using p-values and R².

Across all analyses, none of the tested factors — gender on evaluation, age on beauty, or beauty on evaluation — showed any statistically significant effect.
Thus, within this dataset, teaching evaluations appear independent of gender, age, and beauty.
