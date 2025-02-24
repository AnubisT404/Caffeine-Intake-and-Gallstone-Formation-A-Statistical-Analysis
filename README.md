# **Caffeine Intake and Gallstone Formation: A Statistical Analysis**  

## **Overview**  
This project investigates the potential association between **caffeine consumption** and **gallstone formation** using data from the **NHANES 2017–2018** survey. The study explores whether caffeine intake influences gallstone prevalence and assesses whether this relationship varies across different demographic groups.  

Using **logistic regression models**, the analysis incorporates various **lifestyle, dietary, and demographic factors** to understand their role in modifying this association.  

---

## **Research Objectives**  
- Examine the relationship between **caffeine intake** and **gallstone occurrence**  
- Assess how **age, sex, race, and dietary factors** impact this relationship  
- Investigate potential differences in the effect of caffeine intake between **men and women**  

---

## **Dataset**  
The analysis utilizes data from the **NHANES 2017–2018** survey, conducted by the CDC.  

**Study Sample:**  
- Initial dataset included **9,254 participants**  
- After applying **exclusion criteria**, the final sample consisted of **3,793 individuals**  

**Caffeine Intake Categories:**  
- **Low:** ≤50 mg  
- **Normal:** 51–200 mg *(reference group)*  
- **High:** 201–400 mg  
- **Very High:** >401 mg  

**Additional Covariates:**  
- **Demographic factors:** Age, Sex, Race/Ethnicity, Education  
- **Lifestyle variables:** BMI, Physical Activity, Smoking, Alcohol Consumption  
- **Dietary factors:** Fiber, Fat, Cholesterol, Vitamin C, Water Intake  

---

## **Methodology**  
### **1. Data Processing & Study Design**  
- Excluded individuals **under 20 years old, pregnant individuals, and diabetics**  
- Caffeine intake data derived from **24-hour dietary recall surveys**  
- Gallstone occurrence was determined via **self-reported medical history**  

### **2. Statistical Analysis**  
**Descriptive Statistics:**  
- **Mean comparisons** using t-tests  
- **Categorical distributions** analyzed with chi-square tests  

**Regression Models:**  
- **Unadjusted Model:** Caffeine intake as the only predictor  
- **Adjusted Model:** Incorporating covariates (age, sex, race, BMI, fiber, fat)  
- **Interaction Model:** Examining caffeine intake × sex interaction  

**Model Performance Metrics:**  
- **Akaike Information Criterion (AIC)** and **Bayesian Information Criterion (BIC)** for model comparison  
- **Pseudo-R² values** to assess goodness-of-fit  
- **Variance Inflation Factor (VIF)** to check for collinearity  

---

## **Results and Key Findings**  

| Predictor | Odds Ratio (OR) | 95% Confidence Interval | p-value |
|-----------|--------------|---------------------|---------|
| **Sex (Female vs. Male)** | 2.53 | (1.61, 3.99) | 0.007 |
| **Age (per year increase)** | 1.04 | (1.03, 1.05) | <0.001 |
| **BMI (per unit increase)** | 1.08 | (1.05, 1.11) | 0.003 |
| **Race (Black vs. White)** | 0.45 | (0.19, 1.07) | 0.060 |
| **Caffeine Intake (Very High vs. Normal)** | 0.86 | (0.28, 2.64) | 0.797 |
| **Caffeine × Sex Interaction** | - | - | 0.014 |

### **Key Takeaways:**  
- **No significant association** was found between **caffeine intake and gallstones**  
- **Women** had a **2.5x higher likelihood** of gallstones compared to men  
- **Higher BMI and age** were significantly associated with increased gallstone risk  
- **Men showed a slight protective trend at very high caffeine intake**, while this was not observed in women  

---

## **Conclusion**  
This study suggests that while **caffeine intake alone is not a significant predictor** of gallstones, **demographic and lifestyle factors play a crucial role** in gallstone development. The **higher prevalence in women** and the **age-related risk** highlight the need for further research into metabolic and dietary influences on gallstone formation.  

---

## **Dependencies and Setup**  
### **Required Libraries (R)**  
```r
install.packages(c("tidyverse", "survey", "haven", "writexl", "jtools", "broom", "ggthemes", "car"))
```
### **Data Sources**  
- NHANES 2017–2018: Public dataset from **CDC National Health and Nutrition Examination Survey**  
- Data downloaded and processed using R **(tidyverse, survey, haven)**  

---

## **Project Structure**  
```
gallstone-analysis/
│── data_preprocessing.R              # Data cleaning and preparation
│── exploratory_analysis.R            # Descriptive statistics and visualizations
│── README.md                         # Project documentation
```

---

## **Next Steps**  
- Expand analysis to include **longitudinal data** for causality assessment  
- Explore **dietary and genetic factors** in gallstone formation  
- Investigate potential **mechanisms behind sex differences** in gallstone risk  
