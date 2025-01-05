Banking Insurance Product 

## **Project Overview**
This project involves developing a predictive model to determine which customers are likely to purchase a variable rate annuity product offered by a commercial bank. The project is divided into three phases, each focusing on specific tasks related to data analysis, model building, and performance evaluation.

### **Objective**
The primary goal is to analyze customer data, identify significant predictors, and build a robust logistic regression model to predict the likelihood of purchasing the insurance product. The final deliverable will include insights, model performance metrics, and actionable recommendations for the bank.

---

## **Project Phases**

### **Phase 1: Variable Understanding and Assumptions**
- **Tasks**:
  - Explore predictor variables individually with the target variable (purchase of insurance product).
  - Summarize significant variables in a ranked table by their significance level ($$ \alpha = 0.002 $$).
  - Categorize variables into four classes: binary, ordinal, nominal, and continuous.
  - Provide odds ratios for binary predictors and interpret the highest magnitude odds ratio.
  - Assess linearity assumptions for continuous variables.
  - Identify missing values and redundant variables.
  - Highlight interesting findings in an executive summary.

- **Deliverables**:
  - A business report summarizing findings.
  - Tables of significant variables (separated by variable class) and odds ratios.
  - Visualizations for missing data and redundancy analysis.

---

### **Phase 2: Variable Selection and Model Building**
- **Tasks**:
  - Use binned training data to handle continuous variables and missing values.
  - Address separation concerns in categorical variables.
  - Build a binary logistic regression model using backward selection ($$ \alpha = 0.002 $$).
  - Rank final variables by $$ p $$-value and interpret one odds ratio as an example.
  - Investigate interactions through forward selection based on main effects.
  - Document interesting findings from odds ratios and interactions.

- **Deliverables**:
  - A business report detailing the final logistic regression model.
  - Ranked list of significant variables with interpretations.
  - Summary of interaction effects.

---

### **Phase 3: Model Assessment and Prediction**
- **Tasks**:
  - Evaluate the final logistic regression model using both training and validation datasets.
  - Report probability metrics:
    - Concordance percentage
    - Discrimination slope (coefficient of discrimination with visual representation)
  - Report classification metrics:
    - ROC curve
    - K-S statistic
    - Confusion matrix
    - Accuracy
    - Lift (with visual representation)
  - Provide actionable insights based on model performance.

- **Deliverables**:
  - A business report summarizing model performance.
  - Visualizations for ROC curve, discrimination slope, and lift chart.
  - Final confusion matrix with accuracy metrics.

---

## **Data Description**
The project uses two datasets provided by the bank:
1. **Training Dataset**:
   - Contains $$8,495$$ observations with $$48$$ variables.
   - Includes customer attributes before being offered the insurance product.
   - Target variable: `INS` (1 = purchased, 0 = not purchased).

2. **Validation Dataset**:
   - Contains $$2,124$$ observations with the same structure as the training dataset.

### **Variable Types**:
- Binary (e.g., `DDA`, `SAV`, `CC`): Indicators for specific accounts or services.
- Ordinal (e.g., `BRANCH`, `RES`): Branch or area classifications.
- Nominal (e.g., `MOVED`, `INAREA`): Categorical customer attributes.
- Continuous (e.g., `ACCTAGE`, `DDABAL`, `INCOME`): Numerical attributes like account age or balance.
