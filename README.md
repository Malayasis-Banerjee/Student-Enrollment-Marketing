
# 🎯 Student Enrollment & Marketing Dashboard

## 📝 Short Description / Purpose
A comprehensive Power BI dashboard designed to analyze studentenrollment, payment performance, academic/completion status, marketingcampaigns, lead generation, and student-level details.
This project demonstrates practical skills in Power BI, DAX, datacleaning, data modeling, KPI development, interactive filtering, andbusiness intelligence reporting.

## 📌 Project Objective
The goal of this project is to transform **student enrollment** and **marketing data** into an interactive dashboard that enables management to answer key business questions.

## 🔍 Key Insights & Questions
- 📊 **Enrollment**
  - How many students are enrolled?
  - Which cities and courses have the highest enrollment?
  - How does enrollment change over time?

- ✅ **Completion**
  - What is the overall completion rate?
  - What is the relationship between feedback and completion?

- 💰 **Payments & Revenue**
  - How many students have paid, pending, or failed payments?
  - Which courses generate the highest revenue?

- 📈 **Marketing**
  - How much is being spent on marketing?
  - Which lead sources generate the most leads?
  - What is the cost per lead?

- 👥 **Follow-up**
  - Which individual students require follow-up?


## 🛠️ Features
- Interactive **Power BI dashboard**
- Visualizations for **student performance, payments, and marketing ROI**
- Drill-through for **individual student profiles**
- KPI cards for **quick insights**
- Trend analysis for **enrollment and marketing spend**


## 🚀 Outcome
A professional dashboard that helps management:
- Monitor student enrollment trends
- Track financial performance
- Evaluate marketing effectiveness
- Identify students requiring follow-up


## 📌 Dashboard Pages

### 1. Executive Overview
Provides a high-level summary of the complete student and marketing operation.

#### 🔑 Key KPIs
- Total Students  
- Total Revenue  
- Average Fees  
- Completed Students  
- Total Marketing Spend  
- Completion Rate  

#### 📊 Main Visuals
- Students by City  
- Completion Status  
- Payment Status  
- Student Enrollment Trend  
- Students by Course
### Dashboard 
![Executive Overview](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Executive%20Overview.png
)

### 2. Student Enrollment Analysis
Focuses on enrollment patterns and student participation.

#### 🔍 Analysis Includes
- Student Enrollment Trend  
- Total Students by City  
- Total Students by Enrollment Mode  
- Course × Enrollment Mode  
- Course × Completion Status  
- Total Students by Class Mode  

#### 🎛️ Interactive Filters
- City  
- Completion Status  
- Enrollment Mode  
- Class Mode  
- Date  
### Dashboard
![Student Enrollment Analysis](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Student%20Enrollment%20Analysis.png
)

### 3. Payment & Student Performance
Analyzes payment behavior, revenue, and student feedback.

#### 🔑 Key KPIs
- Total Revenue  
- Paid Students  
- Pending Students  
- Paid Rate  
- Average Fees  
- Failed Payments  

#### 📊 Main Visuals
- Payment Status by Course  
- Revenue by Course  
- Feedback Distribution  
- Student Feedback by Course  

📌 This page helps identify **payment trends** and highlights courses with stronger or weaker financial performance.
### Dashboard
![Payment & Student Performance](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Payment%20%26%20Student%20Performance.png
)

### 4. Marketing & Lead Analysis
Analyzes marketing expenditure and lead-generation performance.

#### 🔑 Key KPIs
- Total Marketing Spend  
- Total Leads  
- Cost Per Lead  

#### 📊 Main Visuals
- Marketing Spend by Location  
- Marketing Spend Trend  
- Leads by Source  
- Marketing Spend by Lead Source  
- Location vs Marketing Spend Map  

#### 🎛️ Filters
- Lead Source  
- Location  
### Dashboard
![Marketing & Lead Analysis](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Marketing%20%26%20Lead%20Analysis.png
)

### 5. Student Details
Provides a detailed student-level view.

#### 🧾 Student Information Includes
- Student ID  
- Student Name  
- Course  
- City  
- Email  
- Payment Status  
- Enrollment Mode  
- Remarks  

#### 🎛️ Interactive Filters
- Student ID search  
- Class Mode  
- Course  
- Completion Status  
- Payment Status  
- City  

📌 This page can be used to quickly locate **individual students** and identify those requiring **follow-up**.
### Dashboard
![Student Details](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Student%20Details.png
)

### 6. Extra Info
Provides additional analytical insights for deeper investigation.

#### 🔍 Analysis Includes
- Representative Performance  
- Paid Rate by Course  
- Completion Rate by Course  
- City-wise Revenue  
- Enrollment Mode by Completion Status  
- Class Mode by Feedback  
- Feedback vs Completion  
- Students by Source  
- Average Fees by Course  
- Revenue by Course  

📌 This page is designed to support **more detailed business decisions** beyond the main dashboard pages.
### Dashboard
![Extra Info](https://github.com/Malayasis-Banerjee/Student-Enrollment-Marketing/blob/main/Extra%20info.png
)

## 🧹 Data Cleaning & Transformation

The data preparation process included the following steps:

- Removing duplicate records  
- Handling missing/null values  
- Standardizing categorical values  
- Cleaning student names  
- Cleaning phone numbers  
- Standardizing addresses  
- Extracting city information  
- Validating PIN/postal-code values  
- Checking Student ID consistency  
- Resolving mismatched records during data merging  
- Combining multiple source tables  
- Validating payment and enrollment fields  
- Creating analysis-ready columns  
- Creating relationships between tables  
- Creating calculated measures using DAX  

⚠️ **Note:**  
- Missing values should be handled according to the **business meaning** of each column.  
- Categorical fields should **not automatically be filled with the mode**, as this could introduce misleading information.
  
## 📐 Important KPIs

Examples of the analytical measures used in the dashboard include:

### 🎯 Total Student

Total Students =
DISTINCTCOUNT(Main_Data[Student_ID])

### 🎯 Paid Students

Paid Students =
CALCULATE(
    [Total Students],
    Main_Data[Payment_Status] = "Paid"
)

### 🎯 Paid Rate
Paid Rate =
DIVIDE(
    [Paid Students],
    [Total Students],
    0
)

### 🎯 Completion Rate
Completion Rate =
DIVIDE(
    [Completed Students],
    [Total Students],
    0
)

### 🎯 Cost per Lead
Cost Per Lead =
DIVIDE(
    [Total Marketing Spend],
    [Total Leads],
    0
)

## 🛠️ Tools & Technologies

- **Power BI Desktop** – Core platform for building interactive dashboards  
- **Power Query** – Data cleaning and transformation  
- **DAX (Data Analysis Expressions)** – Measures, KPIs, calculations, and analytical logic  
- **Microsoft Excel** – Source data preparation  
- **Data Visualization** – Charts, graphs, and interactive visuals  
- **Data Modeling** – Star schema, relationships, and optimized structures  
- **Interactive Slicers & Filters** – Dynamic exploration of data  

### 🔧 Additional Tools & Technologies
- **SQL** – Querying and managing structured data from databases  
- **Python (Pandas, NumPy, Matplotlib, Seaborn)** – Advanced data analysis and visualization   
- **Jupyter Notebook** – Interactive environment for data exploration and reporting  
- **GitHub** – Version control and collaboration  
- **ETL Pipelines** – Extract, Transform, Load processes for handling large 


## 📊 Business Insights

The dashboard can help management:

- Identify cities with high student enrollment  
- Compare course popularity  
- Monitor student completion  
- Track paid, pending, and failed payments  
- Identify courses with higher revenue  
- Compare online vs offline enrollment  
- Compare live vs recorded classes  
- Evaluate marketing spending by location  
- Compare lead-generation sources  
- Monitor cost per lead  
- Identify students requiring follow-up  
- Understand the relationship between feedback and completion


## 🚀 Outcome

The interactive dashboard delivers actionable insights that empower management to:

- 📊 **Monitor Enrollment Trends**  
  Track how student enrollment changes over time across cities, courses, and modes.  
- 💰 **Track Financial Performance**  
  Identify paid, pending, and failed payments, measure revenue by course, and monitor average fees.  
- ✅ **Evaluate Student Success**  
  Assess completion rates, compare feedback vs completion, and highlight students requiring follow-up.  
- 📈 **Measure Marketing Effectiveness**  
  Analyze marketing spend by location, evaluate lead sources, and calculate cost per lead.  
- 🎯 **Support Strategic Decisions**  
  Provide advanced analysis (city-wise revenue, course performance, representative performance) to guide resource allocation and growth strategies.  

📌 Overall, the dashboard transforms raw enrollment and marketing data into **clear, interactive insights** that support better decision-making and improve both academic and business outcomes.



