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

---
### **Key Takeaways:**  
- **No significant association** was found between **caffeine intake and gallstones**  
- **Women** had a **2.5x higher likelihood** of gallstones compared to men  
- **Higher BMI and age** were significantly associated with increased gallstone risk  
- **Men showed a slight protective trend at very high caffeine intake**, while this was not observed in women  

---

### **Required Libraries (R)**  
```r
install.packages(c("tidyverse", "survey", "haven", "writexl", "jtools", "broom", "ggthemes", "car"))
```
---

## **Next Steps**  
- Expand analysis to include **longitudinal data** for causality assessment  
- Explore **dietary and genetic factors** in gallstone formation  
- Investigate potential **mechanisms behind sex differences** in gallstone risk  
