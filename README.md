# Amazon_Vine_Analysis

## Overview 
The purpose of this analysis is to conduct an analysis on a dataset that contains reviews of a specific product, in this case, shoes from Amazon. The dataset contains information regarding Amazon reviews (such as customer info, product info, review text, review date, etc.) written by members of the paid Amazon Vine program. We use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin for anaylsis. Next, we use PySpark to determine if there is any bias toward favourable reviews from Vine members throughout dataset.

## Resources
- Data Sources: amazon_reviews_us_Shoes_v1_00.tsv
- Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS, PySpark

## Results:
- There were a total of 22 Vine reviews and 26,987 non-Vine reviews
- For 5-star reviews, there were 13 Vine reviews and 14,475 non-Vine reviews
- The percentage of 5 star reviews, 59.1% were Vine reviews and 53.6% were non-Vine reviews

This dataframe is the top 20 rows of the vine_table
![table](https://user-images.githubusercontent.com/33900637/158006051-268e2845-00b0-4ac1-89a2-9a21a1ab7d3e.png)

## Summary: 
With the dataframes, it can be concluded that there is a slight positivity bias for the reviews in the Vine program since 59.1% of the Vine reviews were 5-stars. This is likely due to the fact that members of this program have a slant towards rating the shoes in a positive manner since they got the product for free. On the other hand, a significant number of the reviews come from people who are not in the Vine program and 53.6% still gave the shoes a 5-star review. It can be concluded that even though someone is more likely to write a positive review for a free product, the product itself could still be worthy of those reviews. Therefore, there is no significant bias for reviews for shoes products in the Vine program. An additional analysis that can be performed is to determine how many times each member of the Vine program reviewed a similar product. For instance, if a Vine member is typically reviewing fashion products instead of electronics, then that member is perhaps more likely to be invested in the shoe reviews and write a positive review. Therefore, it could be helpful for the potential customers to know more information on the person giving the review to provide more insight.
