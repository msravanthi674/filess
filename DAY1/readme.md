# 🚢 Titanic Dataset Preprocessing

Welcome to the **Titanic data preprocessing project**!  
This repository demonstrates the essential steps for cleaning, encoding, and scaling data in preparation for machine learning using the iconic Titanic dataset.

---

## 📋 Project Overview
- **Dataset**: Titanic passenger data  
- **Goal**: Prepare raw data for machine learning modeling  
- **Focus**: Null handling, categorical encoding, feature scaling, and outlier analysis  

---

## 🔬 Data Source
**Dataset file**: `Titanic-Dataset.csv`  

**Features**:
- PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked  

---

## 🛠 Preprocessing Steps

### 1. Data Loading
- Imported the dataset using pandas  
- Verified columns and structure  

### 2. Missing Values
- Filled missing **Age** entries with the column mean  
- Filled missing **Embarked** entries with the mode (most frequent value)  

### 3. Feature Encoding
- Label encoded **Sex** (binary categorical)  
- One-hot encoded **Embarked** (multicategorical)  

### 4. Feature Scaling
- Standardized **Age** (zero mean, unit variance)  
- Normalized **Fare** (range 0–1)  

### 5. Preview & Output
- Displayed the processed dataset for further analysis  

---

## 💻 Code Structure

The notebook is organized in modular steps:  

```python
# 1. Load Libraries and Data
import pandas as pd
from sklearn.preprocessing import LabelEncoder, StandardScaler, MinMaxScaler
df = pd.read_csv('Titanic-Dataset.csv')

# 2. Handle Missing Values
df['Age'].fillna(df['Age'].mean(), inplace=True)
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)

# 3. Encoding
le = LabelEncoder()
df['Sex'] = le.fit_transform(df['Sex'])
df = pd.get_dummies(df, columns=['Embarked'])

# 4. Scaling
df['Age_scaled'] = StandardScaler().fit_transform(df[['Age']])
df['Fare_normalized'] = MinMaxScaler().fit_transform(df[['Fare']])

# 5. Preview
df.head()
```

## 🎯 Learning Outcomes

By completing this project, you will:

- Understand how to preprocess raw data for ML tasks  
- Master techniques for null handling, encoding, and feature scaling  
- Gain hands-on experience with **pandas** and **scikit-learn**  

---

## 📦 Files

- **Titanic-Dataset.csv** → Raw passenger data  
- **notebook.ipynb** → Data preprocessing notebook  
- **README.md** → Project summary and usage guide  
