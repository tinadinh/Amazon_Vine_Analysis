# Amazon_Vine_Analysis

## Overview of the analysis: Explain the purpose of this analysis.
This project analyzes Amazon reviews of products in the category "Shoes" written by members of the paid Amazon Vine program. We use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we use PySpark to determine if there is any bias toward favorable reviews from Vine members the dataset.

## Results:
### Vine reviews 
![vine_reviews](https://user-images.githubusercontent.com/33900637/158005685-0568c4f2-bf2f-46f1-a495-0587112a6aae.png)

### Non-Vine reviews
![nonvine_reviews](https://user-images.githubusercontent.com/33900637/158005689-fbd6a574-798e-4345-ba38-8860d43f6580.png)

## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
As shown in the above tables, the percentages of 5-star reviews for the paid and unpaid types are 59.1% and 53.6%, respectively. The 5-star reviews account for a slightly higher percentage of all paid reviews than they do in the unpaid group. However, this difference is not significant considering the difference in size of 2 groups. Therefore, there is no significant bias for reviews for shoes products in the Vine program.

