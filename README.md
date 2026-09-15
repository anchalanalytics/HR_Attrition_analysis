# HR Employee Attrition — SQL Analysis

A SQL-based analysis of IBM's HR Employee Attrition dataset, uncovering the strongest drivers behind why employees quit — overtime, salary, promotion gaps, and job satisfaction — using aggregations, CASE-based bucketing, and grouped comparisons.

## 📊 Dataset

- **Source:** IBM HR Analytics Employee Attrition Dataset (`WA_Fn-UseC_-HR-Employee-Attrition.csv`)
- **Size:** 1,470 employee records, 35 attributes (department, role, income, satisfaction scores, tenure, overtime, etc.)
- **Tool:** MySQL

## 🔍 Key Findings

- **Overall attrition rate:** 16.1% of employees have left the company (237 out of 1,470).
- **Overtime is the single biggest attrition driver:** employees who work overtime leave at **30.5%**, nearly **3x** the rate of those who don't (10.4%).
- **Sales loses the most employees:** Sales has the highest departmental attrition (20.6%), followed by HR (19.1%) and R&D (13.8%).
- **Salary matters more than work-life balance:** low earners (under $3k/month) leave at **28.6%**, over 5x the rate of top earners (5.6%) — a sharper split than work-life balance alone produces (31.3% for "Bad" vs. 14.2% for "Better").
- **Highest-risk profile:** Sales Representatives working overtime leave at **67%** — by far the most at-risk group in the company, followed by overtime Lab Technicians in R&D (50%).

## 🛠️ SQL Techniques Used

- Conditional aggregation with `CASE WHEN` for rate calculations
- Bucketing continuous variables (salary, age, promotion gap) into readable bands
- Multi-column `GROUP BY` with `HAVING` to filter out small, unreliable segments
- Ordered comparisons (`ORDER BY ... DESC`) to surface the highest-risk groups

## 📁 Files

| File | Description |
|------|-------------|
| `hr_attrition03_sql.sql` | Full SQL script — overall rate, department/salary/overtime/satisfaction/work-life-balance breakdowns, age & promotion-gap analysis, and a combined "who's most likely to quit" profile query |
| `WA_Fn-UseC_-HR-Employee-Attrition (1).csv` | Raw dataset used for the analysis |

## 💡 Business Takeaway

Overtime and low pay are the two clearest, most actionable attrition levers — far stronger signals than tenure or work-life balance scores alone. Targeting overtime reduction and pay review in Sales and R&D's most overworked roles would likely yield the biggest retention gains.

---
*Conducted SQL-based HR attrition analysis on IBM dataset — identified top attrition drivers across salary, overtime, job satisfaction, and promotion gaps using advanced SQL aggregations and CASE logic.*
