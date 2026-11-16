# Human Resource Analytics Dashboard

A business-focused HR analytics project that turns employee and performance-review data into insights about workforce composition, employee retention, compensation, and the employee experience.

The goal of this project is not simply to report how many employees the organization has. It is to help HR leaders and business managers understand **where workforce risks are concentrated, which employee groups may need attention, and where people practices can be improved.**

## Business objectives

This analysis is designed to help answer five practical HR questions:

1. **Who makes up the workforce?** Understand headcount by department, role, age group, gender, ethnicity, education, location, and other employee attributes.
2. **Where is employee attrition concentrated?** Compare attrition across departments, job roles, and overtime groups to identify areas for retention action.
3. **How is the workforce changing?** Review hiring patterns and employee tenure to understand workforce growth and experience levels.
4. **How are employees experiencing work?** Examine satisfaction, work-life balance, relationship ratings, and performance feedback.
5. **Where can HR investigate further?** Use the findings to prioritize retention conversations, workload reviews, career development, and training effectiveness.

## Key findings at a glance

The following figures are calculated directly from the supplied CSV files. Percentages are rounded to one decimal place unless otherwise stated.

| Measure | Result |
|---|---:|
| Employees in the employee dataset | **1,470** |
| Employees marked as attrition = Yes | **237** |
| Overall dataset attrition share | **16.1%** |
| Average age | **29.0 years** |
| Median age | **26 years** |
| Average company tenure | **4.6 years** |
| Average salary (as recorded in the source data) | **112,956.50** |
| Performance review records | **6,709** |
| Employees represented in performance reviews | **1,280** |
| Performance review date range | **2013–2022** |

> **How to interpret the attrition figure:** 237 divided by 1,470 gives 16.1%. This is the share of employee records marked as having attrited in this dataset. It should not automatically be interpreted as an annual attrition rate, because the supplied employee file does not provide a consistent period-specific active-employee denominator.

## Business insights

### 1. Retention risk is not evenly distributed

- **Sales has the highest department-level attrition share at 20.6%** (92 of 446 employees).
- Human Resources records 19.0% (12 of 63), while Technology records 13.8% (133 of 961).
- Technology has the largest number of attrition records (133) because it is also the largest department. Sales has the higher rate, which is a different and important signal.
- By job role, Sales Representatives have the highest observed attrition share: **39.8% (33 of 83)**. Recruiters follow at **37.5% (9 of 24)**. These role-level results should be interpreted with their group sizes in mind.
- Data Scientists record 23.8% attrition (62 of 261).

**Business implication:** Prioritize retention analysis in Sales, especially Sales Representative roles. Review role expectations, manager support, workload, career progression, and compensation competitiveness before deciding on interventions. Smaller groups such as Recruiters should be investigated carefully rather than treated as conclusive evidence.

### 2. Overtime is a strong retention signal in this dataset

| Overtime status | Employees | Attrition records | Attrition share |
|---|---:|---:|---:|
| Overtime: Yes | 416 | 127 | **30.5%** |
| Overtime: No | 1,054 | 110 | **10.4%** |

Employees marked as working overtime have an attrition share approximately **2.9 times** that of employees not marked as working overtime (30.5% versus 10.4%).

**Business implication:** Examine overtime patterns by team, role, and manager. Capacity planning, workload distribution, scheduling, and employee well-being are sensible areas for follow-up. This is an association in the supplied data, not proof that overtime causes employees to leave.

### 3. The workforce is concentrated in Technology and early-career age groups

- Technology accounts for **961 employees (65.4%)**, Sales for 446 (30.3%), and Human Resources for 63 (4.3%).
- Employees aged 20–29 make up **874 people (59.5%)**.
- The 30–39 age group represents 289 employees (19.7%), and the 40–49 group represents 219 (14.9%).
- Average age is 29 years and median age is 26 years.

**Business implication:** The organization has a relatively young workforce and a large Technology function. Career pathways, technical skill development, mentoring, and progression opportunities may be important retention levers. These should be evaluated alongside employee feedback rather than assumed to be the cause of attrition.

### 4. Workforce representation should be considered in context

- The dataset contains 675 female employees (45.9%), 651 male employees (44.3%), 124 non-binary employees (8.4%), and 20 employees who selected “Prefer Not To Say” (1.4%).
- The largest ethnicity category in the data is White (860 employees; 58.5%), followed by Black or African American (207; 14.1%) and Mixed or multiple ethnic groups (198; 13.5%).

**Business implication:** These breakdowns provide a starting point for monitoring workforce representation. They should be interpreted respectfully and in context; demographic differences alone do not explain employee outcomes.

### 5. Satisfaction scores leave room for improvement

Across the 6,709 performance-review records, the average scores (on the source's 1–5 rating scale) are:

| Review measure | Average score |
|---|---:|
| Environment satisfaction | **3.87 / 5** |
| Job satisfaction | 3.43 / 5 |
| Relationship satisfaction | 3.43 / 5 |
| Work-life balance | 3.41 / 5 |
| Self rating | 3.98 / 5 |
| Manager rating | 3.47 / 5 |

Environment satisfaction has the highest average among the listed experience measures, while work-life balance is the lowest. Self ratings are also higher on average than manager ratings (3.98 versus 3.47).

**Business implication:** Work-life balance and the difference between self and manager assessments are useful topics for deeper review conversations, manager calibration, and employee listening. The averages summarize review records, not necessarily unique employees.

### 6. Training participation merits a closer look

- The average number of training opportunities available per review record is **2.01**.
- The average number of opportunities taken is **1.02**.
- **2,372 review records (35.4%)** show zero training opportunities taken.

The aggregate average taken-to-available ratio is approximately **50.5%** (1.02 divided by 2.01, using unrounded averages).

**Business implication:** Investigate whether employees have sufficient time, relevant course options, manager encouragement, and access to training. The zero-taken figure is based on review records, so it is not a count of unique employees who never attended training.

### 7. Tenure suggests an opportunity to strengthen early employee experience

- Average company tenure is **4.6 years** and median tenure is 4 years.
- 491 employees (33.4%) have been at the company for two years or less.
- 587 employees fall in the 6–10 years tenure range.

**Business implication:** Strengthen onboarding and the first-two-year employee experience, while also maintaining development and progression opportunities for longer-serving employees.

## Dashboard pages

The supplied Power BI report contains four pages:

| Page | Business focus |
|---|---|
| **Overview** | High-level workforce view and headline indicators |
| **Demographics** | Employee composition across demographic and organizational categories |
| **Performance Tracker** | Employee-level performance and review trends, including a selectable employee view |
| **Attrition** | Workforce exits and attrition patterns across organizational groups |

The dashboard is intended to support exploration and follow-up questions, not to replace HR investigation or manager conversations.

## Suggested business actions

1. Conduct a focused retention review in Sales, particularly among Sales Representatives.
2. Break down overtime by department, role, and manager; validate whether sustained workload pressure is present.
3. Review onboarding, manager check-ins, and career pathways for employees in their first two years.
4. Explore work-life balance feedback and investigate differences between self and manager ratings.
5. Review training access and participation barriers, then monitor participation and outcomes over time.
6. Track attrition with a consistent reporting period, termination dates, and an appropriate average-headcount denominator in future reporting.

## Conclusion

This HR analytics project highlights two particularly actionable patterns: attrition is comparatively high in Sales and in selected customer-facing roles, and employees recorded as working overtime have a substantially higher attrition share. It also surfaces opportunities to improve work-life balance, training participation, and the early employee experience.

Together, these findings give HR teams a practical starting point for targeted investigation and evidence-informed workforce planning.

## 👨‍💻 Author

**Ved Patil** | [LinkedIn](https://linkedin.com/in/vedpatil3076/)

Aspiring Data Analyst | Business Intelligence Enthusiast  
**Project:** Human Resource Analytics Dashboard  
**Tools:** Excel | PostgreSQL | SQL | Power BI
