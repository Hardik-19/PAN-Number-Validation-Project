# Comprehensive PAN Number Validation & Cleansing Using SQL Techniques

## 📌 Objective

This project focuses on cleaning and validating a dataset of Indian Permanent Account Numbers (PAN) using pure SQL. The objective is to ensure that each PAN strictly follows the official format defined by the Income Tax Department of India. Based on the validation, PAN numbers are categorized as **Valid** or **Invalid**.

---

## 📂 Dataset

- **Filename:** `PAN Number Validation Dataset.xlsx`
- **Description:** Contains a column of PAN numbers that may include missing values, duplicates, formatting inconsistencies, or invalid entries.

---

## 🔧 Instructions

### 1. 🧹 Data Cleaning and Preprocessing

- **Handle Missing Data:** Identify and remove or impute missing PAN numbers.

- **Check for Duplicates:** Remove duplicate PAN numbers to maintain data integrity.

- **Trim Whitespaces:** Remove leading and trailing spaces in PAN numbers.

- **Correct Case:** Convert all PAN numbers to uppercase for uniformity.

---

### 2. ✅ PAN Format Validation

A **valid PAN number** must meet the following criteria:

- Exactly **10 characters** long.
- Follow the pattern: `AAAAA1234A`
  
#### Letter Rules (First 5 Characters):
- All must be **uppercase alphabets** (`A-Z`).
- **No two adjacent characters** can be the same (e.g., `AABCD` is invalid).
- Must **not form a complete alphabetical sequence** (e.g., `ABCDE`, `BCDEF` are invalid).

#### Digit Rules (Next 4 Characters):
- Must be **numeric digits** (`0-9`).
- **No two adjacent digits** should be the same (e.g., `1123` is invalid).
- Must **not form a complete numeric sequence** (e.g., `1234`, `2345` are invalid).

#### Last Character:
- Must be an **uppercase alphabet** (`A-Z`).

#### ✅ Example of a Valid PAN: AHGVE1276F
#### ✅ Example of a Invalid PAN: AGGVE1276F | AHGVE1176F | AHgVE1276f ....

---

### 3. 📊 Categorization

- **Valid PAN:** Meets all the format and validation rules above.
- **Invalid PAN:** Fails one or more format rules, is incomplete, or contains invalid characters.
- **Missing PAN:** If any row contains a missing or empty PAN value.

---

## 📝 Output

| Total records processed | Total valid PANs | Total invalid PANs | Total missing PANs |
|-------------------------|------------------|---------------------|---------------------|
| X                       | Y                | Z                   | W                   |
---

## 💻 Tools Used

- **Structured Query Language (SQL)** – This project has been implemented entirely using SQL for data cleaning, transformation, and validation of PAN numbers. All logic, including pattern matching and classification, is executed through SQL queries without the use of any external programming languages or libraries.

- The solution is compatible with standard relational database management systems such as **MySQL**, **PostgreSQL**, **SQLite**, and **SQL Server**.
