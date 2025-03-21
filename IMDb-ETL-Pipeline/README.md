# IMDb ETL Pipeline

This project demonstrates an **ETL (Extract, Transform, Load)** pipeline applied to IMDb's "Top 250 Movies" dataset. The goal is to extract data from IMDb's website, clean and preprocess it, and load it into a MySQL database for further analysis. The pipeline includes web scraping, data transformation, and database integration.

---

## Project Overview

### **Objective**
- **Extract:** Scrape IMDb's "Top 250 Movies" data using web scraping tools.
- **Transform:** Clean and preprocess the extracted data for analysis.
- **Load:** Store the processed data in a MySQL database for querying and insights.

---

## Features

1. **Web Scraping:**
   - Extracts movie details (title, release year, rating, director, genres, etc.) from IMDb.
   - Fetches additional information like cast, crew, and production details.
   - Uses `BeautifulSoup` and `Selenium` for scraping.

2. **Data Transformation:**
   - Cleans and preprocesses raw data (e.g., handling missing values, normalizing formats).
   - Normalizes numerical data (e.g., gross revenue).
   - Structures data into a relational format for database storage.

3. **Database Integration:**
   - Loads processed data into a MySQL database.
   - Creates tables with primary and foreign keys for efficient querying.
   - Executes SQL queries to derive insights (e.g., movies by year, top directors).

---

## Technologies Used

- **Web Scraping:** `BeautifulSoup`, `Selenium`, `requests`
- **Data Processing:** `pandas`, `numpy`, `re`
- **Database:** `MySQL`, `SQLAlchemy`
- **Visualization:** `matplotlib`, `seaborn` (optional for analysis)

---

## Code Structure

IMDb-ETL-Pipeline/
- dags: Airflow DAG files (if applicable)
- scripts: Python scripts for ETL
  - DataExtraction.py: Web scraping logic
  - DataLoading.py: Database loading logic
  - ml.py: Machine learning integration (if applicable)
- data: Raw and processed data files
  - Movies_info.csv: Extracted movie details
  - full_cast_and_crew.csv: Cast and crew details
  - integrated_dataframe.csv: Final integrated dataset
- README.md: Project documentation
- requirements.txt: Python dependencies


---

## How to Run

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
2. Run the Pipeline:
   - Execute the DataExtraction.py script to scrape IMDb data.
   - Run DataLoading.py to clean and load data into MySQL.

3. Query the Database:

   - Use the provided SQL queries (or create your own) to analyze the data.

---

## Key Insights
- Movies by Release Year: Identifies trends in movie releases over time.
- Top Directors: Lists directors with the most movies in the top 250.
- Gross Revenue Analysis: Normalizes and analyzes worldwide gross revenue.

## Example Queries
1. Movies Released in 2000:
  ```bash
  SELECT * FROM movies_info WHERE `Release Year` = 2000;
```
2. ## Unique Movie Titles and IDs:
  ```bash
  SELECT DISTINCT ID, Title FROM movies_info;
```
3. Movie Counts by Release Year:
  ```bash
  SELECT `Release Year`, COUNT(*) as count FROM movies_info GROUP BY `Release Year`;
```

---

## Skills Demonstrated
- **Web Scraping**: Extracting structured data from dynamic websites.
- **Data Cleaning**: Handling missing values, normalizing data, and feature engineering.
- **Database Design**: Creating and managing relational databases with MySQL.
- **ETL Pipelines**: Building end-to-end data pipelines for real-world datasets.

---

## Contact
For questions or feedback, feel free to reach out:

- Email: mohanadassaf01@gmail.com
- LinkedIn: Mohanad Assaf
- GitHub: kabuto1012
