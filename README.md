# Instructor-Effectiveness-Analysis
Machine Learning project to evaluate instructor effectiveness

Project Overview :
This project aims to evaluate and predict instructor effectiveness using data-driven techniques. By analysing learner performance, engagement, and feedback metrics, we build a machine learning model to identify high-performing instructors.



Objective :
- Define a meaningful  Instructor Effectiveness Score
- Perform Exploratory Data Analysis (EDA)
- Apply Feature Engineering
- Train ML models to classify instructor performance
- Provide actionable insights for EdTech platforms



Dataset Description :
The dataset contains batch-level information with the following key features:

- `completion_rate`
- `avg_score_improvement`
- `avg_quiz_score`
- `dropout_rate`
- `avg_watch_time`
- `assignment_submission_rate`
- `forum_activity_rate`
- `avg_feedback_score`
- `feedback_response_rate`

Each row represents a course batch handled by an instructor.



Approach

Data Preprocessing :
- Checked for missing values (none found)
- Ensured data consistency



Exploratory Data Analysis (EDA) :
- Statistical summary using `.describe()`
- Correlation analysis using heatmap
- Distribution plots for key features

Key Insights:
- Completion rate positively correlates with feedback score
- Dropout rate negatively impacts performance
- Engagement features strongly influence outcomes



Feature Engineering :
- Created normalized feedback score
- Designed engagement score combining:
  - Watch time
  - Assignment submission
  - Forum activity



Effectiveness Score Design :
A custom score was created using weighted metrics:

- Positive factors:
  - Completion Rate
  - Score Improvement
  - Engagement
  - Feedback

- Negative factor:
  - Dropout Rate

This score was then converted into categories:
- Low
- Medium
- High effectiveness



Aggregation :

- Aggregated data at instructor level
- Calculated mean performance
- Added batch count as experience indicator



Model Building :
Two models were used:

🔹 Logistic Regression
- Provides interpretability
- Works well with scaled features

🔹 Random Forest
- Captures non-linear relationships
- More robust and accurate



Model Evaluation :
- Accuracy Score
- Classification Report
- Feature Importance Analysis



Key Findings :
- Completion rate and engagement are strongest predictors
- Feedback plays a crucial role in effectiveness
- Random Forest outperformed Logistic Regression slightly



Limitations :
- No data on course difficulty
- No student demographic information
- Possible bias due to varying course complexity



Future Improvements :
- Include instructor experience data
- Add course-level difficulty metrics
- Use advanced models (XGBoost, Neural Networks)



Technologies Used :
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook



Conclusion :
This project demonstrates how data can be used to evaluate teaching effectiveness in a scalable and objective way. It provides valuable insights for improving instructor performance and enhancing learner outcomes.



Author :
Narayan Ekhande 
