# Employee Attrition Analytics — Indicino

**Why is Indicino losing people, who is leaving next, and what should HR do about it?**

*by Balqis Bankole*

---

## 1. Business Context

Indicino is a digital payments company based in Accra, Ghana, operating a fully on-site work model and offering staff educational grants. Despite already running several retention initiatives, the company has recently lost a number of key staff and overall attrition has risen. Leadership needs to know why people are leaving, who is likely to leave next, and what is actually worth doing about it.

This project uses 1,470 employee records across 35 attributes covering demographics, compensation, satisfaction, and tenure.

---

## 2. North Star Metrics

This analysis is organised around three metrics. Each one answers a different question a stakeholder actually asks, and together they move from "how bad is it" to "why" to "where do we act first."

| # | North Star Metric | Definition | Why this metric |
|---|---|---|---|
| 1 | **Overall Attrition Rate** | (Employees who left ÷ Total employees) × 100 | This is the number the CEO and board will ask about every quarter. It provides the overall measure of employee attrition and serves as the baseline for assessing attrition across different employee groups. |
| 2 | **Overtime Attrition Gap** | Attrition rate among employees who work overtime − attrition rate among those who don't | Measures the difference in attrition between employees who work overtime and those who do not. It provides a focused measure of the relationship between working patterns and employee attrition. |
| 3 | **Predicted High-Risk Concentration** | Average model-predicted attrition rate across the job roles identified as highest risk by the model | HR has finite time and budget. This metric converts the company’s problem into an ordered shortlist of where an intervention will do the most good per hour invested. |

---

## 3. Executive Recommendations

| Finding | Owner | Recommendation |
|---|---|---|
| **Overtime triples attrition (31% vs 10%) in every segment tested** | COO / Line managers + HR Business Partners | Treat sustained overtime as a sign that workload or staffing may need review. Assess workload and staffing in teams with consistently high overtime, then consider hiring, redistributing work or adjusting targets. |
| **18–25-year-olds on overtime attrite at 64%, vs 23% for their peers who aren't** | Group Head of HR / L&D | Introduce additional support for early career employees, including structured first year onboarding, an assigned mentor and closer monitoring of overtime for entry level roles. |
| **Sales Representatives, Lab Technicians and HR staff are the three roles the model consistently flags highest, both in actual and predicted attrition** | Sales, Lab and HR function heads | Prioritise these roles for stay interviews. Focus on workload, targets and manager support to understand what is driving turnover before introducing broader retention initiatives. |
| **Frequent travel is a compounding risk, especially for employees who are new to their manager (0–2 years: 34.6% attrition vs 5.6% at 11+ years)** | Group Head of HR + role-specific line managers | Give new manager–employee pairs a lighter travel schedule in the first two years, or pair frequent travellers with more senior managers with strong retention record. |
| **Attrition falls from 21.4% to 4.1% as time with the current manager increases from 0–2 years to 11+ years.** | People leaders / L&D | Invest in new-manager onboarding and relationship-building (regular 1:1s, clear expectations) in the first two years of a reporting relationship. This is a lower-cost lever than compensation and shows a larger effect size in this data. |
| **Higher performance ratings receives larger salary increases (21.9% vs 14.0% average hike) but attrition remains almost the same (16.4% vs 16.1% — statistically flat)** | Total Rewards / Compensation | Continue recognising performance through salary increases, but do not rely on salary increases alone to improve retention. Give greater attention to competitive pay, career progression, employee involvement and recognition throughout the year. |
| **The predictive model over-estimates every role's attrition rate relative to what actually happened (e.g. Sales Rep: 68% predicted vs 40% actual)** | Data/Analytics team + whoever consumes the dashboard | Use the model to identify which roles need attention rather than treating the predicted percentages as forecasts. Consider the model’s precision and recall when interpreting the results. |

---

## 4. Key Insights

### 4.1 The headline number, in context

<img width="739" height="882" alt="waffle_attrition" src="https://github.com/user-attachments/assets/6b852d65-3f53-4f3a-8710-e383509fb73e" />
Indicino's overall attrition rate is **16.1% (237 of 1,470 employees)**. On its own, that number is only mildly concerning: recent industry benchmarking (Mercer's 2025 U.S. turnover survey) puts average voluntary turnover around 13%, with financial-services-adjacent sectors like insurance running closer to 8%, and higher-turnover sectors like retail well above 25%. As a payments company, Indicino sits somewhere between those poles, so 16.1% is elevated but not alarming in aggregate.

The reason this project doesn't stop at the headline number is that an aggregate rate hides where the real damage is happening. When the same 16.1% is broken apart by overtime status, job role, age and manager relationship, some segments are running **three to five times** the company average, while others sit near zero. A single blended KPI tells leadership that something is wrong; it can't tell them what to fix or who to protect first. That's the gap the rest of this analysis closes.

### 4.2 The overtime trap: Indicino's single strongest, most controllable driver
<img width="349" height="324" alt="32629518-05ec-4bce-8d3b-4cc21399c0c2 3" src="https://github.com/user-attachments/assets/395c20bf-6d8d-45da-8f95-8a77ce609c36" />

Employees who work overtime leave at **30.5%**, compared with **10.4%** for those who don't — roughly a 3x gap, and the 2nd largest single effect of any variable tested in this dataset. Crucially, this isn't a fluke confined to one group: the same gap reappears, with the same direction, inside every slice examined —

- across every **work–life balance** level (worst case: poor balance + overtime → **45.5% attrition**),
- across every **environment satisfaction** level (worst case: lowest satisfaction + overtime → **51.6%**),
- across every **job involvement** level (worst case: lowest involvement + overtime → **52.0%**),
- across every **job level** (Job Level 1 jumps from **26.3%** without overtime to **52.6%** with it), and
- across every **age band** (18–25-year-olds jump from **22.6%** to **64.1%**).

The "so what" here is important: a variable that only matters for one niche group is a nuance; a variable that consistently doubles or triples attrition everywhere it appears is a structural problem, not a coincidence of who happens to work overtime. That consistency is exactly why the Overtime Attrition Gap was chosen as a core metric. It shows that it is an important area for management to investigate.

What's likely driving it isn't overtime itself but what overtime signals: understaffing, unrealistic targets, or a role where the workload structurally exceeds the hours allotted for it. Indicino has already tried multiple retention initiatives without reducing attrition, which suggests that employee engagement alone may not be enough to address the problem If workload and staffing pressures are contributing to overtime, these underlying issues also need to be addressed as part of the retention strategy.

**So what should Indicino do?**

Overtime should be treated as a staffing and workload issue, not simply an HR issue. Line managers and the COO's team should should monitor sustained overtime as a signal that a team may be under-resourced or facing unrealistic workloads. When overtime remains high, the response should be to review staffing levels, redistribute work or reassess targets. HR can support this by identifying which teams and roles have consistently high overtime and providing the data needed to guide these decisions.

### 4.3 The early-career cliff: age, tenure, and who bears the overtime cost

<img width="1947" height="649" alt="Screenshot 2026-08-25 at 23 51 53 2" src="https://github.com/user-attachments/assets/b847e02e-5865-477b-bce9-8a2f36d0cd1b" />
Attrition is not evenly distributed by age. Employees aged **18–25 leave at 35.8%** — roughly double the company average, and by far the highest of any age band — while attrition falls to its lowest point at **36–45 (9.2%)** before edging back up slightly for older bands (46–55: ~12%, 55+: ~17%).

The age difference becomes more important when considered alongside overtime. An 18–25-year-old working overtime leaves at **64.1%**, nearly three times the rate of a same-age peer who isn't (**22.6%**). This is precisely the population least likely to have built the internal relationships, financial cushion, or role security to tolerate sustained overload — so it makes intuitive business sense that this is where the overtime effect is most extreme, and it's corroborated by the model's own predictions: the classifier separately estimates the **18–25 band has the lowest predicted retention of any age group (34.6%)**, versus **87.0% for 46–55-year-olds**.

This matters commercially, not just sentimentally: early-career hires are the cheapest to recruit but arguably the most expensive to lose, because Indicino has typically not yet recouped the ramp-up investment (training, onboarding, lost productivity during the learning curve) before they walk out the door. Losing a 24-year-old six months after onboarding is a pure sunk cost; losing a 15-year veteran, while still painful, is a smaller proportional loss relative to what the company has already extracted in value.

**So what should Indicino do?**

Indicino should give early-career employees specific retention support rather than relying on its general engagement initiatives. This could include a structured first-year onboarding programme, an assigned mentor in addition to their manager, and closer monitoring of overtime for entry-level employees. The overtime finding is particularly important for this group, where 18–25-year-olds working overtime have an attrition rate of 64.1%.

### 4.4 Frequent travel: a second lever that compounds with the first

Employees who travel frequently for work leave at **25%**, compared with **15%** for those who travel rarely and just **8%** for those who don't travel at all — attrition rises with travel frequency. The relationship remains evident even among employees with the highest job satisfaction: frequent travellers have **17.2% attrition**, compared with **2.3%** among satisfied employees who do not travel. This suggests that job satisfaction alone may not offset the challenges associated with travelling frequently, such as reduced personal time and disruption to work–life balance.

The more useful version of this insight, comes from combining it with tenure under a manager (see 5.5 below): frequent travel is at its worst for employees who are still new to their manager. Employees with 0–2 years under their current manager who also travel frequently leave at **34.6%**, versus **5.6%** for frequent travellers who've had 11+ years with the same manager. In other words, travel is a manageable trade-off once a strong manager relationship exists to absorb it, but a serious risk multiplier when it's stacked on top of a relationship that hasn't had time to build trust or support.

**So what should Indicino do?**

Indicino should consider how frequent travel affects employees who are new to their manager. Where possible, employees in their first two years with a manager could have a lighter travel schedule. Another option is to assign frequent travellers to managers with strong retention records. The data suggests that the manager relationship may influence how well employees cope with frequent travel.

### 4.5 The manager relationship is Indicino's strongest protective factor

Manager tenure is strongly associated with employee retention. Attrition falls steadily as employees spend more time with their current manager, from **21.4% among employees with 0–2 years under their current manager to 4.1% among those with 11+ years** — a more than 5x difference.

This single variable also helps explain why the other two risk factors (Overtime and Business travel) have a greater impact on some employees than others. As shown above, both overtime and frequent travel are dramatically worse for employees with a new manager (overtime: 0–2 years → **39.0% attrition vs 11+ years → 10.5%**; frequent travellers: 0–2 years → **34.6% vs 11+ years → 5.6%**) than for employees with a long-standing one. A strong, established manager relationship appears to buffer employees against the two biggest structural stressors in this company — workload and travel demands. Newer manager–employee relationships may not yet have developed the trust, context, or support needed to make heavy demands feel survivable.

**So what should Indicino do?**

Strengthening manager relationships may be a more practical and lower cost option than reducing workload or travel. Indicino can support new manager and employee relationships through regular one to one meetings, clear expectations and HR check ins during the first 6 to 12 months. This is especially important because attrition is higher when employees are new to their manager and are also exposed to overtime or frequent travel.

### 4.6 Who to prioritise

<img width="526" height="411" alt="32629518-05ec-4bce-8d3b-4cc21399c0c2 2" src="https://github.com/user-attachments/assets/96f17b96-67ea-4a5d-b93c-82b2be356431" />

Combining actual attrition rates with a predictive model provides a clear view of which roles require attention. A logistic regression classifier was used to predict individual attrition risk and these predictions were then analyzed by job role. Three roles stand out consistently in both the actual data and the model's predictions:

| Job Role | Actual Attrition Rate | Model-Predicted Attrition Rate |
|---|---:|---:|
| Sales Representative | 40% | 68.4% |
| Laboratory Technician | 24% | 56.7% |
| Human Resources | 23% | 50.0% |
| Sales Executive | 17% | 39.4% |
| Research Scientist | 16% | 35.9% |
| Manufacturing Director | 7% | 14.8% |
| Research Director | 3% | 16.7% |
| Healthcare Representative | 7% | 11.5% |
| Manager | 5% | 0% |

Two things are true at once here. First, the ranking is genuinely useful and worth acting on: Sales Representatives, Lab Technicians and HR staff are the highest-risk roles by both measures, and both Sales Representative overtime attrition (66.7%) and Lab Technician overtime attrition (50%) are also among the highest when overtime attrition is assessed by job roles, reinforcing again, that these roles are where overtime is doing the most damage. Second, the model's absolute numbers should not be read literally: it over-predicts attrition for most roles, sometimes by close to 2x (Research Director: 3% actual vs 16.7% predicted). This is linked to the modelling approach: SMOTE was used to balance the training data so the model would be more likely to identify employees who may leave. This helped the model achieve 74% recall, but reduced precision to 46%. In practical terms, fewer than half of the employees the model identifies as being at risk actually leave.

**So what should Indicino do?**

The model should be used to prioritise which roles need attention, not as a forecast of how many employees will leave. For example, the results indicate that Sales Representatives should receive attention before Managers, but the 68% predicted rate does not mean that 68% of Sales Representatives will resign. HR should use the model alongside other information, such as manager feedback and exit interview themes, before deciding where to focus retention efforts. The model’s precision and recall should also be considered alongside the predicted rates so that the results are interpreted appropriately.

### 4.7 Pay recognises performance — but It is not reducing Attrition

<img width="455" height="422" alt="32629518-05ec-4bce-8d3b-4cc21399c0c2" src="https://github.com/user-attachments/assets/5306b037-d148-4492-afcc-b1c971ded322" />

Indicino's reward system is doing exactly what it's designed to do on the compensation side: employees rated 4 receive an average salary increase of **21.85%**, nearly 8 points higher than the **14.00%** average for employees rated 3 (who make up 84.6% of the workforce). Performance is being financially recognised, and clearly so.

What the data shows just as clearly is that this recognition isn't buying retention. Attrition is statistically flat across both performance groups — **16.1% for rating-3 employees versus 16.4% for rating-4 employees** — and the average salary hike is nearly identical between employees who stayed (**15.23%**) and those who left (**15.10%**). A larger salary increase does not appear to meaningfully reduce an employee’s likelihood of leaving. The same pattern can be seen in promotion timing: employees with a performance rating of 4 have gone slightly longer since their last promotion, averaging **2.32 years** compared with **2.16 years** for employees rated 3. This suggests that higher performance is being rewarded through salary increases, but is not necessarily being reflected in faster career progression.

The difference becomes clearer when we look at what does separate employees who leave from those who stay. Monthly income is one of them: employees who stayed earn an average of **$6,833 per month**, compared with **$4,787** among those who left — around 30% higher. Job satisfaction and involvement also show a clear difference: attrition is **22.8%** among employees with the lowest job satisfaction, compared with **11.3%** among those with the highest. For job involvement, the difference is even larger, at **33.7%** for the lowest level compared with **9.0%** for the highest.

This suggests that overall pay level and employees’ day-to-day experience at work may have a stronger relationship with retention than the size of their annual salary increase. Indicino is rewarding higher performance financially, but the evidence points to other areas — competitive pay, job satisfaction and employee involvement — as more relevant to keeping employees.

**So what should Indicino do?**

This should be considered as part of Indicino’s wider reward strategy. The findings suggest that larger salary increases for higher performers are not enough to improve retention. Indicino should also focus on competitive base pay, career progression, employee involvement and recognition throughout the year. These areas show greater potential for supporting retention than relying on performance based salary increases alone.

### 4.8 The composite picture: who is Indicino's highest-risk employee?

Looking across the findings, the employees at greatest risk of attrition share several characteristics. They are young employees aged 18 to 25, work in higher risk roles such as Sales, Laboratory and HR, work overtime, travel frequently and have been with their current manager for less than two years. Each of these factors is associated with higher attrition, with some showing rates two to five times the company average.

The concentration of these risk factors provides Indicino with a clear group to prioritise for retention efforts. Employees facing a combination of high workloads, frequent travel, limited time with their manager and higher risk roles should receive targeted support, rather than relying on a single retention approach across the entire workforce.

---

## 5. Methodology and Model

**Data cleaning:** the raw data contained 1,470 rows and 35 columns. Column names were cleaned to remove leading and trailing spaces, and the inconsistently formatted JobInvolvement field (stored as text with stray characters) was corrected. Three constant-value columns (EmployeeCount, Over18, StandardHours) were removed along with the ID column because it had no analytical value.

**Modelling approach:** Attrition was framed as a binary classification problem (Attrition = Yes/No) and modelled with Logistic Regression. Categorical features were one-hot encoded and numeric features standardised via a ColumnTransformer, fit only on the training split (80/20) to avoid leakage. Because only ~16% of employees in the training data had left, SMOTE was applied to the training set only (never the test set) to prevent the model from simply defaulting to "predict everyone stays."

**Model performance:** The model achieved **77% accuracy, 74% recall, 46% precision and an F1 score of 0.57**. The model was designed to prioritise recall because, in a retention context, identifying employees who may leave is more important than avoiding every false alert. As a result, the predicted attrition percentages should be interpreted as a way to rank risk rather than as exact probabilities.

**Tools used:** Python (pandas, NumPy, seaborn/matplotlib for EDA, scikit-learn for modelling, imbalanced-learn for SMOTE), Tableau for the executive dashboard.

The full technical workflow — data cleaning, exploratory analysis, feature engineering, and model evaluation — is documented in `Indicino.ipynb`.
