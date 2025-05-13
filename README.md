# Customer Data Processing and Analysis Using PySpark

## Description
This project processes customer and order data using PySpark on Databricks. It includes:
- Data ingestion from CSV files.
- Data cleaning and transformation (e.g., handling missing values, date formatting).
- Aggregation and analysis (e.g., total orders per customer, average spending, failed orders).
- Joining customer and order datasets for deeper insights.

## Features
- Reads customer and order data from CSV files.
- Cleans and transforms data:
  - Fills missing values for `city`, `state`, and `country`.
  - Converts `registration_date` to a proper date format.
  - Extracts year and month from `registration_date`.
  - Adds ranking columns (`Rank`, `Dense_Rank`, `Row_Number`) based on registration dates.
- Performs aggregation and analysis:
  - Total orders per customer.
  - Average spending per customer.
  - Failed orders count by status.
  - Monthly order trends.
- Joins customer and order datasets for comprehensive analysis.
- Saves processed data in Parquet format.

## Technologies Used
- PySpark
- Databricks
- Python

## Installation Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/hrithikwayal14/databricks-pyspark-project.git 
   cd MyProject
    ```
2. Install dependencies:
    ```bash
   pip install -r requirements.txt
   ```
3. If running on Databricks:
- Import the notebook into your Databricks workspace.
- Attach the cluster with the required libraries (e.g., PySpark).
- Run the notebook cells sequentially.

3. If running locally:
- Use spark-submit or a local Spark setup to execute the scripts.
## Input Data

- Place your input CSV files (`customers.csv` and `orders.csv`) in the `data/` folder.
- Ensure the column names match the expected schema:
  - **Customers**: `customer_id`, `name`, `city`, `state`, `country`, `registration_date`, `is_active`
  - **Orders**: `order_id`, `customer_id`, `order_date`, `total_amount`, `status`

## Output Data

- Processed data will be saved in the `processed_data/` folder in Parquet format.

