# Amazon_Vine_Analysis

## Overview of the analysis: Explain the purpose of this analysis.
This project analyzes Amazon reviews of products in the category "Shoes" written by members of the paid Amazon Vine program. We use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we use PySpark to determine if there is any bias toward favorable reviews from Vine members the dataset.

The purpose of this project was to conduct an analysis on a dataset that contains reviews of a specific product, in this case, shoes from Amazon. The dataset contains information regarding shoe reviews conducted on amazon by members of the paid Amazon Vine program, which provides members with the product so they are required to publish a review. The dataset that was provided by Amazon contains all information pertaining to the product reviews such as customer info, product info, review text, review date, etc. The dataset was extracted and transformed, connected to an AWS RDS instance, and loaded into pgAdmin for analysis. Pandas was also used to determine if there were any bias towards favorable reviews from the Vine members throughout the dataset.

## Resources
- Data Sources: amazon_reviews_us_Shoes_v1_00.tsv
- Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS, PySpark

## Results:
- There were a total of 22 Vine reviews and 26,987 non-Vine reviews
- For 5-star reviews, there were 13 Vine reviews and 14,475 non-Vine reviews
- The percentage of 5 star reviews, 59% were Vine reviews and 54% were non-Vine reviews

The dataframe below shows a snapshot of the top 20 rows of the vine_table that was created and exported from pgAdmin 4 and read into a dataframe using Pandas.
![table](https://user-images.githubusercontent.com/33900637/158006051-268e2845-00b0-4ac1-89a2-9a21a1ab7d3e.png)

## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
As shown in the above tables, the percentages of 5-star reviews for the paid and unpaid types are 59.1% and 53.6%, respectively. The 5-star reviews account for a slightly higher percentage of all paid reviews than they do in the unpaid group. However, this difference is not significant considering the difference in size of 2 groups. Therefore, there is no significant bias for reviews for shoes products in the Vine program.

In summary, there are more unpaid non-Vine reviews than paid Vine reviews for shoes on Amazon. It can be concluded that there is a slight positivity bias for the reviews in the Vine program (those who are getting the product for free), since 59% of the Vine reviews were 5-stars. This is likely due to the fact that members of this program have a slant towards rating the shoes in a positive manner since they did not have to pay for them, and potentially hoping that if they write a good review, they will be sent more products in the future. On the other hand, a significant number of the reviews come from people who are not in the Vine program and 54% still gave the shoes a 5-star review. It can be concluded that even though someone is more likely to write a positive review for a free product, the product itself could still be worthy of those reviews. Overall, it is advisable to analyze reviews that are not part of the Vine program when considering purchasing a product.

An additional analsis that can be performed with the given dataset that would support this statement, would be to determine how many times each member of the Vine program reviewed a similar product. For instance if a Vine member is typically reviewing fashion products instead of electronics, then that member is perhaps more likely to be invested in the shoe reviews and write a positive review. Therefore, it could be helpful for the potential customer to know more information on the person giving the review to provide more insight.
