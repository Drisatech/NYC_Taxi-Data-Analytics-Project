# NYC Taxi Data Analysis Project (Jan–Feb 2025)

## Project Overview

This project analyzes New York City taxi trip data from January and February 2025 to gain insights into trip patterns, payment types, and peak hours. The analysis is performed using Apache Spark with PySpark on Azure Databricks, with data stored and accessed from Azure Blob Storage using a Shared Access Signature (SAS) token.

## Data Sources

The data used in this analysis is sourced from two Parquet files located in Azure Blob Storage:

- `wasbs://nytaxi@nytaxidata2025.blob.core.windows.net/yellow_tripdata_2025-01.parquet`
- `wasbs://nytaxi@nytaxidata2025.blob.core.windows.net/yellow_tripdata_2025-02.parquet`

## Technologies Used

- **Azure Databricks:** Cloud-based platform for big data processing and analytics.
- **Apache Spark (PySpark):** Distributed computing system for large-scale data processing.
- **Azure Blob Storage:** Scalable and secure cloud storage for unstructured data.
- **Python:** Programming language used for data manipulation and analysis.
- **Matplotlib & Seaborn:** Libraries for data visualization.

## Project Steps

1.  **Mount Azure Blob Storage:** Configure and mount the Azure Blob Storage container using a SAS token to access the data files.
2.  **Load and Explore Data:** Load the January and February 2025 taxi trip data from Parquet files into Spark DataFrames. Explore the schema and sample data to understand the structure and content.
3.  **Data Cleaning and Transformation:**
    *   Handle missing values in critical columns (`tpep_pickup_datetime`, `tpep_dropoff_datetime`, `trip_distance`).
    *   Convert datetime columns to a consistent timestamp format.
    *   Filter out invalid trips (e.g., trips with zero distance).
    *   Calculate `trip_duration` in minutes.
    *   Format datetime columns to remove milliseconds for consistency.
4.  **Joining Datasets:** Combine the cleaned data from January and February into a single Spark DataFrame.
5.  **Analyzing the Data:**
    *   Calculate key metrics such as average trip duration and average fare amount.
    *   Analyze the distribution of payment types.
    *   Determine the number of trips per hour to identify peak times.
    *   Identify the top pickup and dropoff locations based on trip counts.
6.  **Visualizing the Results:**
    *   Export aggregated results (payment type counts, hourly trip counts, sample fare vs. distance data) to Pandas DataFrames.
    *   Create visualizations using Matplotlib and Seaborn to illustrate:
        *   Distribution of Payment Types
        *   Trips per Hour of Day
        *   Trip Distance vs. Fare Amount
7.  **Saving the Results:**
    *   Save the cleaned and combined dataset back to Azure Blob Storage in Parquet format.
    *   Save the aggregated analysis results (payment types, peak hours) as CSV files in Azure Blob Storage.
    *   Generate a summary report in Markdown format with key findings.

## How to Run the Project

1.  Ensure you have access to an Azure Databricks workspace.
2.  Upload the notebook to your Databricks workspace.
3.  Configure the Azure Blob Storage connection with the provided SAS token in the notebook.
4.  Run the notebook cells sequentially to execute the data loading, cleaning, analysis, visualization, and saving steps.

## Results and Insights

The analysis revealed several key insights into NYC taxi trips during January and February 2025, including average trip metrics, popular payment methods, peak travel hours, and high-traffic pickup and dropoff zones. These insights can be used for operational planning, resource allocation, and understanding urban mobility patterns.

*Key findings are summarized in the generated Markdown report.*

## Contact


For questions or further information, please contact Engr Idris Aliyu - drisatech@gmail.com.
