# Call Center Performance Analytics — Project Work

## 1. Project Overview

This project is a **Call Center Performance Analysis dashboard developed in Microsoft Power BI**.

The project focuses on:

- Overall call volume
- Answered vs. unanswered calls
- Answer rate
- Resolved calls
- Resolution rate
- Average speed of answer
- Customer satisfaction
- Agent-level performance
- Call topics
- Monthly call trends
- Call resolution status
- Performance classification
- Detailed call-level records

The report contains three main report sections:

1. **Agent Report**
2. **Performance Analysis**
3. **Insights**

---

## 2. Data Used

The main data table used in the Power BI model is:

**data**

The report uses fields including:

- Call Id
- Agent
- Answered (Y/N)
- Resolved_
- Speed of answer (sec)
- Satisfaction rating
- Performance
- Topic
- Date

The report also uses Power BI's automatic **Date Hierarchy**, particularly the **Month** level, for time-based analysis.

---

## 3. Data Analysis / Data Fields Used

The project analyzes the following major dimensions and metrics.

### Call-related fields

- Call Id
- Date
- Topic
- Agent

### Call status fields

- Answered (Y/N)
- Resolved_

### Performance fields

- Performance
- Speed of answer (sec)
- Satisfaction rating

The *Performance* field is used to classify performance into:

- **Poor**
- **Good**
- **Excellent**

---

## 4. Measures Created / Used

A dedicated *_Measures* table is used in the report.

The following measures are confirmed from the PBIX report metadata.

### 4.1 Total Calls

**Measure:** *Total_Calls*

Used to display the total number of calls.

Used in:

- KPI card
- Agent-level analysis
- Dashboard

### 4.2 Answered Calls

**Measure:** *Answered_Call*

Used to calculate/display the number of calls that were answered.

Used in:

- KPI card
- Answered vs Unanswered analysis
- Agent performance analysis

### 4.3 Resolved Calls

**Measure:** *Resolved_Call*

Used to calculate/display the number of resolved calls.

Used in:

- KPI card
- Resolution analysis

### 4.4 Answer Rate

**Measure:** *Answer_Rate %*

Used to calculate the percentage of total calls that were answered.

Conceptually:

**Answer Rate = Answered Calls / Total Calls**


### 4.5 Resolved Rate

**Measure:** *Resolved_Rate %*

Used to calculate the percentage of calls that were resolved.

Conceptually:

**Resolved Rate = Resolved Calls / Total Calls**

### 4.6 Average Speed of Answer

**Measure:** *Avg_Speed_of_Answer (in sec)*

Used to calculate the average speed of answer in seconds.

This KPI represents how quickly calls are being answered.

### 4.7 Average Satisfaction Rating

**Measure:** *Avg_Satisfaction_Rating*

Used to calculate the average customer satisfaction rating.

### 4.8 Unanswered Calls

**Measure:** *UnAnswered_Call*

Used specifically for the **Answered vs Unanswered** visual.

---

## 5. Calculations / Aggregations Used

The report uses multiple Power BI aggregation techniques.

These include:

- Count of Call Id
- Count of non-null Call Id
- Count of Agent
- Sum of Speed of Answer
- Sum of Satisfaction Rating
- Measure-based calculations
- Average-based KPI calculations

The report also uses **month-level aggregation** for time-series analysis.

---

## 6. Date / Time Analysis

The report uses the Date field with Power BI's automatic:

**Date Hierarchy**

The hierarchy is used at the:

**Month level**

This is used to analyze call volume over time.

The dashboard contains a **monthly call trend line chart**.

There is also a model field/measure named:

**Count of Call Id MoM%**

which indicates that a **Month-over-Month percentage analysis** has been incorporated into the model/report.

---

## 7. Dashboard KPIs

The main Dashboard contains six KPI cards.

### KPI 1 — Total Call

Shows overall call volume.

### KPI 2 — Answered Call

Shows the number of answered calls.

### KPI 3 — Answer Rate %

Shows the percentage of calls answered.

### KPI 4 — Resolved Rate %

Shows the percentage of calls resolved.

### KPI 5 — Average Speed of Answer

Shows average answer speed in seconds.

### KPI 6 — Average Satisfaction

Shows the average customer satisfaction rating.

These KPIs provide the high-level view of the call center's operational health.

---

## 8. Dashboard Visualizations

The main Dashboard contains the following visual analysis.

### 8.1 KPI Cards

Six cards are used for the main performance indicators:

- Total Calls
- Answered Calls
- Answer Rate
- Resolved Rate
- Average Speed of Answer
- Average Satisfaction

### 8.2 Monthly Call Trend

A **Line Chart** is used.

**X-axis:**
- Month

**Metric:**
- Count of Call Id

Purpose:

To understand how call volume changes over time.

### 8.3 Answered vs Unanswered

A **Pie Chart** is used.

Measures:

- Answered_Call
- UnAnswered_Call

Purpose:

To show the proportion of answered and unanswered calls.

### 8.4 Agent Performance Table / Matrix

A **Pivot Table / Matrix** is used to compare agents.

The analysis includes:

- Agent
- Total Calls
- Answer Rate %
- Other performance measures

This allows performance to be examined at the individual-agent level.

### 8.5 Calls by Topic

A **Donut Chart** is used to analyze calls by topic.

The *Topic* field is used as the category and call count is used as the metric.

### 8.6 Call Volume by Topic

Another topic-level visual is present in the report.

It uses:

- Topic
- Count of Call Id

This provides a ranking/distribution of call topics based on call volume.

---

## 9. Slicers / Interactive Filters

The Dashboard contains multiple slicers for interactive analysis.

### Date

Allows the user to filter the report by date.

### Agent

Allows analysis for a particular agent.

### Topic

Allows filtering based on call topic.

### Satisfaction Rating

Allows filtering based on customer satisfaction rating.

The Agent Report also contains an **Agent slicer**.

These slicers make the dashboard interactive and allow the same KPIs and visuals to be analyzed for different subsets of the data.

---

## 10. Agent Report

A separate **Agent Report** page has been created.

This page is more detailed than the high-level dashboard.

It contains:

- Detailed call table
- Agent slicer
- KPI cards
- Topic analysis
- Date-based analysis
- Additional filtering

The KPI cards on this page include:

- Total Call
- Answered Call
- Resolved Call
- Resolved %

---

## 11. Detailed Call-Level Table

The Agent Report contains a detailed table with fields including:

- Call Id
- Agent
- Answered (Y/N)
- Resolved_
- Speed of answer (sec)
- Satisfaction rating
- Performance

This provides a **row-level operational view** of individual calls.

---

## 12. Conditional Formatting

Conditional formatting has been implemented in the detailed call table.

There are two confirmed conditional-formatting mechanisms.

### 12.1 Resolution Status Icons

The *Resolved_* field has conditional icons.

The logic distinguishes between:

- Blank
- No
- Yes

Different icons are displayed based on the resolution status.

This makes resolved/unresolved status visually easier to identify.

## 13. Visual Formatting

The report also uses Power BI visual-formatting features such as:

- Custom visual titles
- Font sizing
- Text alignment
- Font colors
- Background formatting
- Borders
- Bold column headers
- Center alignment
- Theme-based colors
- KPI card formatting
- Customized visual layouts

The report also contains a Power BI theme/resource package.

---

## 14. Report Design / Layout

The PBIX contains three report pages:

### Page 1 — Agent Report

Detailed agent and call-level analysis.

### Page 2 — Dashboard

High-level business performance overview.

### Page 3 — Insights

Dedicated page for insights / interpretation.

The Dashboard also contains visual design elements including:

- Header/text elements
- KPI cards
- Charts
- Tables
- Slicers
- Background/theme formatting
- Supporting visual elements

---

## 15. Interactivity

The report uses Power BI's interactive capabilities.

These include:

- Slicers
- Cross-filtering
- Visual interactions
- Drill/filter behavior
- Date filtering
- Agent filtering
- Topic filtering
- Satisfaction filtering

The detailed table is also configured so that visual interactions can filter other visuals.

---

## 16. Business Health

The business health is evaluated through five major operational dimensions:

### 16.1 Call Demand

**Total Calls**

Shows the overall workload handled by the call center.

### 16.2 Accessibility / Responsiveness

**Answered Calls + Answer Rate**

These indicate how effectively the call center is responding to incoming demand.

A higher answer rate indicates that a greater proportion of incoming calls are being attended.

### 16.3 Resolution Effectiveness

**Resolved Calls + Resolved Rate**

These measure the ability of the call center to successfully resolve customer issues.

### 16.4 Operational Efficiency

**Average Speed of Answer**

This indicates how quickly customers are being connected to an agent.

### 16.5 Customer Experience

**Average Satisfaction Rating**

This represents the customer's reported experience with the service.

### Overall Business Health Framework

The dashboard therefore evaluates the call center across:

**Demand → Responsiveness → Resolution → Efficiency → Customer Satisfaction**

This gives a complete operational view rather than relying on only one KPI.

---

## 17. Agent-Level Business Health

Agent performance is analyzed through:

- Total calls handled
- Answer rate
- Resolution performance
- Performance classification
- Satisfaction
- Call-level status
- Individual call records

This makes it possible to identify differences in performance between agents.

---

## 18. Topic-Level Analysis

The project also analyzes the distribution of calls across different topics.

This allows the report to show:

- Which topics generate more calls
- Relative volume of different topics
- Topic-level workload distribution

Topic analysis is displayed through donut/chart-based visualizations.

---

## 19. Time-Based Analysis

The project uses monthly analysis to understand call volume over time.

The report therefore supports:

- Monthly call volume
- Month-level trend analysis
- MoM percentage analysis

This adds a time dimension to the operational analysis.

---

## 20. Insights Page

A separate **Insights** page has been created.

The Insights section summarizes the important patterns identified from:

- KPI performance
- Agent performance
- Call volume
- Resolution
- Answer rate
- Satisfaction
- Speed of answer
- Topic distribution
- Time trends

---

## 21. Overall Power BI Techniques Used

### Data / Model

- Data table
- Dedicated `_Measures` table
- Date field
- Date hierarchy
- Measures
- Aggregations

### DAX / Calculations

- KPI measures
- Count calculations
- Answer-rate calculation
- Resolution-rate calculation
- Average calculations
- MoM percentage analysis
- Measure-based visual calculations

### Visualizations

- Card visuals
- Line chart
- Pie chart
- Donut chart
- Table
- Matrix / Pivot Table
- Text boxes
- Image elements

### Filtering

- Slicers
- Agent filtering
- Date filtering
- Topic filtering
- Satisfaction filtering
- Cross-filtering between visuals

### Formatting

- Conditional formatting
- Conditional icons
- Conditional background colors
- Theme colors
- Font formatting
- Borders
- Alignment
- KPI card formatting
- Header formatting

### Report Design

- Multiple report pages
- Dashboard layout
- Dedicated Agent Report
- Dedicated Insights page
- Interactive dashboard
- KPI-focused design

---

## 22. Project Workflow

The overall project workflow can be represented as:

**Raw Call Center Data**

↓

**Data Fields / Model**

↓

**Measures & Calculations**

↓

**KPI Creation**

↓

**Agent Analysis**

↓

**Topic Analysis**

↓

**Time-Series Analysis**

↓

**Conditional Formatting**

↓

**Interactive Slicers**

↓

**Dashboard**

↓

**Agent Report**

↓

**Insights**

↓

**Business Health Assessment**

---

## 23. Project Summary

This Power BI project converts call-center-level data into an interactive performance-monitoring solution.

The project covers:

- Call volume analysis
- Answered/unanswered analysis
- Answer rate
- Resolution analysis
- Resolution rate
- Average speed of answer
- Customer satisfaction
- Agent-level performance
- Topic-level analysis
- Monthly trend analysis
- MoM analysis
- KPI cards
- Interactive slicers
- Detailed call-level reporting
- Conditional icons
- Conditional background formatting
- Dedicated measures
- Dashboard design
- Agent reporting
- Insights presentation
- Business health assessment

### Overall Dashboard Structure

**Operational KPIs + Agent Performance + Customer Experience + Call Trends + Topic Analysis + Detailed Call Data + Insights**