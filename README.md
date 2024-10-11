# Home_Sales

## Project Overview
This project utilizes PySpark to analyze a dataset of home sales, focusing on key metrics such as average home prices based on various attributes (e.g., number of bedrooms, bathrooms, square footage, etc.). The purpose of this analysis is to uncover trends in the real estate market, particularly how specific features impact home prices over time.

## Dataset
The dataset used in this project contains information on home sales, including:
- Sale price
- Number of bedrooms and bathrooms
- Square footage
- Year built
- View rating
- Date of sale

The dataset is provided in CSV format, and PySpark was used for querying and analyzing the data.

## Methodology
1. **Data Loading**: The data is read from a CSV file and loaded into a Spark DataFrame.
2. **SQL Queries**: SparkSQL is used to answer the following questions:
   - What is the average price for a four-bedroom house sold for each year?
   - What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms?
   - What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet?
   - What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000?
   
3. **Caching**: The data is cached for performance comparisons when running queries.
4. **Partitioning**: The data is partitioned by the `date_built` field and saved in Parquet format to improve query performance.

## Assumptions
- The dataset is assumed to be accurate and free of missing data.
- Price trends are assumed to reflect market demand without accounting for external economic factors such as interest rates or location-specific trends.

## Results
Key insights from the analysis include:
- Prices for homes with specific features (3 bedrooms, 3 bathrooms, 2 floors, and ≥ 2,000 sq ft) have increased steadily over time, indicating growing demand for larger homes.
- Homes with higher view ratings tend to have higher average prices, particularly when the average price is $350,000 or more.

## Conclusion
This analysis provides valuable insights for homebuyers and real estate investors. Future analyses could consider more granular factors, such as location and economic trends, to improve the depth of insights.
