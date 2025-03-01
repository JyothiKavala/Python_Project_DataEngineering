# Automated ETL Pipeline for Top 10 Largest Banks by Market Capitalization

This project automates the extraction, transformation, and loading (ETL) of financial data for the top 10 largest banks in the world, ranked by market capitalization. The processed data is stored in multiple currencies (USD, GBP, EUR, and INR) and saved both as a CSV file and an SQL database table.

## Project Overview
The ETL pipeline follows these key steps:

1. Extract: Scrapes the latest data from a Wikipedia page using BeautifulSoup and stores it in a Pandas DataFrame.
2. Transform: Converts market capitalization to GBP, EUR, and INR using exchange rates from a CSV file.
3. Load: Saves the transformed data as a CSV file and loads it into an SQL Server database.
4. Query Execution: Runs predefined queries on the database for analysis.
5. Logging: Tracks the progress of each stage in a log file (code_log.txt).

## Features
1. Automated Data Extraction – Scrapes market capitalization data from Wikipedia.
2. Data Transformation – Converts values to GBP, EUR, and INR using exchange rates.
3. Data Persistence – Saves processed data as a CSV file and an SQL database table.
4. Logging System – Logs key events to code_log.txt for easy debugging.
5. Scalability – Can be re-executed every financial quarter for updated reports.

## Technologies Used
- Python
- Pandas – For data manipulation
- BeautifulSoup – For web scraping
- NumPy – For numerical operations
- SQL Server – For database storage
- PyODBC – For SQL Server connection
- Requests – For fetching webpage data

##  Sample Output  

| Name                           | MC_USD_Billion | MC_GBP_Billion | MC_EUR_Billion | MC_INR_Billion  |
|--------------------------------|---------------|---------------|---------------|---------------|
| JPMorgan Chase                 | 432.92        | 346.34        | 402.62        | 35910.71      |
| Bank of America                | 231.52        | 185.22        | 215.31        | 19204.58      |
| Industrial and Commercial Bank  | 194.56        | 155.65        | 180.94        | 16138.75      |

## Future Enhancements
1. Automate the extraction at scheduled intervals (e.g., quarterly).
2. Store the data in a cloud database (e.g., AWS RDS, Azure SQL).
3. Build a dashboard for visual analysis using Power BI or Tableau.
