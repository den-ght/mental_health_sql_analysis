# 🧠 Mental Health of International Students — SQL Analysis Project

This project explores the mental health of international students using SQL inside a Jupyter Notebook. The dataset comes from a Japanese university survey conducted in 2018 and aims to understand how international status and length of stay impact depression, social connectedness, and acculturative stress.

---

## 📁 Dataset Overview

| Column Name     | Description                                               |
|-----------------|-----------------------------------------------------------|
| `inter_dom`     | Type of student (`Inter` or `Dom`)                        |
| `japanese_cate` | Japanese language proficiency                             |
| `english_cate`  | English language proficiency                              |
| `academic`      | Current academic level (`Undergraduate`, `Graduate`)      |
| `age`           | Age of the student                                        |
| `stay`          | Length of stay in years                                   |
| `todep`         | Depression score (PHQ-9 test)                             |
| `tosc`          | Social connectedness score (SCS test)                     |
| `toas`          | Acculturative stress score (ASISS test)                   |

---

## 🎯 Project Goal

To use SQL queries to:
- Compare mental health metrics between international students based on years of stay.
- Identify whether longer stay reduces depression or improves social connectedness.
- Practice working with PostgreSQL using real-world mental health data.

This project was originally inspired by a DataCamp DataLab challenge (2024). All SQL code was written independently and executed in a local Jupyter Notebook environment.

---

## 🧪 SQL Query Example

```sql
SELECT stay,
       COUNT(inter_dom) AS count_int,
       ROUND(AVG(todep), 2) AS avg_depression,
       ROUND(AVG(tosc), 2) AS avg_social_connection,
       ROUND(AVG(toas), 2) AS avg_stress
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay;
```

---

## 📊 Tools Used

- PostgreSQL for data analysis
- Jupyter Notebook (`.ipynb`) using `%%sql` cells
- GitHub for version control

---

## 📎 Files in This Repo

- `students.csv` — Dataset
- `notebook.ipynb` — SQL-based analysis notebook
- `mentalhealth.jpg` — Project visualization
- `README.md` — This file

---

## 🧠 Visual Overview

![](mentalhealth.jpg)

---

## 📌 Attribution

This project is inspired by the DataCamp DataLab challenge:  
**“Mental Health of International Students”**  
Available via: [DataCamp DataLab Project](https://www.datacamp.com/datalab/w/8628a42e-3ccd-4718-bd09-dd083790e749)

Dataset and general concept are provided by DataCamp.  
All SQL queries, visualizations, and explanations in this repository were written independently by me for learning and portfolio purposes.

---

## ✅ License

MIT License — free to use, share, and modify.

> ⚠️ This repository is intended strictly for educational and demonstration purposes only. It is not affiliated with or endorsed by DataCamp.

