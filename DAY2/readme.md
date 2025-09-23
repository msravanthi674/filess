# 🚢 Titanic Dataset: Exploratory Data Analysis (EDA)

Welcome to a deep dive into the Titanic disaster using hands-on data analysis!  
This project showcases the key steps, visualizations, and insights from studying the legendary passenger manifest.

---

## 📋 Project Overview
This notebook investigates the classic Titanic dataset, applying an exploratory approach to:

- Summarize key statistics for passenger features  
- Visualize distributions and outliers  
- Explore feature relationships via correlation and plots  
- Reveal the factors that shaped survival outcomes  

---

## 🗂 Data
- **Source**: Titanic passenger manifest (`Titanic-Dataset.csv`)  
- **Features**: PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked  

---

## 🛠 How to Run
1. Download the dataset and notebook files from this repository.  
2. Install required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`.  
3. Open `Titanic_EDA.ipynb` in **Jupyter Notebook** or **VS Code**.  
4. Run notebook cells in order to see the full analysis and graphs.  

---

## 🔬 Analytical Steps
- **Data Inspection**: Info, null-value checks, summary statistics  
- **Distribution Analysis**: Histograms and boxplots for `Age`, `Fare`, etc.  
- **Categorical Exploration**: Survival rates across `Sex`, `Pclass`, `Embarked`  
- **Feature Relationships**: Pairplot, heatmap correlation matrix  
- **Insights**: Patterns linking survival to gender, class, fare, and embarkation  

---

## 💻 Example Code Block
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv("Titanic-Dataset.csv")
sns.countplot(x="Sex", hue="Survived", data=df)
```
---
## 📊 Key Findings
- Women and children had higher survival rates compared to men  
- First-class passengers were more likely to survive  
- Fare and age had notable outliers  
- Embarkation port 'S' was most common, but survival rates varied by port  

---
## 👩‍💻 Tech Stack
- **Python**, **pandas**, **numpy**  
- **seaborn**, **matplotlib**  
