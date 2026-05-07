# DataTales: Student Performance Explorer Dashboard

[cite_start]**Group Project:** ICT305 [cite: 13]
[cite_start]**Team Members:** Warda Baig, Areeba Shoaib, Lidya Tesfay Adal, Hiba Zubairi, Wadiqa Baig [cite: 14, 15, 16, 17, 18]
[cite_start]**Date:** 8th November 2025 [cite: 12]

---

## 📖 Introduction

### The Problem
[cite_start]In the current emerging academic practices, total study hours cannot be the only element to consider when justifying a student's performance[cite: 24]. [cite_start]It is also possible that everyday habits, lifestyle choices, and personal experiences can have an impact on a student's academia[cite: 24]. [cite_start]Although previous studies have examined independent variables such as study time or sleep time, there is a knowledge gap regarding the joint effect of these diverse influences (Lakhani, 2024; Mary, 2024)[cite: 24]. [cite_start]To answer the question of the relationship between various habits, situations, and exam performance, we will identify trends that provide informative findings for students seeking self-improvement and educators seeking to enhance their existing teaching techniques[cite: 24].

### The Goal
[cite_start]To build an interactive dashboard that presents actionable insights on the correlation between student habits and academic results, which will enable educators and students to make better decisions in order to improve academic results[cite: 24].

### Target Audience
* [cite_start]**Primary:** Educational administrators and academic advisors[cite: 24].
* [cite_start]**Secondary:** Parents who are seeking their student’s improvement insights[cite: 24].
* [cite_start]**Tertiary:** Researchers in educational psychology and policymakers[cite: 24].

### The Dataset
[cite_start]The dataset, "Student Habits vs Academic Performance", is acquired from Kaggle’s open-source repository (Nath, 2025)[cite: 24]. [cite_start]It contains 1,000 student records, which include individual features related to daily lifestyle habits, socio-demographic characteristics, and final exam performance[cite: 24].

### The Dashboard
[cite_start]The Student Performance Explorer Dashboard has been developed using Dash and Plotly within a Jupyter Notebook environment[cite: 24]. [cite_start]This interactive dashboard allows users to visually analyse student data and explore patterns in academic performance, lifestyle habits, and socio-economic factors[cite: 24]. 

The dashboard aims to:
* [cite_start]Present student data through clear and interactive visualisations[cite: 24].
* [cite_start]Help identify relationships between study habits, mental health, and exam outcomes[cite: 24].
* [cite_start]Support data-driven discussions on student wellbeing and performance[cite: 24].

---

## ⚙️ Data Preprocessing

[cite_start]The raw dataset (`student_habits_performance.csv`) was imported using the pandas library for cleaning and transformation[cite: 25]. 

**Key preprocessing steps included:**
* [cite_start]**Handling Missing Values:** Identified 91 missing values in the `parental_education_level` column[cite: 25]. [cite_start]Since this feature was not needed for our current study hypotheses, the column was dropped entirely (`df_student.drop('parental_education_level', axis=1)`) rather than imputing the missing data[cite: 25].
* [cite_start]**Feature Engineering:** Continuous numerical columns were grouped into categorical "bins" to enhance interpretability and visualisation clarity[cite: 25]. [cite_start]For example, `sleep_hours` were categorized into `<7 hrs`, `7-9 hrs`, and `>9 hrs`[cite: 25]. [cite_start]`exam_score` and `social_media_hours` were similarly binned[cite: 25].
* [cite_start]**Outlier Detection:** Box plots were used to visually identify potential outliers in exam scores[cite: 25]. [cite_start]Because an 'outlier' in this context (e.g., high study hours but a low score) represents real student experiences rather than an error, no outliers were removed[cite: 25].
* [cite_start]**Final Status:** The cleaned dataset was reduced from 16 to 15 columns and prepared for interactive dashboard development[cite: 25].

---

## 🚀 Setup & Installation

### Prerequisites
Before running the dashboard, ensure the following software is installed on your system:
* [cite_start]**Anaconda Navigator:** for managing Python environments and launching Jupyter Notebook[cite: 26].
* [cite_start]**Python:** 3.9 or later[cite: 26].
* [cite_start]**Jupyter Notebook:** pre-installed within Anaconda[cite: 26].

### Project Folder Setup
1. [cite_start]Extract the downloaded ZIP folder to your preferred location[cite: 26].
2. [cite_start]Ensure the extracted folder contains the following structure[cite: 26]:
   * [cite_start]`assets/`: comprises of the logos and `style.css` which is used in the dashboard[cite: 26].
   * [cite_start]`Setup/`: contains the `environment.yml` file[cite: 26].
   * [cite_start]`DataTalesDashboard.ipynb`: Jupyter Notebook containing the dashboard code[cite: 26].
   * [cite_start]`student_habits_performance.csv`: Dataset file used for analysis[cite: 26].

### Setting up the Environment
1. [cite_start]Open Anaconda Navigator[cite: 26].
2. [cite_start]Navigate to **Environments** and click **Import** to load the provided `environment.yml` file from the `Setup/` folder[cite: 26].

### Launching the Dashboard
1. [cite_start]Go to the **Home** tab in Anaconda Navigator and click **Launch** under Jupyter Notebook[cite: 26].
2. [cite_start]Navigate to your extracted project folder and open `DataTalesDashboard.ipynb`[cite: 26].
3. [cite_start]In the Jupyter menu, navigate to **Kernel > Restart Kernel and Run All Cells...**[cite: 26].
4. The dashboard will launch locally. 

[cite_start]*Note: To stop or restart the dashboard, click the Stop button in the Jupyter toolbar or go to Kernel > Interrupt to release the local server[cite: 26].*

---

## 📚 References
* Lakhani, K. (2024). Sleep Patterns and Alertness in Class. [cite_start]*The International Journal of Indian Psychology*, 12(4). https://doi.org/10.25215/1204.157 [cite: 28]
* Mary, B. J. (2024, December 30). A Quantitative Study of the Impact of Daily Study Hours on Academic Performance Among High School Students. [cite_start]*ResearchGate*. [cite: 28]
* Nath, J. (2025). Student Habits vs Academic Performance. [cite_start]*Kaggle.com*. https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance/data [cite: 28]

[cite_start]*The 'DataTales' logo and 'Analysis Flow' were designed with assistance from Google's Gemini 2.5 Pro.* [cite: 28]
