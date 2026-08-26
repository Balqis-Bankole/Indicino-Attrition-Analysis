# Indicino Employee Attrition Analysis

Prepared by: Balqis Bankole  
Prepared for: Indicino Leadership Team

## 1. Client Background

Indicino is a digital payments company based in Accra, Ghana. The company operates a fully on-site work model and offers educational grants to eligible employees as part of its benefits package.

Despite existing retention initiatives, Indicino experienced significant employee attrition, including the departure of key employees. Leadership requested a data-driven review to identify the factors associated with employee attrition, determine which employee segments face the highest observed risk, and identify where retention efforts should be prioritised.

Objective: Identify the key factors associated with employee attrition and develop evidence-based recommendations to improve retention.

---

## 2. North Star Metric

Primary Metric: Overall Attrition Rate — 16.1%

Overall attrition rate is the primary measure of retention performance and provides the baseline against which all other workforce segments should be evaluated.

Supporting indicators include attrition within high-risk segments, overtime-related attrition, early manager-tenure attrition, job satisfaction and involvement, and predictive model performance. Together, these measures allow leadership to monitor both the retention outcome and the workforce conditions associated with it.

---

## 3. Executive Summary

This analysis identifies several workforce conditions and employee segments associated with higher attrition at Indicino.

Overtime showed the strongest association with attrition among the key risk factors examined, with attrition of 30.5% compared with the 16.1% overall rate. Business travel, low job involvement and poor work-life balance were also associated with above-baseline attrition. When multiple risk conditions occurred simultaneously, observed attrition reached 64–75% in the highest-risk combinations.

The strongest concentration of risk appears among early-career employees and specific operational roles. Employees aged 18–25 account for only 8.4% of the workforce, yet attrition reaches 64.1% among those working overtime, compared with 22.6% among those who do not. Sales Representatives and Laboratory Technicians also show the highest observed attrition across the role analysis.

Manager tenure provides another important signal. Employees in their first two years with a manager have an attrition rate of 21.4%, compared with 4.1% among employees with 11 or more years under the same manager.

Compensation alone does not appear sufficient to explain retention. Although employees rated 4 receive substantially larger salary increases than those rated 3, attrition between the two groups is almost identical. Employees who left also earned approximately 30% less on average than those who stayed.

A logistic regression model was developed to demonstrate how employee-level attrition risk can be identified. The model achieved 77% accuracy, 74% recall and 46% precision. Its predictions highlight substantial concentrations of risk within several job roles and reinforce the observed age-related pattern.

The findings point towards a retention strategy focused on workload management, early-career support, high-risk roles, manager relationships and employee experience, rather than relying on compensation increases alone.

---

## 4. Data Structure

The analysis is based on a single employee-level dataset containing 1,470 records and 35 fields, with no duplicate or missing values. The dataset represents one record per employee, with Attrition as the outcome variable.

The fields cover demographics, job and career characteristics, compensation, satisfaction and engagement, work conditions and manager relationships.

The dataset required minimal cleaning before analysis. Full data preparation, exploratory analysis and modelling are documented in Indicino.ipynb.

---

# 5. Insight Deep Dive

## 5.1 Scale of Attrition

<img width="739" height="882" alt="waffle_attrition" src="https://github.com/user-attachments/assets/9673340e-8fe4-4888-a6eb-f5b52fc6e379" />


Approximately one in six employees left Indicino, establishing a 16.1% baseline for evaluating the segments and conditions associated with higher attrition.

---

## 5.2 Risk Factors Compound

<img width="2720" height="1680" alt="attrition_risk_factor_flow" src="https://github.com/user-attachments/assets/2c5691cc-7e07-471a-a839-26d4ef2232a1" />


Four conditions examined were associated with attrition above the company baseline: overtime (30.5%), frequent business travel (24.9%), low job involvement (33.7%) and poor work-life balance (31.2%).

When multiple conditions occur together, observed attrition rises sharply, reaching 64–75% in the highest-risk combinations. Overtime consistently appears alongside some of the highest observed attrition rates, making workload conditions an important area for further investigation.

---

## 5.3 Highest-Risk Segment: Young Employees Working Overtime



Employees aged 18–25 represent 8.4% of the workforce, but show the greatest sensitivity to overtime. Attrition rises from 22.6% among those who do not work overtime to 64.1% among those who do.

No other age group shows a comparable difference. This suggests that early-career employees may require particular attention where workload pressures are present.

---

## 5.4 Job Roles Requiring Attention

<img width="1710" height="1112" alt="Screenshot 2026-08-26 at 13 22 57" src="https://github.com/user-attachments/assets/aebd671b-7862-4bf5-924f-9e872975f2a0" />


Sales Representatives and Laboratory Technicians show the highest observed attrition across the role analysis. Sales Representatives working overtime have an attrition rate of 66.7%, further highlighting the interaction between role and workload.

These roles should therefore be prioritised for deeper investigation into workload, career progression, performance expectations and employee experience.

---

## 5.5 Manager Tenure and Attrition

[Insert Chart: Attrition by Years with Current Manager]

Attrition among employees in their first two years with a manager is 21.4%, compared with 4.1% among employees with 11 or more years under the same manager.

The relationship between manager tenure and attrition, alongside the stronger overtime and travel patterns observed during earlier manager relationships, indicates that the first years of a manager-employee relationship warrant closer attention.

---

## 5.6 Satisfaction and Involvement
<img width="1710" height="1112" alt="Screenshot 2026-08-25 at 16 10 36" src="https://github.com/user-attachments/assets/70548e25-e7b1-40a3-95f9-c8770e237e65" />


Job Satisfaction and Job Involvement show consistent inverse relationships with attrition. Employees with the lowest involvement rating have an attrition rate of 33.7%, compared with 9.0% among those with the highest rating. For job satisfaction, the corresponding rates are 22.8% and 11.3%.

These findings reinforce the importance of monitoring employee experience alongside operational factors such as workload.

---

## 5.7 Compensation and Performance

<img width="1710" height="1112" alt="Screenshot 2026-08-26 at 13 23 55" src="https://github.com/user-attachments/assets/ef79305e-b2bd-4598-807d-936df6769022" />


Employees rated 4 receive an average salary increase of 21.85%, compared with 14.00% for employees rated 3, indicating that performance-based salary increases are being differentiated as intended.

However, attrition is almost identical between the two groups (16.4% vs. 16.1%). Separately, employees who left earned approximately 30% less on average than those who stayed.

This suggests that lower income is associated with higher attrition, while salary increases alone do not appear sufficient to distinguish retention among higher-performing employees. Compensation should therefore be considered alongside career progression, manager support and employee engagement.

---

## 5.8 Predictive Outlook

A logistic regression model was developed to demonstrate how employee-level attrition risk can be identified from workforce characteristics. SMOTE was applied to the training data to address class imbalance.

The model achieved 77% accuracy, 74% recall and 46% precision. Recall was prioritised because failing to identify an employee who may be at risk can be more costly than initiating an unnecessary retention conversation.

For the highlighted roles, predicted risk is higher than the corresponding historical attrition rate:

| Job Role | Historical Rate | Predicted Risk |
|---|---:|---:|
| Sales Representative | 39.8% | 68.4% |
| Laboratory Technician | 23.9% | 56.8% |
| Human Resources | 23.1% | 50.0% |
| Sales Executive | — | 39.4% |
| Research Scientist | 16.1% | 35.9% |

These results indicate that the employee characteristics represented in the model contain substantial concentrations of predicted risk within these roles. They should not be interpreted as evidence that attrition is increasing over time.

The model also reinforces the age-related pattern: employees aged 18–25 have the lowest predicted retention (34.6%), while employees aged 46–55 have the highest (87.0%).

With precision at 46%, predictions should be used to prioritise retention conversations and further investigation rather than to label employees as certain leavers.

---

# 6. Recommendations

| Risk Segment | Recommended Action |
|---|---|
| Sales Representatives | Review workload, targets and career progression |
| 18–25 age group | Introduce early-career mentorship and clearer development pathways |
| Overtime-heavy teams | Audit staffing and workload allocation to address the underlying causes of overtime |
| New manager-employee relationships | Strengthen onboarding and regular check-ins during the first two years |
| Frequent travellers | Assess travel volume and its impact on workload and work-life balance |
| Job Level 1 employees | Review progression speed and access to development opportunities |

Any compensation review undertaken by Indicino should be accompanied by investment in career progression, manager support and employee engagement. The evidence suggests that pay increases alone are unlikely to address the broader attrition pattern.

### Interpretation Note

This analysis identifies associations rather than proven causes. Findings should be treated as evidence-based starting points for further investigation. The predictive model should be used to prioritise retention conversations and not replace managerial judgement.

Tools Used: Python · pandas · NumPy · scikit-learn · Logistic Regression · SMOTE · seaborn · matplotlib

Technical documentation: Indicino.ipynb contains the complete data-cleaning, exploratory analysis, feature engineering, modelling and evaluation workflow.
