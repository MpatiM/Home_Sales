# Home_Sales
The Module 22 assignment was completed to assess understanding of SparkSQL, PySpark, partitioning, and caching.

# Instructions
**After importing the necessary PySpark SQL functions and creating the temporary table `home_sales`, the following questions were answered based on our findings:**
* What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

  ![query1](https://github.com/user-attachments/assets/43e2094e-4e58-4be3-b1b6-00c839dab4a2)


* What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

  ![query2](https://github.com/user-attachments/assets/9c5f81b8-c9c3-4d9e-8ec0-791c7aa1ba26)


* What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

  ![query3](https://github.com/user-attachments/assets/34e558ff-5d84-4f73-ba71-220efd34e7af)


* What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

  ![query4](https://github.com/user-attachments/assets/9e9e0501-c332-42d6-b02c-49cc7c2acba4)

----
**After, cache the temp table `home_sales`. The query run time was compared to the uncached data by the following:**
* Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

  ![query5](https://github.com/user-attachments/assets/3d1eee1e-511f-46ec-bedc-c861facef735)

----
**Partition by the "date_built" field on the formatted parquet home sales data. Create another temporary table for the parquet data. The runtime is compared again to the uncached data:**
* Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

  ![query6](https://github.com/user-attachments/assets/531ba001-bc2e-44b1-987c-9a55d0415583)

----

Uncache the `home_sales` temporary table and verify that the `home_sales` temporary table is uncached using PySpark.

----
## Findings
After comparing the runtime for all three SparkSQL queries, it seems that after partitioning the data by the field "date_built" made it run significantly faster, decreaisng run time from 1.41 seconds to 0.58 seconds. 
