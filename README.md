# CIVE-202-Project-4
---
## This includes files for Project no. 2:
- [Gantt Chart](CIVE202_Spring2026_Group151-05_Project4_GanttChart.pdf)
- [Timesheet](CIVE202_Spring2026_Group09_Project4_EngineeringTimesheet.docx)
- [Scope of Work](CIVE202_Spring2026_Group151-05_Project4_SOW.docx)
- [Annotated Code Document](CIVE202_Spring2026_Group151-05_Project4_ACD.docx)
- [Written Report](CIVE202_Spring2026_Group151-05_Project4_WrittenReport.docx)
- [Python Code](CIVE202_Spring2026_Group151-05_Project4_PythonCode.ipynb)
- [Colorado.csv](Colorado.csv)
- [Texas.csv](Texas.csv)
---
## Overview
Risk Averse, LLC hired us to examine where bias may exist in the NRI scoring methodology by doing sensitivity analysis. Risk Averse, LLC, wants to compare the current risk levels determined using the NRI method and data to an independent consultant’s definition of risk. For this project, we analyzed NRI data at the Census Tract level for Texas and Colorado and evaluate whether FEMA’s risk methodology introduces bias against socially vulnerable communities. Specific hazards examined include lightning and winter weather in Colorado, and heat waves and tornadoes in Texas. In addition, this project will develop an alternative risk model that places greater emphasis on social vulnerability and compare it with the existing NRI framework using the following formula:

Risk Score = (Expected Annual Loss × 0.40) + (Social Vulnerability × 0.45) + ((1 − Community Resilience) × 0.15)

The results will provide insight into how risk is distributed across communities and how different definitions of risk may influence decision making and resource allocation. The goal of this project is to analyze and evaluate natural disaster risk using publicly available NRI data and assess potential bias in FEMA’s methodology. The client has requested the following analyses:

1. Analyze risk at the Census Tract level for any two states, Texas and Colorado, focusing on lightning and winter weather in Colorado and heat waves and tornadoes in Texas.

2. Explain how FEMA defines and calculates risk using Expected Annual Loss, Social Vulnerability, and Community Resilience.

3. Develop an alternative risk formula that places greater emphasis on social vulnerability and compare it with FEMA’s model at the county level for each selected hazard.

4. Identify potential bias in risk classification and discuss its implications for affected communities.
---
## Project Tasks: 

### 1. Data Acquisition and Preparation
* NRI and SVI data cleaned
* select relevant vairables and merge state data

### 2. Understanding and explaining the NRI Model
* Review FEMA documentation
* Analysis factors of risk score

### 3. Data Analysis and Summarie Statistics
* analysis datasets for states
* Find mean, median, min, max
* Identify trends and differences in risk distribution

### 4. Development of Alternative Risk Model
* Define Risk
* Apply to datasets
* Analysis new risk

### 5. Sensitivity Analysis and 
*preform sensitivity analysis and compare risk scores
* Use the groupby() and agg() functions in pandas
* examine changes in risk classification

### 6. Visualization and Mapping
* Bar charts
* Maps for each state for each scores

### 7. Documentation and Reporting
* ACD
* Written report
* discussion of comparisons
* Github
  
## Methods
* We collected data from FEMA and CDC indexs
* We isolated colorado and Texas from the larger datasets
* We used metafiles for the variables in the NRI data
* We replaced null values with 9999
* NRI and SVI were merged using geographic identifier STCOFIPS/STCNTY
* Used python to calculate risk scores for the hazards
* We generated county level averages using python
* We generated heat maps using matplotlin and geopandas
  
## Results and Analysis
* The results showed that FEMA’s NRI scores and the alternative risk model did not produce identical patterns of risk. When the alternative formula placed more weight on social vulnerability, some counties and Census tracts appeared more at risk than they did under FEMA’s original method. Other areas became less prominent when compared to the NRI rankings. This shows that the final classification of “risk” is sensitive to the way the model is structured. 
* The county-level comparisons for Colorado and Texas showed noticeable differences between the original NRI values and the team’s calculated scores for the selected hazards. The maps and visualizations also showed that these changes were not evenly distributed across all areas. Instead, certain locations shifted more than others depending on their vulnerability and resilience characteristics. This suggests that the two methods highlight different communities as priorities for concern. 
* Overall, the results confirmed that modifying the weights in the risk formula changes how hazard risk is interpreted. The NRI method emphasizes FEMA’s existing framework, while the alternative model raises the importance of social conditions that may increase disaster impacts even when physical hazard exposure is not the highest.

## Discussion and Comparison 
* This project showed that the definition of risk has a major effect on the conclusions drawn from the data. FEMA’s NRI is useful because it provides a standardized way to compare communities nationwide, but it may not fully capture the challenges faced by socially vulnerable populations if those conditions do not strongly affect the final score. By increasing the weight on social vulnerability, the alternative model shifts more attention toward communities that may have fewer resources, weaker support systems, or more difficulty recovering after a disaster.

* These findings have important ethical and policy implications. If disaster funding or mitigation planning depends heavily on one risk formula, then communities identified as high risk under a different but reasonable definition may receive less support than they need. In this way, the structure of a model can create categorical bias by favoring one understanding of risk over another. This matters because FEMA funding and public policy decisions may be influenced by how these rankings are interpreted.

* In conclusion, the project found that FEMA’s NRI and the proposed alternative model can lead to different interpretations of natural disaster risk in Colorado and Texas. The sensitivity analysis supports the idea that risk scoring is not purely objective and depends on how important variables are weighted. For Risk Averse, LLC, this means that future analyses should carefully consider both the mathematical design of risk formulas and the social consequences of using them.
