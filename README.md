# Project Rest Wellness and Lifestyle

**Project Rest Wellness and Lifestyle** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.



# ![what is wellness ](https://lirp.cdn-website.com/6aa52cbd/dms3rep/multi/opt/what+is+wellness-1920w.jpg)


## Dataset Content

* Synthetic data set created by Laksika Tharmalingam for illustrative purposes. The Sleep Health and Lifestyle Dataset comprises 400 rows and 13 columns, covering a wide range of variables related to sleep and daily habits. It includes details such as gender, age, occupation, sleep duration, quality of sleep, physical activity level, stress levels, BMI category, blood pressure, heart rate, daily steps, and the presence or absence of sleep disorders. It has been stored on Kaggle (https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data).

* Dataset Columns:

Person ID: An identifier for each individual.

Gender: The gender of the person (Male/Female).

Age: The age of the person in years.

Occupation: The occupation or profession of the person.

Sleep Duration (hours): The number of hours the person sleeps per day.

Quality of Sleep (scale: 1-10): A subjective rating of the quality of sleep, ranging from 1 to 10.

Physical Activity Level (minutes/day): The number of minutes the person engages in physical activity daily.

Stress Level (scale: 1-10): A subjective rating of the stress level experienced by the person, ranging from 1 to 10.

BMI Category: The BMI category of the person (e.g., Underweight, Normal, Overweight).

Blood Pressure (systolic/diastolic): The blood pressure measurement of the person, indicated as systolic pressure over diastolic pressure.

Heart Rate (bpm): The resting heart rate of the person in beats per minute.

Daily Steps: The number of steps the person takes per day.

Sleep Disorder: The presence or absence of a sleep disorder in the person (None, Insomnia, Sleep Apnea).

* Details about Sleep Disorder Column:

None: The individual does not exhibit any specific sleep disorder.

Insomnia: The individual experiences difficulty falling asleep or staying asleep, leading to inadequate or poor-quality sleep.

Sleep Apnea: The individual suffers from pauses in breathing during sleep, resulting in disrupted sleep patterns and potential health risks.

## Business Requirements

* Objective:

The purpose of this study is to analyze the relationship between sleep disorders and cardiovascular health indicators (blood pressure and heart rate), as well as the impact of obesity on sleep quality. The findings will help in: Identifying potential health risks associated with sleep disorders. Understanding the cardiovascular implications of sleep disturbances. Evaluating how obesity affects sleep quality.

## Scope

* The study will assess:

Blood pressure and heart rate variations between individuals with and without sleep disorders.

Sleep quality differences between obese and normal BMI individuals.

Statistical significance of observed differences to validate or reject the stated hypotheses.

## Hypothesis and how to validate?

* Hypothesis 1: Cardiovascular Impact of Sleep Disorders

Null Hypothesis (H₀): There is no significant difference in blood pressure and heart rate between individuals with and without sleep disorders.

Alternative Hypothesis (H₁): There is a significant difference in blood pressure and heart rate between individuals with and without sleep disorders.

* Hypothesis 2: Obesity and Sleep Quality

Null Hypothesis (H₀): Individuals classified as obese do not have lower sleep quality compared to those with normal BMI.

Alternative Hypothesis (H₁): Individuals classified as obese have lower sleep quality compared to those with normal BMI.

* Validation:
A. Test for Hypothesis 1 (Sleep Disorders & Cardiovascular Health)
1. Data Preprocessing:

Check for missing values and outliers.
Ensure normality of data distribution (use Shapiro-Wilk test or Q-Q plots).

2. Choose Statistical Test:

If data follows a normal distribution: Independent t-test (to compare mean blood pressure & heart rate between groups).
If data is non-normally distributed: Mann-Whitney U test (non-parametric alternative).
If multiple factors (e.g., age, gender) influence results: ANCOVA (to adjust for covariates).

3. Interpret Results:

If p-value < 0.05, reject H₀ → Significant difference exists.
If p-value ≥ 0.05, fail to reject H₀ → No significant difference.

B. Test for Hypothesis 2 (Obesity & Sleep Quality)
1. Data Preprocessing:

Categorize participants based on BMI (Normal, Overweight, Obese).
Ensure sleep quality score is a continuous variable.
2. Choose Statistical Test:

If sleep quality scores are normally distributed: ANOVA (to compare means across BMI groups).
If non-normal distribution: Kruskal-Wallis test (non-parametric alternative).
For binary classification (Good vs. Poor Sleep Quality): Chi-Square Test.

3. Interpret Results:

If p-value < 0.05, reject H₀ → Obesity significantly impacts sleep quality.
If p-value ≥ 0.05, fail to reject H₀ → No significant impact detected.

## Project Plan

* Making decision whether to analyze the existing small dataset or generate additional synthetic data — ChatGPT's synthetic data recommendation
* Undertake initial analysis to look at potential hypothesis to test - Paraplexity Ideation Session
* Choose Hypothesis to test
* Complete ETL and EDA for core data
* Undertake analysis to prove/disprove hypothesis firstly in Jupiter Notebook, secondly in Tableau 
* Undertake statistical tests on the dataset
* Creating Dashboard in Tableau
* Produce commentary on hypothesis and analysis

## The rationale to map the business requirements to the Data Visualisations

* Understand the cardiovascular implications of sleep disturbances
A. Rationale: If sleep disorders significantly impact cardiovascular metrics, this could justify preventive measures and medical interventions.

Visualizations:
Scatter plots showing the relationship between sleep duration and cardiovascular indicators (heart rate, blood pressure).
Correlation heatmaps to explore relationships among sleep disorders, blood pressure, and heart rate.

* Evaluate how obesity affects sleep quality
B. Rationale: Obese individuals may experience poor sleep quality due to factors such as sleep apnea and metabolic issues. Understanding this relationship could guide lifestyle recommendations.

Visualizations:
Bar charts or boxplots comparing sleep quality scores across BMI categories (Normal, Overweight, Obese).
Violin plots illustrating the distribution of sleep quality within each BMI category.


## Analysis techniques used

1. Independent t-tests (for Hypothesis 1: Cardiovascular Impact of Sleep Disorders)

Used to compare the means of blood pressure and heart rate between individuals with and without sleep disorders.

Limitations:
- Assumes normality and equal variance, which may not always be true.
- Does not account for potential confounding variables (e.g., age, stress levels).

Alternative: A Mann-Whitney U test could be used if normality assumptions are violated.

2. One-Way ANOVA (for Hypothesis 2: Obesity and Sleep Quality)

Used to compare sleep quality across different BMI categories (Normal, Overweight, Obese).

Limitations:

- Assumes normality and homogeneity of variance.
- Only detects if there is a difference but does not indicate where the difference lies.

Alternative: A Kruskal-Wallis test could be used if data is non-parametric. Post-hoc tests (Tukey's HSD) could pinpoint group differences.

3. Correlation Analysis & Visualization

- Correlation heatmaps help identify relationships between variables like sleep duration, blood pressure, and heart rate.

Limitations:

- Correlation does not imply causation.
- Does not account for interaction effects or confounding variables.

Alternative: A multiple regression analysis could adjust for confounders.

* Structure of Data Analysis Techniques & Justification:

- ETL (Extract, Transform, Load) and (Exploratory Data Analysis) - Checked for missing values, outliers, and data distribution. Justification: Ensures data integrity and suitability for statistical tests.

- Hypothesis Testing - T-tests and ANOVA to evaluate statistical significance.

- Visualisation & Interpretation - Used boxplots, scatter plots, and heatmaps to communicate findings effectively. Helps in identifying patterns, trends, and outliers visually.

* Did the data limit you, and did you use an alternative approach to meet these challenges?

I intentionally chose a small dataset due to my laptop's limited computing power. However, this turned out to be a challenge, as data cleaning left me with only 369 rows. I considered creating an additional dataset but ultimately decided to proceed with the one I already had.

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

During ideation, I used Paraplexity to identify relevant items for investigation. I also consulted ChatGPT while considering the creation of additional synthetic data. When my code or Copilot-generated code didn’t work, I sought assistance from ChatGPT. Additionally, I used Copilot to generate some of the plots. Additionaly, I used ChatGPT to help me with grammar corrections while writing my README file.

## Ethical considerations (comments generated with Chat GPT Input)

1. Data Privacy Issues & Mitigation
Issue: Since the dataset is synthetic, there is no real personal or health data at risk. However, synthetic data should still be generated in a way that accurately represents real-world distributions without inadvertently leaking sensitive information from original datasets.

Mitigation: 
Ensured the synthetic data was fully artificial, generated using statistical models and deep learning techniques without direct mapping to real individuals.
Validated that no identifiable patterns from real data sources were replicated.
Followed ethical guidelines for data synthesis and anonymization techniques to prevent re-identification risks.

2. Bias and Fairness Issues
Sampling Bias:

Issue: Synthetic data may unintentionally mirror biases present in the original dataset (e.g., underrepresentation of certain demographics).

Solution: Ensured diversity by balancing gender, age, and BMI distributions when generating synthetic records.

Algorithmic Bias:

Issue: If synthetic data was generated using biased real-world datasets, it might still reflect inequalities (e.g., over-representing a particular population group).

Solution: Used bias detection tools to test for imbalances and adjusted distributions accordingly.

Data Quality & Realism:

Issue: If synthetic data does not reflect real-world conditions accurately, the study's findings may lack validity.
Solution: Used real-world statistics to calibrate synthetic data generation and validated outcomes against known medical research.

3. Legal and Societal Issues & Solutions

Ethical Transparency: Clearly communicated that the dataset was synthetic and not based on actual patient records.
Regulatory Compliance: Since no real patient data was used, there were fewer legal constraints, but the study still adhered to best practices for research ethics (e.g., Institutional Review Board (IRB) approval if needed).

Avoiding Misuse: Ensured that synthetic data was not used to train AI models in a way that could introduce biased healthcare policies.

Final Takeaway
By using properly generated synthetic data, we eliminated privacy risks while still addressing bias and fairness concerns through careful validation. As I didn't create synthetic dataset which I used in the project I can not comment how was created and did bias detection tools were used. 

## Dashboard Design

Dashboard - 'Sleep Disorders, BMI & Vital Signs' Consists:
- Table - 'Average Sleep Duration in Hours'
- Graphs: 'Systolic Pressure vs Sleep Disorder', 'Diastolic Pressure vs Sleep Disorder',
'Average sleep quality per BMI Group'and 'BMI vs Sleep Disorder' 

'Systolic Pressure vs Sleep Disorder'and 'Diastolic Pressure vs Sleep Disorder' have drop down where user can choose sleep disorder. 

The dashboard was designed with a non-technical audience in mind, so simple bar charts were used to present insights in an easily digestible format. For the KPI, I chose average sleep duration in hours to highlight differences in sleep patterns across various BMI categories.

## Unfixed Bugs

There are no unfixed bugs in the project. I made sure to address all identified issues during the development process.
Throughout the development, I did not encounter any specific shortcomings of the frameworks or technologies that prevented me from fixing bugs. 
While working on the project, I did recognize a few gaps in my knowledge, particularly around creating Dashboard in Tableau. To address this, I researched documentation and youtube videos to enhance my understanding.

## Development Roadmap

* A major challenge I faced was ensuring the dashboard, designed for a non-technical audience, presented data in a simple and understandable way while still conveying important details. I couldn’t use box plots, as they are often difficult for many people to interpret. To address this, I used bar charts instead, as they are more accessible and easier to understand for a non-technical audience.

* In the near future, I plan to learn how to use Streamlit to deploy my next dashboard. 

## Main Data Analysis Libraries

Plotly is used for data visualisation as it supports a wide range of charts like 3D plots.


## Credits 

* LMS, Chatgpt, Paraplexity

### Content 

Dataset taken from: https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data

Dataset Summary comments layout taken from: https://www.kaggle.com/code/sulaniishara/sleep-wellbeing 

Picture what is wellness taken from: https://lirp.cdn-website.com/6aa52cbd/dms3rep/multi/opt/what+is+wellness-1920w.jpg

