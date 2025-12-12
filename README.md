Team: Soham Sarvade, Annie Niland, Fangzhou Zheng, Bei SU
Predicting Book Popularity Using Goodreads Data

This project analyzes a large Goodreads dataset to understand what drives book ratings and long term popularity. Using PySpark, we cleaned and structured millions of book and review records, explored key patterns, and built models to predict both average ratings and future engagement.

Project Summary

The raw Goodreads data comes as large, nested JSON files that are difficult to work with directly. We standardized schemas, removed unnecessary fields, and converted everything to Parquet for faster and more reliable processing. Books were then joined with their reviews and enriched with clean publication dates.

A major focus of the project was early momentum. For each book, we created time based features that captured review activity in the first few months after publication and compared them to engagement years later.

What We Analyzed

We explored how ratings and popularity vary across genres, how genre trends change over time, and how author reputation relates to book performance. We also examined whether early reviews can predict long term success.

Modeling Approach

Two types of models were built.

To predict average ratings, we used a Random Forest model. This showed that author reputation, publisher, and genre matter far more than numeric traits like page count or publication year.

To predict long term review volume, we used linear regression. Early review counts were extremely predictive of engagement five to ten years later, resulting in very strong model performance.

Key Takeaways

Author and publisher reputation play a major role in ratings
Early engagement strongly predicts long term popularity
Genre affects audience size more than rating
Most books settle into their long term trajectory within the first few years

Tools Used

PySpark
Spark SQL
Pandas and Matplotlib
Random Forest Regression
Linear Regression

Dataset: https://www.google.com/url?q=https%3A%2F%2Fcseweb.ucsd.edu%2F%7Ejmcauley%2Fdatasets%2Fgoodreads.html
