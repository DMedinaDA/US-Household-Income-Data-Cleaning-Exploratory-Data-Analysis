# US-Household-Income-Data-Cleaning-Exploratory-Data-Analysis

A complete MySQL project that cleans and explores the us_project household income dataset (2020–2024 ACS estimates) to answer:

Which states and cities have the highest/lowest mean and median household incomes?

How do land vs. water mass correlate with income?

Which area types (Borough, City, CDP, Community, etc.) earn the most?

Where are the wealthiest and poorest cities in each state?

📁 Datasets
Table	Purpose	Rows (after cleaning)
us_household_income	Geographic details (state, county, city, place, type, land/water)	~45,000
us_household_income_statistics	Income metrics (mean, median, primary income by ID)	~45,000
Database: us_project (MySQL 8.0+)

🎯 Business & Policy Questions Answered
Where should a retailer target high-end stores? → Rich cities in CA, VA, MD, MA.

Which states need economic stimulus? → Lowest mean/median: MS, AR, WV, LA.

Do larger land areas correlate with wealth? → No clear pattern; Texas is huge but mid-tier in income.

What area type earns the most? → Cities > Boroughs > CDPs > Communities.

🛠️ Requirements
MySQL 8.0+ (window functions: ROW_NUMBER() OVER)

Database: us_project

Tables: us_household_income, us_household_income_statistics


📝 Lessons Learned
Always check for import artifacts (garbled column names, hidden characters).

Duplicates can hide in seemingly unique IDs; use ROW_NUMBER() to catch them.

Manual corrections are sometimes unavoidable for typos in state/city names.

Inner joins are safest when one table has missing matches; document what you drop.

Mean vs. Median: Mean can be skewed by a few ultra-wealthy households; median tells the “typical” story.
