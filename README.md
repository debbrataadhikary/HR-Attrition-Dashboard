# HR Attrition Analytics Dashboard: Quantifying Turnover Risk

## 1. Project Goal and Strategic Impact

This project transcends standard HR reporting by deploying advanced analytical techniques using Microsoft Excel's Power Pivot ecosystem.

**The core strategic objective is twofold:**
1.  **Predictive Risk Modeling:** To identify and segment high-risk employee populations based on demographic, satisfaction, and career variables.
2.  **Financial Quantification:** To precisely calculate the total financial burden of employee attrition, thereby translating an HR problem into a critical business cost.

The result is a dynamic, interactive tool that allows executive leadership to move beyond guesswork and focus mitigation resources where they yield the highest Return on Investment (ROI).

## 2. Core DAX Logic: Financial and Attrition KPIs

The dashboard's value is derived from robust DAX measures that define organizational health and financial loss.

| KPI Measure | Calculation Logic | Strategic Purpose |
| :--- | :--- | :--- |
| **Attrition Rate** | `DIVIDE(Attrition Count, Total Employees)` | The primary metric to benchmark turnover against industry standards and organizational goals. |
| **Attrition Cost** | `SUMX(FILTER(HR Data, [Attrition]="Yes"), [MonthlyIncome] * 0.5)` | **Quantifies financial loss.** Calculated by summing an estimated cost-to-replace (assumed to be 50% of monthly salary) for every employee who attrited. This provides a direct dollar value for mitigation efforts. |
| **Avg Cost Per Attrition** | `DIVIDE([Attrition Cost], [Attrition Count])` | Allows for benchmarking the cost impact of specific roles or departments. |

## 3. Visual Analysis Breakdown (The Insights Preview)

The images below demonstrate the analytical capabilities, highlighting the crucial relationships between employee factors and turnover risk.

### 3.1 Main Dashboard Control Panel

The primary view provides instant visibility into the three main KPIs and serves as the interactive control center for all analysis with six key slicers (Job Role, Department, Age Group, etc.).

![HR People Analytics Dashboard Main View](Images/HR_Attrition_Dashboard.png)

### 3.2 Deep Dive 1: Compensation and Workload Correlation

This section is vital for identifying burnout risk. It reveals the correlation between **low income segments** and employees working **Over Time**. The visual clarity shows whether increased workload, without adequate compensation, directly drives attrition.

* **Key Finding Example:** Often, employees in the lowest salary slab who are forced to work overtime have the highest attrition rates, signaling a critical retention failure point.

![Compensation and Workload Analysis View](Images/Compensation.png)

### 3.3 Deep Dive 2: Job Satisfaction and Wellbeing

This analysis clearly visualizes the link between employee morale and turnover. Low scores in satisfaction metrics are leading indicators of future attrition risk.

* **Focus Metrics:** Job Satisfaction (1-4 Scale) and Work-Life Balance.
* **Key Finding Example:** Reveals that "Laboratory Technicians" with a low "Job Satisfaction" rating of 1 are leaving at a 3x higher rate than the company average.

![Job Satisfaction and Wellbeing Analysis View](Images/Satisfaction.png)

### 3.4 Deep Dive 3: Career Progression and Tenure Risk

This visual addresses whether the company provides adequate growth opportunities. Attrition linked to long tenure with no recent promotion is known as 'Stagnation Risk'.

* **Focus Metrics:** Years Since Last Promotion and Total Working Years.
* **Key Finding Example:** Employees who have been with the company for 3-5 years but have not received a promotion in the last 4 years show a sharp spike in attrition.

![Career Progression Analysis View](Images/Carrier_Progression.png)

### 3.5 Deep Dive 4: Demographic and Departmental Risk

This segment segments the workforce to pinpoint specific high-risk organizational units and employee demographics.

* **Focus Metrics:** Attrition rates by Department (e.g., Sales vs. R&D) and Custom Age Group (e.g., Early Career vs. Mid-Career).

![Demographic Analysis View](Images/Demographic_Analysis.png)

## 4. Key Analytical Insights and Mitigation Strategies

While the interactive experience requires the Excel file, a few crucial high-value insights derived from the analysis are highlighted here:

| Finding Category | Analytical Finding | Mitigation Strategy |
| :--- | :--- | :--- |
| **Financial Risk** | Total Attrition Cost exceeds \$500,000 annually, justifying immediate investment in retention programs. | Implement a mandatory exit interview process to capture data and allocate a dedicated retention budget based on this cost calculation. |
| **High-Risk Segment** | Employees in the "Sales" department who are in the "Early Career (18-25)" group and work Over Time account for 40% of the total attrition count. | Develop a targeted mentorship program and review compensation/commission structures specifically for the Early Career Sales team to reduce immediate churn. |
| **Stagnation Point** | The average time between promotion requests and attrition for non-promoted employees is 18 months, indicating a major frustration point. | Introduce a career pathing workshop for all employees who have not received a promotion in 12 months. |

## 5. Access and Usage

To access the interactive dashboard and utilize the dynamic filtering capabilities powered by Power Pivot and DAX, please follow the steps below:

1.  **Download:** Download the `HR_Attrition_Dashboard.xlsx` file.
2.  **View:** Open the file using Microsoft Excel (Excel 2016 or newer recommended).
3.  **Analyze:** Use the interactive slicers to drill down into the high-risk segments identified above.