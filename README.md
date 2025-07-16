# Global Layoffs EDA Using MySQL

## Project Overview
This project focuses on exploring global layoffs data using **MySQL**. The analysis uncovers insights into how layoffs have impacted different industries, companies, countries, and time periods. The primary objective is to use SQL to answer real-world business questions and identify patterns in workforce reductions.

## Dataset
The dataset was obtained from [Kaggle's World Layoff Dataset]([https://www.kaggle.com/),](https://www.kaggle.com/datasets/swaptr/layoffs-2022) which includes information on:
- Company Name
- Total Laid Off
- Percentage Laid Off
- Industry
- Country
- Date
- Company Size
- Stage (e.g., Seed, Series A, Public)

## Tools & Technologies Used
- **MySQL**
- **MySQL Workbench**
- **GitHub**
- **VS Code** (for writing and organizing SQL queries)


---

## Key Business Questions Explored
-  Which companies recorded the highest number of layoffs?
-  What industries were most affected globally?
-  Which countries experienced the most layoffs?
-  What was the trend of layoffs over the years?
-  How does the percentage of laid-off employees vary by company size?

---
## Sample SQL Queries

```sql
-- Top 10 companies with the highest layoffs
SELECT company, SUM(total_laid_off) AS total_layoffs
FROM layoffs
GROUP BY company
ORDER BY total_layoffs DESC
LIMIT 10;

-- Total layoffs by country
SELECT country, SUM(total_laid_off) AS country_layoffs
FROM layoffs
GROUP BY country
ORDER BY country_layoffs DESC;

-- Layoffs trend by year
SELECT YEAR(date) AS year, SUM(total_laid_off) AS yearly_layoffs
FROM layoffs
GROUP BY YEAR(date)
ORDER BY year;


---
## Key Insights
Tech companies dominate the top of the layoffs list, especially post-2020.

United States, India, and Canada had the highest layoffs globally.

Layoffs spiked significantly in 2022 and 2023, particularly in startups and public companies.

Tech, Finance, and Consumer industries were among the most affected sectors.

Smaller companies (under 500 employees) experienced higher layoff percentages on average.
