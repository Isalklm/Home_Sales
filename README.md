# Home Sales Analysis with PySpark

This project analyzes home sales data using **PySpark** for big data processing. The dataset contains various features, such as the number of bedrooms, bathrooms, square footage, and more. The analysis includes querying, caching, partitioning, and performance comparison of PySpark SQL queries.

## Project Overview

The following tasks were performed in this project:

1. **Setup and Installation**:
   - Installed Apache Spark and Java.
   - Set up environment variables for `SPARK_HOME` and `JAVA_HOME`.
   - Installed necessary Python libraries: `findspark` and `py4j`.

2. **Loading and Processing Data**:
   - Read a home sales dataset from an AWS S3 bucket into a PySpark DataFrame.
   - Created a temporary SQL view for querying.

3. **SQL Queries**:
   - Calculated the **average price** of four-bedroom houses per year.
   - Computed the **average home price per year** for homes with **3 bedrooms and 3 bathrooms**.
   - Filtered results to include homes with **3 bedrooms, 3 bathrooms, 2 floors, and at least 2000 square feet**.
   - Found the **average home price per view rating** for homes priced **above $350,000**.
   - **Cached** the table and compared query performance with cached vs. uncached data.

4. **Performance Optimization**:
   - Measured query execution time before and after caching the dataset.
   - Partitioned the dataset by `date_built` for optimized queries.
   - Read the partitioned data and stored it in **Parquet format** for efficient retrieval.

5. **Final Steps**:
   - Created a **temporary table** for partitioned data.
   - Verified that caching improved performance.
   - **Uncached** the table after completion.
     
## Results and Insights

- **Caching** significantly improved query performance, reducing execution time.
- **Partitioning data by `date_built`** optimized query efficiency when retrieving specific years.
- Using **PySpark SQL**, we analyzed **trends in home prices over different years and attributes**.

## How to Run

1. Open the **Google Colab** link in this repository.
2. Run all the cells in order to install Spark and load the dataset.
3. Experiment with the queries and modify filters for custom analysis.
4. Compare performance using **caching and partitioning**.
5. Save results and export to **Parquet** format for optimized storage.

## License

This project is open-source under the [MIT License](https://opensource.org/licenses/MIT).
