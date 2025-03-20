# Automated ETL Pipeline with Apache Airflow

This project demonstrates a **complete data pipeline** using Apache Airflow to automate the ETL (Extract, Transform, Load) process, integrate machine learning, and manage workflow operations.

---

## Project Overview
- **Objective:** Automate the ETL process and integrate machine learning into the workflow.  
- **Tech Stack:** Apache Airflow, Python, Pandas, Scikit-learn, MySQL  
- **Key Features:**  
  - Automated data extraction, transformation, and loading (ETL)  
  - Integration of a machine learning model for diabetes prediction  
  - Workflow orchestration using Airflow DAGs  

---

## Pipeline Architecture
1. **Data Extraction:**  
   - Fetch diabetes-related data from external APIs using `requests`.  
2. **Data Transformation:**  
   - Clean, preprocess, and prepare data for ML using `pandas`.  
3. **Machine Learning Integration:**  
   - Train and deploy a diabetes prediction model using `scikit-learn`.  
4. **Data Loading:**  
   - Store processed data and model outputs in a MySQL database using `sqlalchemy`.  

---

## Code Structure
- **`dags/`:** Contains Airflow DAG definitions for workflow orchestration.  
  - `sample.py`: Main DAG for the ETL pipeline.  
  - `proof.py`: Testing/validation DAG.  
  - `Diabetes_unseen.py`: DAG for processing unseen data.  
  - `diabetes_records.py`: DAG for processing diabetes records.  
  - `DataTrans.py`: DAG for data transformation.  
- **`scripts/`:** Includes Python scripts for data extraction, loading, and ML.  
  - `DataExtraction.py`: Fetches raw data using `requests`.  
  - `DataLoading.py`: Loads processed data into MySQL using `sqlalchemy`.  
  - `ml.py`: Trains and integrates the ML model using `scikit-learn`.  
- **`requirements.txt`:** Lists all Python dependencies.  

---

## How to Run
1. Install dependencies:  
   ```bash
   pip install -r requirements.txt
2. Start Apache Airflow:
  airflow standalone
3. Upload the DAGs to Airflow and trigger the pipeline.

---

##Skills Demonstrated
-**Data Engineering**: ETL pipeline design, workflow automation

-**Machine Learning**: Model training and integration

-**Tools**: Apache Airflow, Python, Pandas, Scikit-learn, MySQL
