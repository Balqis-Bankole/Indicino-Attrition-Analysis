# Indicino Employee Attrition Analysis

Prepared by: Balqis Bankole  
Prepared for: Indicino Leadership Team

## 1. Client Background
Indicino is a digital payments company based in Accra, Ghana, operating a fully on-site work model with educational grants as part of its benefits package. Despite running several retention initiatives, the company experienced a significant rise in attrition, including the resignation of key employees. Leadership requested a data-driven review to identify the underlying causes and flag employees currently at risk.

The analysis covers 1,470 employee records across 35 fields, with no missing or duplicate records. Overall attrition was 16.1%, meaning approximately one in six employees left during the period represented in the dataset.

> Interpretation note: The findings identify associations in the employee data; they do not establish that any factor directly causes attrition.

---

## 2. North Star Metric

### Overall Attrition Rate — 16.1%

Overall attrition rate is the primary measure of retention performance and provides the baseline against which all other workforce segments should be evaluated.

Supporting indicators include:

- Attrition within high-risk roles and age groups
- Overtime-related attrition
- Early manager-tenure attrition
- Job satisfaction and involvement
- Predictive model precision and recall

Together, these measures allow leadership to monitor both the retention outcome and the workforce conditions associated with it.

---

## 3. Executive Summary

Attrition is concentrated around workload, career stage, employee experience and specific job roles.

Overtime showed the strongest association with attrition among the key risk factors examined, with attrition of 30.5% among employees working overtime compared with the 16.1% overall rate. Business travel, low job involvement and poor work-life balance were also associated with above-average attrition. When multiple risk conditions occurred together, observed attrition increased to 64–75% in the highest-risk combinations.

The 18–25 age group represents only 8.4% of the workforce but shows the highest sensitivity to overtime: attrition reaches 64.1% among employees in this age group who work overtime, compared with 22.6% among those who do not.

Risk is also concentrated in specific roles. Sales Representatives and Laboratory Technicians consistently show the highest observed attrition. Sales Representatives working overtime have an attrition rate of 66.7%.

Employee experience is another important signal. Attrition among employees with their current manager for 0–2 years is 21.4%, compared with 4.1% among those with 11 or more years under the same manager. Job involvement and job satisfaction also show inverse relationships with attrition.

Compensation findings suggest that pay alone may not be sufficient as a retention strategy. Higher-performing employees receive substantially larger salary increases, but attrition is almost identical among performance ratings 3 and 4 (16.1% vs. 16.4%). Employees who left also earned approximately 30% less on average than those who stayed.

---

# 4. Key Findings

## 4.1 Risk Factors Compound

<img width="2720" height="1680" alt="attrition_risk_factor_flow" src="https://github.com/user-attachments/assets/348416fd-68d9-4f78-a28d-d5c2f2bba2c9" />

Four conditions examined were associated with attrition above the company baseline: overtime (30.5%), frequent business travel (24.9%), low job involvement (33.7%) and poor work-life balance (31.2%).

When multiple risk conditions occur together, observed attrition rises sharply, reaching 64–75% in the highest-risk combinations. Overtime consistently appears alongside some of the highest observed attrition rates, making workload conditions an important area for further investigation.

---

## 4.2 Highest-Risk Segment: Young Employees Working Overtime

<img width="1947" height="649" alt="Screenshot 2026-08-25 at 23 51 53 2" src="https://github.com/user-attachments/assets/e7ed8033-39f9-485c-9f76-8ba66461f2a6" />


Employees aged 18–25 represent 8.4% of the workforce, but show the greatest sensitivity to overtime. Attrition rises from 22.6% among those who do not work overtime to 64.1% among those who do.

No other age group shows a comparable difference.

This makes early-career employees an important segment for further investigation, particularly where workload pressures are present.

---

## 4.3 Job Roles Requiring Attention

Sales Representatives and Laboratory Technicians consistently show the highest observed attrition across the role analysis. Sales Representatives working overtime have an attrition rate of 66.7%, further highlighting the interaction between role and workload.

These roles should therefore be prioritised for deeper investigation into workload, career progression, performance expectations and employee experience.

---

## 4.4 Manager Tenure and Attrition

Attrition among employees in their first two years with a manager stands at 21.4%, compared with 4.1% among employees with 11 or more years under the same manager.

The relationship between manager tenure and attrition, alongside the stronger overtime and travel patterns observed during earlier manager relationships, indicates that the first years of a manager-employee relationship warrant closer attention.

---

## 4.5 Satisfaction and Involvement

Job Satisfaction and Job Involvement show consistent inverse relationships with attrition. Employees with the lowest involvement rating have an attrition rate of 33.7%, compared with 9.0% among those with the highest rating.

For job satisfaction, the corresponding rates are 22.8% and 11.3%.

These findings reinforce the importance of monitoring employee experience alongside operational factors such as workload.

---

## 4.6 Compensation and Performance

<img width="890" height="1019" alt="Screenshot 2026-08-25 at 23 55 48" src="https://github.com/user-attachments/assets/c9299344-f085-44bd-8b23-e6f065b684d0" />

Employees rated 4 receive an average salary increase of 21.85%, compared with 14.00% for employees rated 3, indicating that performance-based salary increases are being differentiated as intended.

However, attrition is almost identical between the two groups (16.4% vs. 16.1%). Separately, employees who left earned approximately 30% less on average than those who stayed.

This suggests that lower income is associated with higher attrition, while salary increases alone do not appear sufficient to distinguish retention among higher-performing employees. Compensation should therefore be considered alongside career progression, manager support and employee engagement.

---

# 5. Predictive Outlook

<img width="1130" height="917" alt="Screenshot 2026-08-25 at 23 51 53 3" src="https://github.com/user-attachments/assets/184d6ced-5912-44c9-b8c2-1c6711f7d91f" />


A logistic regression model was developed to demonstrate how employee-level attrition risk can be identified from workforce characteristics. SMOTE was applied to the training data to address class imbalance.

The model achieved:

- Accuracy: 77%
- Recall: 74%
- Precision: 46%

Recall was prioritised because failing to identify a potentially at-risk employee may be more costly than initiating an unnecessary retention conversation.

For the highlighted roles, predicted risk was higher than the corresponding historical attrition rate:

| Job Role | Historical Attrition | Predicted Risk |
|---|---:|---:|
| Sales Representative | 39.8% | 68.4% |
| Laboratory Technician | 23.9% | 56.8% |
| Human Resources | 23.1% | 50.0% |
| Sales Executive | 17.5% | 39.4% |
| Research Scientist | 16.1% | 35.9% |

These results suggest that the employee characteristics represented in the model contain substantial concentrations of predicted risk within these roles. They should not be interpreted as proof that attrition is increasing over time.

The age pattern is also reflected in the model: the 18–25 group has the lowest predicted retention (34.6%), while the 46–55 group has the highest (87.0%).

With precision at 46%, predictions should be used to prioritise retention conversations and further investigation rather than to label employees as certain leavers.

---

# 6. Recommended Actions

### 1. Address overtime at its source

Audit staffing levels, workload allocation and scheduling in teams with persistent overtime. The priority should be reducing the conditions creating excessive overtime rather than simply monitoring hours.

### 2. Strengthen early-career retention

Introduce structured mentorship, clearer promotion pathways and regular development conversations for employees aged 18–25 and Job Level 1 employees.

### 3. Target high-risk roles

Review workload, performance expectations, career progression and employee experience within Sales Representative and Laboratory Technician roles.

### 4. Strengthen new manager-employee relationships

Introduce structured onboarding and regular check-ins during the first two years of a manager-employee relationship, when observed attrition is substantially higher.

### 5. Review travel and employee experience

Assess whether frequent business travel is creating workload or work-life-balance pressures, particularly where travel overlaps with overtime.

### 6. Treat compensation as one part of retention

Compensation reviews should be accompanied by investment in career progression, manager support and employee engagement. The analysis does not indicate that salary increases alone are sufficient to address attrition.

> Interpretation note: This analysis identifies associations rather than proven causes. Findings should be treated as evidence-based starting points for further investigation, and predictive outputs should support—not replace—managerial judgement.

---

## Tools & Technical Documentation

Tools: Python · pandas · NumPy · scikit-learn · Logistic Regression · SMOTE · seaborn · matplotlib

Technical documentation: The complete data-cleaning, exploratory analysis, feature engineering, model development and evaluation workflow is documented in Indicino.ipynb.
