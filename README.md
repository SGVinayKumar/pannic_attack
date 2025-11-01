# 🧠 Panic Attack Data Analysis Dashboard

This Power BI project explores a dataset on panic attacks, analyzing symptoms, triggers, demographics, and behavioral patterns to uncover key insights. The goal is to understand the prevalence and patterns of panic attack symptoms and contributing factors across different age groups and demographics.

## 📊 Overview

This interactive dashboard provides a comprehensive analysis of panic attack data sourced from Kaggle. It visualizes symptom frequency, demographic breakdowns, lifestyle factors, and correlations between panic scores, sleep, and triggers. The project demonstrates data cleaning, transformation, and visualization using SQL and Power BI, with DAX formulas like `IF` and `SWITCH` to derive meaningful metrics.

---

## 📁 Dataset

- **Source**: [Kaggle - Panic Attacks Dataset](https://www.kaggle.com/)
- **Format**: CSV
- **Imported via**: Snowflake
- **Data Cleaning & Profiling**: Performed using SQL (null handling, data type casting, outlier treatment, and normalization)

---

## 🛠️ Tools & Technologies

| Tool/Tech     | Purpose                              |
|---------------|--------------------------------------|
| **Snowflake** | Cloud data warehouse for ingestion   |
| **SQL**       | Data cleaning and transformation     |
| **Power BI**  | Data modeling and dashboard creation |
| **DAX**       | Custom metrics and logic             |

---

## 🧮 DAX Formulas Used

- **IF Statement**:  
  ```DAX
  Panic_Level = IF([Panic_Score] > 6, "High", IF([Panic_Score] > 3, "Medium", "Low"))
  ```

- **SWITCH Statement**:  
  ```DAX
  Trigger_Category = SWITCH(TRUE(),
      [Trigger] = "PTSD", "Trauma",
      [Trigger] = "Caffeine", "Stimulant",
      [Trigger] = "Phobia", "Fear",
      [Trigger] = "Social Anxiety", "Social",
      [Trigger] = "Stress", "Stress-related",
      "Other"
  )
  ```

---

## ⚙️ Prerequisites

To explore or modify this project, ensure you have:

- Power BI Desktop installed
- Access to Snowflake (optional if using local CSV)
- Basic knowledge of SQL and DAX
- Dataset downloaded from Kaggle: `panic_attacks.csv`

---

## 🔍 Key Insights

- **Top Symptoms**:
  - Sweating (836 patients), Dizziness (620), Trembling (590), Chest Pain (487), Shortness of Breath (487)
- **Gender Distribution**:
  - Data includes Female, Male, and Non-binary categories (exact counts not specified)
- **Trigger Analysis**:
  - PTSD is the most common trigger selected
- **Sleep Patterns**:
  - Most patients sleep between 6–8 hours; fewer sleep <5 or >9 hours
- **Panic Attack Duration**:
  - Majority last between 2–10 minutes; few extend to 30–40 minutes
- **Alcohol Consumption**:
  - Varies widely; some patients report 0–4 drinks/week, others up to 30+
- **Age Group Comparison**:
  - Adolescents show higher average sleep hours and panic scores than adults
  - PTSD and Social Anxiety are more impactful in adolescents

---

## ❓ Analytical Questions Framed

1. What are the most common symptoms reported during panic attacks?
2. How do panic triggers vary across age groups?
3. Is there a correlation between sleep hours and panic score?
4. How does alcohol consumption relate to panic attack frequency?
5. What is the average duration of panic attacks?
6. Are there gender-based differences in symptom reporting?
7. How do adolescents and adults differ in panic response patterns?

---

## 📌 Conclusion

This project demonstrates how data visualization and analytics can uncover meaningful patterns in mental health data. By leveraging Power BI and DAX, we’ve built a dashboard that can support awareness, early detection, and intervention strategies for panic attacks.



