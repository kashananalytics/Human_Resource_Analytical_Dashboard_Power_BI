# Human_Resource_Analytical_Dashboard_Power_BI
An interactive Power BI Dashboard Project focused on Employee Attrition, Workforce demographics, Job Satisfaction and HR performance analysis. The dashboard provides meaningful insights using KPIs, Charts, Slicers, and DAX measures to support data-driven HR decisions.
<br>
# 👥 Human Resource Analytics Dashboard — Power BI

> Built to answer the question every HR team needs to face: who is leaving, why are they leaving, and what does the data actually say about it?

---

## 📸 Dashboard Preview

![Dashboard Preview](dashboard.png)


---

## 📌 Project Summary

This is a real-world HR analytics project built in Power BI. The dataset covers **1,470 employees** with detailed information on their age, gender, education, department, job role, marital status, travel frequency, monthly pay, and job satisfaction ratings.

The goal was to build a dashboard that helps HR teams and managers understand attrition patterns clearly — not just see numbers but actually understand what those numbers mean.

---

## 🔢 KPI Cards

| KPI | Value |
|---|---|
| 👥 Total Employees | 1,470 |
| ✅ Active Employees | 1,233 |
| 🔴 Total Attrition | 237 |
| 📉 Attrition Rate | 16.11% |
| 💰 Avg Monthly Pay | 6,503 |
| 🎂 Average Age | 37 |

---

## 🎛️ Filters & Slicers

Every filter on this dashboard cross-filters all visuals instantly.

| Filter | Options |
|---|---|
| Education | Associates · Bachelor's · Doctoral · High School · Master's Degree |
| Gender | Female · Male |
| Marital Status | Divorced · Married · Single |
| Travel Frequency | Non-Travel · Travel Frequently · Travel Rarely |

---

## 📊 Visuals Built

**1. Clustered Bar Chart — Employees by Age Group & Gender**
Compares male vs female headcount across five age groups.

| Age Group | Female | Male |
|---|---|---|
| Under 25 | 37 | 60 |
| 25 – 34 | 217 | 337 |
| 35 – 44 | 196 | 309 |
| 45 – 54 | 113 | 132 |
| Over 55 | 25 | 44 |

The 25–34 age group has the highest headcount for both genders — and also the highest attrition risk.

---

**2. Area Line Chart — Attrition by Age**
Plots attrition count against employee age from 18 to 60. The chart peaks sharply between ages **28 and 32** — the career-switching window where employees are most likely to leave.

---

**3. Donut Chart — Department Wise Attrition**

| Department | Attrition Count | Share |
|---|---|---|
| Sales | 133 | 56.12% |
| R&D | 92 | 38.82% |
| HR | 12 | 5.06% |

Sales is losing more than half of all employees who leave the company.

---

**4. Horizontal Bar Chart — Attrition by Job Role**

| Job Role | Attrition Count |
|---|---|
| Sales Executive | 326 |
| Research Scientist | 292 |
| Laboratory Technician | 259 |
| Manufacturing Director | 145 |
| Healthcare Representative | 131 |
| Manager | 102 |
| Sales Representative | 83 |

Sales Executives top the list by a significant margin.

---

**5. Matrix Table — Job Satisfaction Rating**
Shows how each job role rated their satisfaction from 1 (lowest) to 4 (highest).

| Job Role | 1 | 2 | 3 | 4 | Total |
|---|---|---|---|---|---|
| Healthcare Representative | 26 | 19 | 43 | 43 | 131 |
| Human Resources | 10 | 16 | 13 | 13 | 52 |
| Laboratory Technician | 56 | 48 | 75 | 80 | 259 |
| Manager | 21 | 21 | 27 | 33 | 102 |
| Manufacturing Director | 26 | 32 | 49 | 38 | 145 |
| Research Director | 15 | 16 | 27 | 22 | 80 |
| Research Scientist | 54 | 53 | 90 | 95 | 292 |
| Sales Executive | 69 | 54 | 91 | — | 326 |
| **Total** | **289** | **280** | **442** | **459** | **1,470** |

Research Scientists lean toward rating 4. Sales Executives have the highest count at rating 1. That pattern matters.

---

**6. Funnel Chart — Attrition by Education Field**
Shows which education backgrounds have the most attrition.

- Life Sciences — highest
- Medical
- Marketing
- Technical Degree
- Other
- Human Resources — 7.9% (lowest)

---

## 🧮 DAX Measures

```dax
-- Total Employees
Total Employees = COUNTROWS('HR Data')

-- Total Attrition
Total Attrition = CALCULATE(COUNTROWS('HR Data'), 'HR Data'[Attrition] = "Yes")

-- Attrition Rate
Attrition Rate = DIVIDE([Total Attrition], [Total Employees])

-- Active Employees
Active Employees = [Total Employees] - [Total Attrition]

-- Average Monthly Pay
Avg Monthly Pay = AVERAGE('HR Data'[MonthlyIncome])

-- Average Age
Average Age = AVERAGE('HR Data'[Age])
```

---

## 💡 Key Insights

- 🔴 **16.11% attrition rate** — roughly 1 in 6 employees is leaving
- 📉 **Ages 28–32 are the danger zone** — this is where attrition spikes the hardest
- 🏢 **Sales department** is responsible for over half of all attrition (56.12%)
- 😟 **Sales Executives** have the highest attrition (326) AND the most rating 1 satisfaction scores — the two are connected
- 🎓 **Life Sciences graduates** leave more than any other education field
- 💍 Filtering by **Single + Travel Frequently** shows the highest attrition combination
- 📊 Rating 3 and 4 dominate overall satisfaction — but the roles with the most attrition still lean toward rating 1

---

## 🛠️ Tools Used

- **Microsoft Excel** — raw data source
- **Power Query** — data cleaning and transformation
- **Power BI Desktop** — dashboard design and layout
- **DAX** — all KPI measures and calculations

---

## 🚀 How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Use the **education tabs** at the top to filter by degree type
4. Use the **gender, marital status and travel slicers** on the right
5. Click any bar, donut slice or funnel segment to cross-filter all visuals
6. Hover over the satisfaction matrix to see exact counts per role

---

*Feel free to fork this or adapt the DAX measures for your own HR or people analytics projects.*

## Author
Kashan Ahmed  
BS Statistics Graduate | Power BI & Data Analytics.
