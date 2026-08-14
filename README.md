# Patient Healthcare Cost Analysis

## Project Overview

This project analyzes patient-level healthcare data to investigate the factors associated with post-index total healthcare costs.

The analysis focuses on healthcare utilization,comorbidity burden,medication adherence,and their relationships with healthcare costs.

The project combines exploratory data analysis,statistical hypothesis testing,correlation analysis,multivariable linear regression,and regression diagnostics to identify meaningful patterns and potential healthcare cost drivers. 

## Business Questions

This project addresses the following key business and healthcare analytics questions:

1. Is medication adherence (PDC ≥ 80%) associated with differences in post-index total healthcare costs?

2. Which healthcare utilization measures are most strongly associated with post-index healthcare costs?

3. Does comorbidity burden contribute to higher post-index healthcare costs?

4. Which factors remain significantly associated with healthcare costs after adjusting for multiple variables simultaneously?

5. How well does the multivariable regression model explain variation in post-index healthcare costs?

6. Are there important limitations in the regression model, such as heteroscedasticity or increasing prediction error at higher cost levels?

## Datasaet

The project uses patient-level healthcare data containing information on healthcare utilization, medication adherence, comorbidity burden, and post-index healthcare costs.

The dataset was divided into training and test files and combined during the analysis to create the final analytical sample.

Key variables used in the analysis include:

- Inpatient admissions
- Outpatient visits
- Emergency room visits
- Total length of stay
- Comorbidity count
- Medication adherence (PDC ≥ 80%)
- Post-index total healthcare cost

The analysis focuses on the relationship between these variables and post-index total healthcare costs.

## Tools & Technologies

The project was developed using the following tools and technologies:

- Python — primary programming language for data analysis
- Pandas — data loading, cleaning, transformation, and analysis
- NumPy — numerical calculations and regression computations
- SciPy — statistical hypothesis testing and p-value calculations
- Matplotlib — data visualization and regression diagnostics
- scikit-learn — multivariable linear regression
- Jupyter Notebook — development environment and analytical documentation

## Methodology
 The analysis followed a structured healthcare analytics workflow:

1. Data Preparation
   - Loaded and reviewed the healthcare datasets.
   - Checked the structure and relevant variables.
   - Prepared the data for statistical analysis.

2. Exploratory Data Analysis
   - Examined patient characteristics and healthcare utilization.
   - Analyzed distributions of healthcare costs and length of stay.
   - Identified important patterns and variability in the data.

3. Medication Adherence Analysis
   - Compared post-index healthcare costs between patients with PDC < 80% and PDC ≥ 80%.
   - Used Welch's t-test to evaluate whether the difference in mean costs was statistically significant.

4. Correlation Analysis
   - Evaluated the relationships between healthcare utilization, comorbidity burden, medication adherence, and post-index healthcare costs.
   - Calculated correlation coefficients and statistical significance.

5. Multivariable Linear Regression
   - Built a multivariable linear regression model using healthcare utilization, length of stay, comorbidity count, and medication adherence as predictors.
   - Evaluated model fit using R².
   - Calculated regression coefficients, standard errors, t-statistics, and p-values.

6. Regression Diagnostics
   - Examined residuals and prediction errors.
   - Compared absolute residual variability across predicted-cost groups.
   - Evaluated potential heteroscedasticity.
   - Performed a lag-1 residual correlation check.

7. Business and Healthcare Interpretation
   - Translated statistical findings into healthcare analytics insights.
   - Identified potential areas for utilization monitoring, cost management, and future analysis.

## Key Findings
The analysis identified several important findings:

- Healthcare utilization was strongly associated with post-index healthcare costs.
- Inpatient admissions showed the strongest correlation with cost (r = 0.600).
- Outpatient visits also showed a strong positive association with cost (r = 0.551).
- Total length of stay was positively associated with cost (r = 0.503).
- Emergency room visits showed a moderate positive association with cost (r = 0.313).
- Comorbidity count showed a weaker but statistically significant positive association with cost (r = 0.231).
- The difference in mean costs between patients with PDC < 80% and PDC ≥ 80% was not statistically significant (Welch's t-test, p = 0.613).
- The multivariable regression model achieved an R² of 0.545, explaining approximately 54.5% of the variation in post-index healthcare costs.
- In the adjusted regression model, inpatient admissions, outpatient visits, emergency room visits, total length of stay, and comorbidity count remained statistically significant.
- Medication adherence (PDC ≥ 80%) was not statistically significant in the multivariable model (β = 191.38, p = 0.625).
- Regression diagnostics indicated potential heteroscedasticity, with prediction errors increasing at higher predicted-cost levels.

## Statistical Analysis

The statistical analysis was used to evaluate whether the observed relationships between patient characteristics, healthcare utilization, medication adherence, and post-index healthcare costs were statistically significant.

### Medication Adherence — Welch's t-test

Post-index healthcare costs were compared between patients with PDC < 80% and patients with PDC ≥ 80%.

Patients with PDC ≥ 80% had a lower observed mean cost than patients with PDC < 80%. However, the difference was not statistically significant (Welch's t-test, p = 0.613).

Therefore, the analysis does not provide sufficient statistical evidence that medication adherence status was independently associated with differences in mean post-index healthcare costs in this sample.

### Correlation Analysis

Correlation analysis was used to evaluate the strength and direction of relationships between healthcare utilization, comorbidity burden, medication adherence, and post-index healthcare costs.

The strongest positive correlations with post-index healthcare costs were observed for:

- Inpatient admissions: r = 0.600
- Outpatient visits: r = 0.551
- Total length of stay: r = 0.503
- Emergency room visits: r = 0.313
- Comorbidity count: r = 0.231

All reported correlation tests were statistically significant (p < 0.001).

These results indicate that higher healthcare utilization and greater comorbidity burden were associated with higher post-index healthcare costs. However, correlation does not imply causation.

## Regression Analysis

A multivariable linear regression model was developed to evaluate the relationship between healthcare utilization, comorbidity burden, medication adherence, and post-index healthcare costs while controlling for multiple predictors simultaneously.

The model included:

- Inpatient admissions
- Outpatient visits
- Emergency room visits
- Total length of stay
- Comorbidity count
- Medication adherence (PDC ≥ 80%)

### Model Performance

The regression model achieved an R² of 0.545, meaning that the included predictors explained approximately 54.5% of the variation in post-index healthcare costs.

### Significant Predictors

After adjusting for the other variables in the model, inpatient admissions, outpatient visits, emergency room visits, total length of stay, and comorbidity count remained statistically significant predictors of post-index healthcare costs.

This indicates that healthcare utilization and comorbidity burden were associated with healthcare costs even after controlling for the other variables included in the model.

### Medication Adherence

Medication adherence (PDC ≥ 80%) was not statistically significant in the multivariable regression model (β = 191.38, p = 0.625).

Although the estimated coefficient was positive, the p-value indicates that there was insufficient statistical evidence of an independent association between PDC ≥ 80% status and post-index healthcare costs in this model.

### Regression Diagnostics

Regression diagnostics indicated potential heteroscedasticity, with prediction errors increasing at higher predicted-cost levels.

This suggests that the constant-variance assumption of ordinary least squares regression may not be fully satisfied and should be considered when interpreting the model results.

## Business / Healthcare Insights

The findings provide several potential insights from a healthcare analytics perspective.

### Healthcare Utilization and Cost

Healthcare utilization measures showed the strongest associations with post-index healthcare costs. In particular, inpatient admissions, outpatient visits, and length of stay were strongly associated with higher costs.

This suggests that monitoring healthcare utilization may be valuable for identifying patients with higher expected healthcare costs and for supporting resource planning.

### Comorbidity Burden

Comorbidity count was positively associated with post-index healthcare costs and remained statistically significant in the multivariable regression model.

Patients with a higher burden of comorbid conditions may therefore represent a group that requires closer monitoring from a healthcare resource and cost-management perspective.

### Medication Adherence

Medication adherence based on PDC ≥ 80% was not statistically significant in either the group comparison or the multivariable regression model.

This does not demonstrate that medication adherence has no relationship with healthcare outcomes. Instead, the results suggest that additional analysis and potentially more detailed adherence measures may be required to understand its relationship with healthcare costs.

### Potential Healthcare Applications

The analysis could support several potential healthcare analytics applications:

- Monitoring high healthcare utilization
- Identifying patients with potentially higher future healthcare costs
- Supporting resource allocation and capacity planning
- Evaluating the relationship between comorbidity burden and healthcare utilization
- Supporting further analysis of medication adherence and healthcare outcomes

These findings should be interpreted as associations rather than causal relationships.

## Limitations

The analysis has several limitations that should be considered when interpreting the results.

- The dataset is observational, so the analysis identifies associations but does not establish causal relationships.
- The dataset may not represent the full complexity of real-world healthcare populations and utilization patterns.
- The analysis is based on the variables available in the dataset, and potentially relevant factors may not be included in the model.
- Medication adherence was represented using a PDC ≥ 80% threshold, which may not capture the full complexity of medication-taking behavior.
- The multivariable regression model explained 54.5% of the variation in post-index healthcare costs, indicating that other factors not included in the model may also contribute to cost differences.
- Regression diagnostics indicated potential heteroscedasticity, suggesting that the variance of prediction errors may not be constant across all levels of predicted cost.
- The analysis did not establish whether the observed relationships would remain consistent across different patient populations or healthcare settings.

## Future Analysis

Future analysis could extend this project in several directions:

- Apply additional regression techniques or transformation methods to address potential heteroscedasticity.
- Explore nonlinear relationships between healthcare utilization and healthcare costs.
- Investigate interaction effects between comorbidity burden, utilization, and medication adherence.
- Evaluate additional patient-level factors that may improve the prediction of healthcare costs.
- Compare model performance using alternative machine learning regression approaches.
- Validate the findings on additional healthcare datasets or different patient populations.
- Develop an interactive Power BI dashboard to communicate key healthcare cost and utilization insights to non-technical stakeholders.

## Project Structure

The repository contains the following main files and directories:

- `Patient_Healthcare_Cost_Analysis.ipynb` — Jupyter Notebook containing the complete data analysis, statistical tests, regression model, visualizations, and diagnostics.
- `healthcareTrain.csv` — Training dataset used as part of the healthcare analysis.
- `healthcareTest.csv` — Test dataset used as part of the healthcare analysis.
- `.gitignore` — Specifies files and directories that should not be tracked by Git.
- `healthcare_analytics_env/` — Local Python virtual environment used for the project and excluded from version control.
