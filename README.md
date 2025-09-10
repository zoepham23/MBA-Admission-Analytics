# MBA-Admission-Analytics
## Project Introduction

As someone interested in the decision-making behind competitive graduate programs, I was curious to explore what factors might influence admission into the Wharton School of Business—one of the top MBA programs in the U.S. Through this project, I aim to uncover data-driven insights on how elements like GPA, GMAT scores, work experience, and demographics relate to admission outcomes. My goal is to better understand the admissions landscape and share findings that may be helpful for prospective applicants.

## Dataset Overview

The dataset used in this project is included in this repository as [`MBA.csv`](MBA.csv).  

- **Source:** [Kaggle – MBA Admission Dataset](https://www.kaggle.com/datasets/taweilo/mba-admission-dataset)  
- **Note:** The dataset is synthetic, generated from Wharton Class of 2025 statistics

## Research Questions
Some research questions I use to guide the exploratory stage are:

1. How do GPA and GMAT scores correlate with admission status?
2. Are applicants from certain undergraduate majors (Business, STEM) more likely to be admitted?
3. What is the distribution of admission across gender, race, and international status?
4. Does demographic background impact admission rates?
5. Does the number of years of work experience correlate with higher admission rates?
6. Which industries have the highest proportion of admitted applicants?

## Key Insights
**1. GPA & GMAT:**
- Both GPA and GMAT scores are positively correlated with admission outcomes, meaning applicants with higher academic performance and stronger test scores tend to be admitted at higher rates.  
- Correlation analysis shows that GMAT (correlation coefficient 0.35) is a stronger driver of admission than GPA (0.28). This suggests that while both matter, admissions committees may weigh standardized test scores more heavily than academic GPA when making decisions.  
- The scatterplot below illustrates this relationship. Admitted applicants (orange) are generally clustered toward higher GMAT scores, while declined applicants are concentrated in the lower GMAT range. GPA shows a similar but weaker separation.  

![GPA vs GMAT Scatter](plots/gpa_gmat_scatterplot.png)

**2. Work Experience**  
Work experience demonstrates a clear threshold effect. Applicants with at least two years of professional experience were admitted at higher rates compared to those with less than two years.  

Admission rates increased from ~12% for applicants with 0–2 years of experience, to ~14–15% for those with 2–10 years. Beyond 5 years, the increase plateaus, suggesting diminishing returns after a certain point.  

This implies admissions committees may view professional experience as a critical qualification, but additional years beyond a threshold do not dramatically improve chances.  

![Admission by Work Experience](plots/work_exp.png)  


**3. Industry Background**  
Admission rates vary significantly by applicant industry. Investment Management (21.7%) and Financial Services (19.1%) had the highest admission rates, while Energy had the lowest (9.4%).  

This indicates that applicants from industries with stronger ties to MBA programs may be viewed more favorably, either due to alignment with business school career pipelines or transferable skill sets.  

The bar chart below shows how industry background influences admission outcomes.  

![Admission by Industry](plots/industry.png)  

**4. Undergraduate Majors**  
Admission rates across undergraduate majors (Business, STEM, Humanities) were broadly similar, averaging around 14%.  

A one-way ANOVA test confirmed there were **no statistically significant differences** between the groups (F = 0.28, p = 0.76). This suggests that, in this dataset, an applicant’s field of undergraduate study was **not a determining factor** in admissions decisions.  

The chart below illustrates the nearly identical admission rates across majors.  

![Admission by Major](plots/majors.png)


**5. Demographic Patterns**  
Logistic regression revealed demographic associations with admission outcomes. Female applicants were admitted at higher rates than males across most groups. Race effects also emerged: coefficients were positive for White and Other categories, and negative for Black and Hispanic categories.  

The model achieved 66% accuracy, but predictive power was limited due to class imbalance and unobserved factors (essays, recommendations, etc.). This means the results should be interpreted as patterns in the dataset, not definitive drivers of admissions.  

The chart below illustrates the logistic regression coefficients for demographic variables.  

![Logistic Regression Coefficients](plots/log_reg_coeffs.png)  

## Limitation Acknowledgement

## Next Steps

