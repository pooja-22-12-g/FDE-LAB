# 🧪 LAB-1: Data Ingestion Using Python

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

---

## 📌 Aim

To ingest and explore **structured**, **semi-structured**, and **unstructured** datasets using Python, and understand the characteristics of different data types by loading and displaying them in a Python environment.

---

## 📖 Introduction

In data engineering, data is collected from multiple sources and exists in various formats. Understanding how to ingest and interpret these data types is a fundamental skill for building efficient and reliable data pipelines.

### 📊 Types of Data
- **Structured Data** – Fixed schema (CSV, Excel)
- **Semi-Structured Data** – Flexible schema (JSON)
- **Unstructured Data** – No predefined format (Text files)

This experiment demonstrates how Python can be used to handle all three types efficiently.

---

## 📂 Datasets Used

| Data Type | File Format | Description |
|---------|------------|-------------|
| Structured | `.csv` | Housing dataset |
| Structured | `.xlsx` | Play Tennis dataset |
| Semi-Structured | `.json` | Flat & nested JSON files |
| Unstructured | `.txt` | Text data |

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas**
- **JSON Module**
- **Google Colab**

---

## 🔄 Algorithm / Steps

1. Create a new notebook in Google Colab  
2. Upload structured, semi-structured, and unstructured datasets  
3. Import required Python libraries  
4. Load CSV and Excel files using Pandas  
5. Parse JSON files (flat and nested)  
6. Read text data  
7. Display dataset samples  
8. Compare data formats  

---

## 💻 Code Implementation

```python
import pandas as pd
import json

# Structured Data
df_excel = pd.read_excel("Play_tennis_dataset.xlsx")
print("\nExcel File Head:")
print(df_excel.head())

df_csv = pd.read_csv("Housing_uncleaned.csv")
print("\nCSV File Head:")
print(df_csv.head())

# Unstructured Data
df_txt = pd.read_csv("dummy_text.txt", delim_whitespace=True)
print("\nText File Head:")
print(df_txt.head())

# Semi-Structured Data
df_json_flat = pd.read_json("normal_json.json")
print("\nNormal JSON File Head:")
print(df_json_flat.head())

with open("nested_json.json") as f:
    nested_data = json.load(f)

df_json_nested = pd.json_normalize(nested_data)
print("\nNested JSON File Head:")
print(df_json_nested.head())
