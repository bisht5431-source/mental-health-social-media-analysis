<div align="center">


<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Mental%20Health%20%26%20Social%20Media%20Analytics&fontSize=32&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Power%20BI%20Dashboard%20%7C%20Student%20Wellness%20Intelligence&descAlignY=58&descSize=16"/>

<!-- Badges -->
[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)](#)
[![Domain](https://img.shields.io/badge/Domain-Mental%20Health-8B5CF6?style=for-the-badge)](#)
[![Dataset](https://img.shields.io/badge/Dataset-Student%20Data-EC4899?style=for-the-badge)](#)

</div>

---

## 🧠 Project Overview

> **How does social media use affect the mental health of students worldwide?**

This Power BI dashboard investigates the relationship between **social media habits**, **academic pressure**, **sleep patterns**, and **mental health outcomes** across a student population. Built for data analysts, researchers, educators, and wellness professionals who need fast, visual answers from complex behavioral data.

---

## 📸 Dashboard Preview

<img width="1302" height="734" alt="Screenshot 2026-06-08 152313" src="https://github.com/user-attachments/assets/ba952135-3bd0-46e5-af86-9b06c215813f" />


```
📁 assets/
    └── dashboard_preview.png   ← Drop your screenshot here
```

<!-- Uncomment after adding screenshot -->
<!-- ![Dashboard Preview](assets/dashboard_preview.png) -->

---

## 🎯 Key KPIs Tracked

| KPI | Description |
|-----|-------------|
| 👥 **Total Students** | Total respondents in the dataset |
| 🔴 **High Stress Rate %** | Percentage of students classified as high-stress |
| 📱 **Avg Daily Usage Hours** | Average daily social media usage per student |
| 🧬 **Avg Mental Health Score** | Mean mental health score across all students |
| 😴 **Avg Sleep Hours** | Average nightly sleep duration per student |

---

## 📊 Dashboard Visuals

| Visual | Chart Type | Insight Delivered |
|--------|-----------|-------------------|
| **Stress Segment Distribution** | Donut Chart | Breakdown of students by stress level category |
| **Hours Spent by Intent** | Clustered Bar | Social media usage hours grouped by purpose of use |
| **Mental Health Across Every Age** | Line Chart | Age-wise trend of average mental health score |
| **Top 5 Platforms Affecting Mental Health** | Clustered Column | Which platforms correlate with the highest/lowest scores |
| **Avg Mental Health Score vs Target** | Gauge | Current score vs a defined mental health target benchmark |
| **Physical Activity by Academic Level** | Funnel Chart | How physical activity hours vary across academic levels |

---

## 🔍 Interactive Filters (Slicers)

Users can dynamically slice all visuals by:

- 🌍 **Country**
- 🚻 **Gender**
- 📱 **Most Used Platform**
- 🎂 **Age**

---

## 🧮 DAX Measures Used

```dax
-- Total students in the dataset
Total Students = COUNTROWS('public students_data')

-- High stress classification rate
High Stress Rate % = 
    DIVIDE(
        CALCULATE(COUNTROWS('public students_data'), 'public students_data'[stress_level] = "High"),
        [Total Students]
    ) * 100

-- Average daily social media usage
Avg Daily Usage Display = AVERAGE('public students_data'[avg_daily_usage_hours])

-- Average mental health score
Avg Mental Health Score = AVERAGE('public students_data'[mental_health_score])

-- Average sleep hours
Avg Sleep Hours = AVERAGE('public students_data'[sleep_hours])

-- Stress percentage by each level
Stress % by Level = 
    DIVIDE(COUNTROWS('public students_data'), [Total Students]) * 100

-- Mental health target benchmark
Mental Health Target = 7   -- (target threshold value)
```

---

## 🗂️ Data Model

### Tables

| Table | Role |
|-------|------|
| `public students_data` | Fact table — raw student-level survey records |
| `Dax Formulas` | Measures table — all custom DAX calculations |

### Key Columns in `students_data`

| Column | Description |
|--------|-------------|
| `age` | Student age |
| `gender` | Gender identity |
| `country` | Country of the student |
| `academic_level` | Undergraduate / Postgraduate / PhD etc. |
| `most_used_platform` | Primary social media platform |
| `avg_daily_usage_hours` | Daily hours on social media |
| `purpose_of_use` | Reason for using social media (study, entertainment, etc.) |
| `mental_health_score` | Self-reported or assessed mental health score (0–10 scale) |
| `stress_level` | Stress classification (Low / Medium / High) |
| `physical_activity_hours` | Weekly physical activity hours |

---

## 💡 Key Insights

- 📉 **Mental health scores decline** with increased daily social media usage beyond 4 hours
- 😴 **Sleep deprivation** is strongly correlated with high stress classification
- 🎓 **Postgraduate students** show the lowest average physical activity hours
- 📱 **Platform choice matters** — certain platforms consistently associate with lower mental health scores
- 👩‍🎓 **Age 20–22** is the most vulnerable band, showing the lowest average mental health scores

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| **Power BI Desktop** | Dashboard design, data modeling, publishing |
| **DAX** | All custom measures and KPI calculations |
| **Power Query (M)** | Data cleaning and transformation |
| **PostgreSQL** | Source database (`public.students_data` table) |

---

## 📁 Repository Structure

```
mental-health-social-media-powerbi/
│
├── 📊 Mental_Health.pbix          ← Main Power BI file
├── 📄 README.md                   ← You are here
│
├── 📁 assets/
│   └── dashboard_preview.png      ← Dashboard screenshot
│
├── 📁 data/
│   └── students_data_sample.csv   ← Sample dataset (optional)
│
└── 📁 dax/
    └── measures.dax               ← All DAX measures (text export)
```

---

## 🚀 How to Use

1. **Clone this repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/mental-health-social-media-powerbi.git
   ```

2. **Open the dashboard**
   - Open `Mental_Health.pbix` in **Power BI Desktop** (free download from Microsoft)

3. **Connect your data** *(if using your own dataset)*
   - Go to **Home → Transform Data → Data Source Settings**
   - Point to your PostgreSQL instance or load the CSV sample

4. **Explore the dashboard**
   - Use the slicers (Country, Gender, Platform, Age) to filter all visuals interactively

---

## 📬 Connect with Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL)

</div>

---

<div align="center">

**⭐ If this project helped you, please consider giving it a star!**

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer"/>

</div>
