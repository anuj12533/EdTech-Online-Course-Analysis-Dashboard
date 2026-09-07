
# 🎓 EdTech Online Course Analysis Dashboard
## 📖 Project Overview

The **EdTech Online Course Analysis Dashboard** is a Business Intelligence project developed using **Power BI** to analyze online course data collected from multiple EdTech platforms.

The objective of this project is to help an EdTech startup understand learner behavior, course performance, instructor effectiveness, language preferences, and engagement trends in recorded lecture-based courses. The analysis focuses primarily on **category-wise insights** to support strategic decision-making and future course development.
---

## 🎯 Business Objective

The startup aims to:
- Expand its recorded lecture offerings.
- Identify the most popular course categories.
- Understand viewer engagement patterns.
- Discover preferred languages across categories.
- Analyze the impact of subtitles on course performance.
- Identify top-performing instructors for collaboration.
- Optimize course duration based on learner preferences.

## 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX (Data Analysis Expressions)**
- **Microsoft Excel / CSV**
- **Data Modeling**

---

## 📂 Dataset Features

The dataset contains information related to online courses, including:

| Column Name | Description |
|------------|-------------|
| Course ID | Unique Course Identifier |
| Title | Course Name |
| Category | Main Course Category |
| Sub-Category | Detailed Classification |
| Course Type | Course / Specialization |
| Instructor | Course Creator |
| Language | Course Language |
| Rating | Course Rating |
| Number of Viewers | Viewer Count |
| Registrations | Enrollment Count |
| Duration | Course Length |
| Subtitle Language | Available Subtitle Languages |

---

## 🧹 Data Cleaning & Transformation

The following preprocessing steps were performed:

### Data Cleaning
- Removed duplicate records.
- Handled missing values.
- Standardized category names.
- Standardized language names.
- Corrected inconsistent text formats.

### Duration Standardization

As specified in the project requirements:

| Original Duration | Converted Duration |
|------------------|-------------------|
| 1 Month | 60 Hours |
| Flexible Schedule | 200 Hours |

### Data Modeling
- Established relationships between tables.
- Created calculated columns and measures using DAX.
- Optimized data model for dashboard performance.

---

# 📊 Dashboard KPIs

### Total Courses

```DAX
Total Courses =
COUNT(Online_Courses[Course_ID])
```

### Average Rating

```DAX
Average Rating =
AVERAGE(Online_Courses[Rating])
```

### Total Viewers

```DAX
Total Viewers =
SUM(Online_Courses[Number of Viewers])
```

### Average Viewers

```DAX
Average Viewers =
AVERAGE(Online_Courses[Number of Viewers])
```

### Average Registrations Per Course

```DAX
Average Registrations =
AVERAGE(Online_Courses[Overall Registrations])
```

---

# 📈 Analysis & Insights

## 1️⃣ Total Number of Courses

### Objective
Determine the total number of courses available in the dataset.

### Insight
- The dataset contains approximately **1,000 courses**.
- Provides an overview of the catalog size.

---

## 2️⃣ Average Course Rating

### Objective
Calculate the average rating across all courses.

### Insight
- Average rating: **4.70 / 5**
- Indicates strong learner satisfaction.

---

## 3️⃣ Total & Average Number of Views

### Objective
Measure overall viewer engagement.

### Metrics
- Total Viewers
- Average Viewers per Course

### Insight
- High engagement levels indicate strong demand for recorded lectures.

---

## 4️⃣ Course Type Distribution Across Categories

### Objective
Analyze course types available across categories and subcategories.

### Visuals Used
- Bar Charts
- Category-wise Distribution Charts

### Insights
- Certain categories are dominated by specialization programs.
- Others have a higher proportion of standalone courses.

### Business Value
Helps determine which course format should be launched in each category.

---

## 5️⃣ Average Views by Category, Subcategory & Language

### Objective
Understand viewer engagement patterns.

### Insights
- Information Technology and Computer Science categories receive higher average views.
- Viewer engagement differs significantly across languages.

### Business Value
Supports data-driven content planning.

---

## 6️⃣ Language Distribution Analysis

### Objective
Analyze the distribution of course languages.

### Visual Used
- Donut Chart

### Insights
- English dominates the course catalog.
- Other languages present growth opportunities.

---

## 7️⃣ Top 5 Categories – Language Preference Analysis

### Objective
Determine language preferences within the most popular categories.

### Methodology
Top 5 categories were selected based on user engagement.

### Insights
- English remains the preferred language across most categories.
- Certain categories exhibit demand for multilingual content.

### Business Value
Improves localization strategy.

---

## 8️⃣ Impact of Subtitles on Viewer Engagement

### Objective
Analyze the relationship between subtitle availability and viewer engagement.

### Visual Used
- Line Chart

### Insights
- Courses with more subtitle options generally attract more viewers.
- Subtitle availability improves accessibility and reach.

### Business Value
Supports investment in subtitle generation.

---

## 9️⃣ Top 3 Instructors by Rating

### Objective
Identify top-performing instructors for each category and subcategory.

### DAX Ranking Measure

```DAX
Instructor Rank =
RANKX(
    ALL(Online_Courses[Instructor]),
    [Average Rating],
    ,
    DESC
)
```

### Insights
- Top-rated instructors consistently receive better learner feedback.
- Potential candidates for future partnerships.

### Note
This visual is implemented as a **static ranking table** as required.

---

## 🔟 Course Duration vs Viewer Engagement

### Objective
Analyze how course duration impacts viewer engagement.

### Duration Conversion Rules

| Duration Type | Hours |
|--------------|--------|
| 1 Month | 60 |
| Flexible Schedule | 200 |

### Insights
- Medium-length courses generally attract higher engagement.
- Extremely long courses tend to experience lower completion interest.

### Business Value
Helps optimize course structure and content planning.

---

# 📌 Key Findings

### Most Popular Categories
- Information Technology
- Computer Science
- Data Science

### Highest Engagement Drivers
- High Ratings
- Subtitle Availability
- Optimized Course Duration

### Language Insights
- English is the dominant language.
- Regional language content offers growth opportunities.

### Instructor Insights
- Top-rated instructors can be targeted for strategic partnerships.

---

# 📊 Dashboard Pages

### Page 1 – Executive Summary

Includes:
- Total Courses
- Average Rating
- Total Registered Users
- Average Registrations
- Course Type Analysis
- Language Distribution
- Category-wise Viewer Analysis

### Page 2 – Advanced Analysis

Includes:
- Average Registrations by Category
- Subtitle Impact Analysis
- Course Duration vs Views
- Category Ranking
- Rating Analysis

---

## 📷 Dashboard Screenshots

### Executive Dashboard

![Dashboard1](dashboard1.png)

### Advanced Analytics Dashboard

![Dashboard2](dashboard2.png)

---

# 📁 Project Structure

```bash
EdTech-Online-Course-Analysis/
│
├── Dataset/
│   └── Online_Courses.csv
│
├── PowerBI/
│   └── EdTech_Analysis.pbix
│
├── Images/
│   ├── dashboard1.png
│   └── dashboard2.png
│
├── README.md
│
└── Project_Report.pdf
```

---

# 🚀 Future Improvements

- Sentiment Analysis on Reviews
- Revenue Forecasting
- Student Retention Analysis
- Course Recommendation System
- Predictive Analytics using Machine Learning


### Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Modeling
- DAX Calculations
- Business Intelligence
- Dashboard Design
- Data Visualization

---
# 👨‍💻 Author

**RAJAN KUMAR**

Data Analyst | Power BI Developer

## ⭐ Support

If you found this project helpful, consider giving it a **Star ⭐** on GitHub.
