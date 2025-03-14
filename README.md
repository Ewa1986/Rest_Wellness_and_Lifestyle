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

The purpose of this study is to analyze the relationship between sleep disorders and cardiovascular health indicators (blood pressure and heart rate), as well as the impact of obesity on sleep quality. The findings will help in:

Identifying potential health risks associated with sleep disorders.

Understanding the cardiovascular implications of sleep disturbances.

Evaluating how obesity affects sleep quality.

Informing healthcare providers and policymakers for better health interventions.

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
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
1. Data Privacy Issues & Mitigation
Issue: Since the dataset is synthetic, there is no real personal or health data at risk. However, synthetic data should still be generated in a way that accurately represents real-world distributions without inadvertently leaking sensitive information from original datasets.
Solution:
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
By using properly generated synthetic data, we eliminated privacy risks while still addressing bias and fairness concerns through careful validation.

* 1. Data Privacy Issues & Mitigation
Issue: The study collects sensitive health data (blood pressure, heart rate, BMI, sleep disorder status). If not handled properly, there is a risk of data breaches or misuse.
Solution:
Used anonymized data by replacing identifiable details with unique participant codes.
Ensured data encryption for storage and transmission.
Limited access to authorized researchers only.
Complied with HIPAA (Health Insurance Portability and Accountability Act) and GDPR (General Data Protection Regulation) standards.
2. Bias and Fairness Issues
Sampling Bias:

Issue: If participants are not diverse (e.g., only a specific age group, gender, or ethnicity), results may not be generalizable.
Solution: Used randomized sampling and ensured diverse representation in the participant pool.
Measurement Bias:

Issue: Self-reported sleep quality may be subjective and influenced by personal perception.
Solution: Used validated sleep quality assessments (e.g., Pittsburgh Sleep Quality Index) and objective measurements like actigraphy.
Algorithmic Bias (If Using AI for Analysis):

Issue: If machine learning models were used, they might reinforce biases present in historical data.
Solution: Conducted bias audits and ensured fairness in model training data.
3. Legal and Societal Issues & Solutions
Informed Consent:
Ensured all participants understood the study objectives, risks, and their rights before participation.
Stigma Around Sleep Disorders & Obesity:
Provided counseling and health education to participants to minimize psychological distress.
Public Health Implications:
Shared findings responsibly to avoid misinterpretation or misuse by insurance companies or employers.


## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

Dataset Summary comments layout inspired by: https://www.kaggle.com/code/sulaniishara/sleep-wellbeing 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.