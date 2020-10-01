Flatiron Data Science Program
Module 2 

September 25, 2020

# Case Study - Hypothesis Testing

---

## Instructions
You are a DS working for Northwind, a supplier company.  Your job is find interesting relationships in their database.  They have tasked you with two questions. You'll find these in the notebooks. You are then tasked to dig into the data in a way that you find interesting.

## Data
The database for this analysis was accessed from the northWind.sqlite database provided for this study. Target data was the quantity of items per order, grouped by ordering region. 

## Question: Is there a difference in order quantity per purchasing region?

## Methods
Order and Order Detail tables were joined. The data was grouped by region, excess columns cleaned and stored in a dictionary of individual pd.DataFrames (per region). A dictionary of per region’s five point statistics p as pd.Series. 

830 unique purchases orders were split between the following purchasing regions: Western Europe, South America, Central America, North America, Northern Europe, Scandinavia, Southern Europe, British Isles and Eastern Europe.

A normal distribution was observed for 3 regions - 'Central_America', 'Northern_Europe’, 'Eastern_Europe' per the Shapiro-Wilke test at confidence level of 95%. The remaing 6 regions did not have normal distributions. 

ANOVA test was conducted to find if there was a difference in means. There was. 

Tukey testing was performed to find which regions were statistically different from the others.

## Conclusions
There are 10 regional comparisions where the means are statistically different (with confidence level of 95%).

## Future Work

1.	Further explore region ordering data by splitting it into corresponding cities.
2. Explore if higher purchase volumes are correlated with specific times of year.
3.	Explore if higher purchase volume is correlated to sales person representing the region.




