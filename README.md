# DataTales: Student Performance Explorer Dashboard

**Group Project:** ICT305
**Team Members:** Warda Baig, Areeba Shoaib, Lidya Tesfay Adal, Hiba Zubairi, Wadiqa Baig
**Date:** 8th November 2025 

---

## 📖 Introduction

### The Problem
In the current emerging academic practices, total study hours cannot be the only element to consider when justifying a student's performance. It is also possible that everyday habits, lifestyle choices, and personal experiences can have an impact on a student's academia. Although previous studies have examined independent variables such as study time or sleep time, there is a knowledge gap regarding the joint effect of these diverse influences (Lakhani, 2024; Mary, 2024). To answer the question of the relationship between various habits, situations, and exam performance, we will identify trends that provide informative findings for students seeking self-improvement and educators seeking to enhance their existing teaching techniques.

### The Goal
To build an interactive dashboard that presents actionable insights on the correlation between student habits and academic results, which will enable educators and students to make better decisions in order to improve academic results.

### Target Audience
* **Primary:** Educational administrators and academic advisors.
* **Secondary:** Parents who are seeking their student’s improvement insights.
* **Tertiary:** Researchers in educational psychology and policymakers.

### The Dataset
The dataset, "Student Habits vs Academic Performance", is acquired from Kaggle’s open-source repository (Nath, 2025). It contains 1,000 student records, which include individual features related to daily lifestyle habits, socio-demographic characteristics, and final exam performance.

### The Dashboard
The Student Performance Explorer Dashboard has been developed using Dash and Plotly within a Jupyter Notebook environment. This interactive dashboard allows users to visually analyse student data and explore patterns in academic performance, lifestyle habits, and socio-economic factors. 

The dashboard aims to:
* Present student data through clear and interactive visualisations.
* Help identify relationships between study habits, mental health, and exam outcomes.
* Support data-driven discussions on student wellbeing and performance.

---

## ⚙️ Data Preprocessing

The raw dataset (`student_habits_performance.csv`) was imported using the pandas library for cleaning and transformation. 

**Key preprocessing steps included:**
* **Handling Missing Values:** Identified 91 missing values in the `parental_education_level` column. Since this feature was not needed for our current study hypotheses, the column was dropped entirely (`df_student.drop('parental_education_level', axis=1)`) rather than imputing the missing data.
* **Feature Engineering:** Continuous numerical columns were grouped into categorical "bins" to enhance interpretability and visualisation clarity. For example, `sleep_hours` were categorized into `<7 hrs`, `7-9 hrs`, and `>9 hrs`. `exam_score` and `social_media_hours` were similarly binned.
* **Outlier Detection:** Box plots were used to visually identify potential outliers in exam scores. Because an 'outlier' in this context (e.g., high study hours but a low score) represents real student experiences rather than an error, no outliers were removed.
* **Final Status:** The cleaned dataset was reduced from 16 to 15 columns and prepared for interactive dashboard development.

---

## 🚀 Setup & Installation

### Prerequisites
Before running the dashboard, ensure the following software is installed on your system:
* **Anaconda Navigator:** for managing Python environments and launching Jupyter Notebook.
* **Python:** 3.9 or later.
* **Jupyter Notebook:** pre-installed within Anaconda.

### Project Folder Setup
1. Extract the downloaded ZIP folder to your preferred location.
2. Ensure the extracted folder contains the following structure:
   * `assets/`: comprises of the logos and `style.css` which is used in the dashboard.
   * `Setup/`: contains the `environment.yml` file.
   * `DataTalesDashboard.ipynb`: Jupyter Notebook containing the dashboard code.
   * `student_habits_performance.csv`: Dataset file used for analysis.

### Setting up the Environment
1. Open Anaconda Navigator.
2. Navigate to **Environments** and click **Import** to load the provided `environment.yml` file from the `Setup/` folder.

### Launching the Dashboard
1. Go to the **Home** tab in Anaconda Navigator and click **Launch** under Jupyter Notebook.
2. Navigate to your extracted project folder and open `DataTalesDashboard.ipynb`.
3. In the Jupyter menu, navigate to **Kernel > Restart Kernel and Run All Cells...**.
4. The dashboard will launch locally. 

*Note: To stop or restart the dashboard, click the Stop button in the Jupyter toolbar or go to Kernel > Interrupt to release the local server.*

---

## 📚 References
* Lakhani, K. (2024). Sleep Patterns and Alertness in Class. *The International Journal of Indian Psychology*, 12(4). https://doi.org/10.25215/1204.157 
* Mary, B. J. (2024, December 30). A Quantitative Study of the Impact of Daily Study Hours on Academic Performance Among High School Students. *ResearchGate*. 
* Nath, J. (2025). Student Habits vs Academic Performance. *Kaggle.com*. https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance/data 

*The 'DataTales' logo and 'Analysis Flow' were designed with assistance from Google's Gemini 2.5 Pro.* ```
