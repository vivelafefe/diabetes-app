# DIABETES APP: AI-Based System for Personalized Insulin Dose Recommendations: Integrating External Factors for Enhanced Accuracy in Type 1 Diabetes Management
## ABSTRACT
This project seeks to develop an AI-based system that will provide personalized short-acting insulin dose recommendations before meals to individuals living with type 1 diabetes, empowering them to better manage their condition. The system will use data collected from individuals in a structured format to accurately predict the most appropriate insulin doses based on their individual factors, including external factors such as weather or physical activity, providing an alternative to the traditional calculation method.
## QUESTION
Can an AI-based system provide more accurate insulin dose recommendations than existing methods of insulin dose prediction?
## HYPOTHESIS
An AI-based system will provide more accurate and personalized insulin dose recommendations than existing methods of insulin dose prediction due to its ability to incorporate a diverse range of external factors that influence insulin sensitivity.
## BACKGROUND
The background research examines the global distribution of type 1 diabetes and investigates the conventional approach for calculating insulin dosage. 
According to the International Diabetes Federation (IDF), around 10% of all people with diabetes have type 1 diabetes and  the total number of people living with diabetes is projected to rise to 643 million by 2030 and 783 million by 2045 [1]. The analysis of the data presented in the IDF's 2022 report [2] reveals the highest prevalence rates in specific regions, namely Northern Europe (Finland, Sweden, Norway), Canada, and Gulf states (Saudi Arabia, Qatar, and Kuwait). 
Countless individuals with diabetes type 1 struggle with accurately predicting insulin doses. The traditional calculation includes two parts: high blood glucose correction + carbohydrate coverage [3], but other factors affecting insulin sensitivity are not taken into account  [4]. The visualization of the factors showcases both the existing factors that are currently considered and the numerous untapped factors that could enhance the accuracy of insulin dosage calculations. This project specifically focuses on a few factors that are easily collectible and quantifiable.

![Image](image9.png)

_Tools used: data preprocessing and analysis in Python ([view notebook1](0_BackgroundResearch_1.ipynb), [view notebook2](0_BackgroundResearch_2.ipynb)) + data storage in PostgreSQL + visualization in Tableau [(view dashboard)](https://public.tableau.com/views/DiabetesApp_0_BackgroundResearch/0_Backgroundresearch?:language=en-US&:display_count=n&:origin=viz_share_link)._

## DATA
Data from one patient was collected to create a core concept for the AI system: pre-meal blood glucose, carb intake, injected insulin doses (manual Excel & dietary app); physical activity (Health App/Apple Watch); and weather records (VisualCrossing.com).
## PROCEDURE
The project consisted of the following steps:
### 1. DATA ANALYSIS
The analysis involves merging, preprocessing, and performing descriptive and predictive analysis on the collected data.

![Image](image1.png)

_Tools used: Matplotlib sankey diagram in Python [(view notebook)](ProcessSankeys.ipynb)_

#### 1_1_Data merging
Collected data from diverse sources were consolidated into a single dataset. The visualization shows a well-distributed pattern of data over time, with higher density in the Health App and weather data. This is because the patient-collected data is recorded only before meals, while other data points are recorded more frequently.

![Image](image7.png)

_Tools used: data manipulation in Python [(view notebook)](1_1_Merging.ipynb) + visualization in Tableau [(view dashboard)](https://public.tableau.com/views/DiabetesApp_1_1_Merging/1_1_Merging?:language=en-US&:display_count=n&:origin=viz_share_link).
