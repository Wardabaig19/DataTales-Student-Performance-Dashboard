# DataTales: Student Performance Explorer Dashboard

**Group Project:** ICT305  
**Team Members:** Warda Baig, Areeba Shoaib, Lidya Tesfay Adal, Hiba Zubairi, Wadiqa Baig  
**Date:** November 8, 2025  

---

## 📖 Introduction

### The Problem
Evaluating academic performance requires a multidimensional approach. Traditional metrics often focus solely on total study hours, overlooking the substantial impact of everyday habits, lifestyle choices, and environmental factors. While previous studies have isolated variables like sleep or study duration, understanding their combined effect remains a challenge. For instance, does a student with excessive study hours but poor sleep outperform one with balanced habits? This project addresses that knowledge gap by replacing subjective methods with a data-driven strategy to uncover trends that can guide self-improvement and teaching methodologies.

### The Goal
To create an interactive dashboard that visualizes the correlations between student habits and academic outcomes, empowering educators and students to make informed, data-backed decisions.

### Target Audience
* **Primary:** Educational administrators and academic advisors.
* **Secondary:** Parents seeking insights to support their children's academic journeys.
* **Tertiary:** Policymakers and researchers in educational psychology.

### The Dataset
The project utilizes the "Student Habits vs Academic Performance" dataset from Kaggle. Comprising 1,000 unique records, it captures a comprehensive view of student life, including demographic traits, daily habits, and final exam scores.

### The Dashboard
Built with Python, Dash, and Plotly in a Jupyter Notebook environment, the Student Performance Explorer Dashboard enables the visual analysis of this dataset. 

Key objectives include:
* Visualizing complex student data interactively and intuitively.
* Uncovering the relationships between mental health, study routines, and exam results.
* Facilitating data-driven discussions regarding student wellbeing.
<img width="2802" height="1620" alt="Screenshot 2026-05-07 212011" src="https://github.com/user-attachments/assets/a7225672-bee2-4c48-a726-8e618a3690e3" />
<img width="2840" height="1630" alt="Screenshot 2026-05-07 212114" src="https://github.com/user-attachments/assets/a5aa2ecd-1aba-4337-abb8-95fb505df3e9" />
<img width="2854" height="1620" alt="Screenshot 2026-05-07 212207" src="https://github.com/user-attachments/assets/b97155ee-0857-49f9-910d-7c95d767dc0a" />


---

## ⚙️ Data Preprocessing

Data preparation was conducted using the Pandas library to ensure accuracy and consistency before building the visualizations.

* **Handling Missing Data:** Identified 91 null values within the parental education feature. As this variable was outside the scope of our primary hypotheses, the entire column was dropped to maintain dataset integrity.
* **Feature Engineering:** Continuous variables were transformed into categorical bins for clearer visualization. Sleep hours were divided into sub-optimal (<7 hrs), optimal (7-9 hrs), and above-optimal (>9 hrs) ranges. Similar binning was applied to exam scores and social media usage.
* **Outlier Analysis:** Box plots were utilized to check for anomalies. Data points outside standard ranges (e.g., high study hours with low grades) were retained, as they represent valid, real-world student experiences rather than systemic errors.

---

## 🚀 Setup & Installation

### Prerequisites
* **Anaconda Navigator** (for environment management and Jupyter access)
* **Python 3.9+**
* **Jupyter Notebook**

### Project Folder Structure
Extract the downloaded project ZIP file. Ensure your directory contains the following structure:
* `assets/`: Contains dashboard styling (`style.css`) and project logos.
* `DataTalesDashboard.ipynb`: The main Jupyter Notebook application containing the dashboard code.
* `student_habits_performance.csv`: The analytical dataset.

### Environment Setup
Open the **Anaconda Prompt** (Windows) or Terminal (Mac) and install the necessary dependencies manually by running the following commands:
```bash
pip install dash
pip install dash-bootstrap-components
pip install pandas
```
---

## 📚 References
* Lakhani, K. (2024). Sleep Patterns and Alertness in Class. *The International Journal of Indian Psychology*, 12(4). https://doi.org/10.25215/1204.157 
* Mary, B. J. (2024, December 30). A Quantitative Study of the Impact of Daily Study Hours on Academic Performance Among High School Students. *ResearchGate*. 
* Nath, J. (2025). Student Habits vs Academic Performance. *Kaggle.com*. https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance/data 

*The 'DataTales' logo and 'Analysis Flow' were designed with assistance from Google's Gemini 2.5 Pro.* 
