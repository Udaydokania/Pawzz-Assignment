# Pawzz® Animal Care Directory: Data Infrastructure & Pipeline

## Project Overview
This repository contains a scalable data infrastructure designed to build a "Practo-standard" directory of verified animal care services across India. The system focuses on transforming "messy" community-sourced data into a structured, auditable PostgreSQL database.

## 🚀 Key Features
* **5-Stage Automated Workflow:** Implements a structured lifecycle (**Submitted → Needs Fix → Ready → Verified → Live**).
* **Intelligent Cleaning (Regex):** Custom Python scripts to normalize inconsistent phone formats into a universal +91 standard.
* **Duplicate Detection (Fuzzy Matching):** Utilizes `RapidFuzz` to identify potential duplicate listings with high name similarity.
* **Automated Red Flag Audit:** Programmatic identification of invalid phones, missing addresses, and NAP inconsistencies.


## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, RapidFuzz, Matplotlib, Seaborn
* **Database:** PostgreSQL (Architecture detailed in the Technical Annex)
* **Environment:** Jupyter Notebook / Quadratic AI

## 📂 Repository Structure
* `Documentation/`: Final project proposal PDF.
* `Notebooks/`: End-to-end Python pipeline for data cleaning and deduplication.
* `Data/`: 
    * `raw_community_data.csv`: "Messy" dataset generated for stress-testing.
    * `verified_directory.csv`: Final unique, standardized records.

## 📊 Results Summary
The pipeline successfully processed the dataset, identifying:
* **12 Phone Duplicates**.
* **6 Exact Duplicates** (automatically flagged and removed).
* **Zero Missing Addresses**.
