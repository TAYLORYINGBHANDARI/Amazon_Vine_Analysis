# Amazon_Vine_Analysis

 analyzing Amazon reviews written by members of the paid Amazon Vine program.

## Resources

- Data Source: [https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt] (Amazon Review datasets), [https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz] (Video Games Review dataset)

- Language & Software: Google Colab Notebook,PySpark, PostgreSQL 12.6, pgAdmin 4, AWS RDS

## Project Overview
Perform an cloud ETL process by picking one of the dataset(Video Games) from the Amazon Review datasets.Use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin.
By the end,use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the dataset. 

### completing tasks
* Deliverable 1: Perform ETL on Amazon Product Reviews
    1. create an AWS RDS database, then import schema and create tables in pgAdmin.

    2. use Google Colab Notebook to extract the Videogames dataset into a Dataframe,and transform into four separate DataFrames that match the table schema in pgAdmin.
    3. Upload the transformed data into tables and run queries in pgAdmin.

* Deliverable 2:  determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.
     The total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews 
* Deliverable 3: A Written Report on the Analysis (README.md)


## Results

### How many Vine reviews and non-Vine reviews were there?

- There were 40565 total reviews,94 are paid and 40471 are unpaid.
![image](https://user-images.githubusercontent.com/85265816/135020611-218a659b-3e11-4786-97bf-a0cdeb0843fa.png)


### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- There were 48 total paid 5-star reviews and 15663 total unpaid 5-star reviews.
![image](https://user-images.githubusercontent.com/85265816/135020625-0aaa83e1-5ce7-48f2-a76d-50d8b50c588e.png)


### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?


- 51.06% of the five_star reviews were vine(paid)
- 38.70% of the five_star reviews were non-vine(unpaid)
![image](https://user-images.githubusercontent.com/85265816/135020649-7a8f67f3-6fd4-42b1-a0ba-dda0c5684e62.png)


## Summary

Based on the statistics we analyzed, it appears people tend to give higher review when review is paid. 51.06 % of the reviews in the Vine program were gaven 5 stars, whereas  only 38.70% of reviews were gaven 5 stars.This describes a positivity bias for reviews in the Vine program.

Additionally we could analyse the mean of the star rating for the Vine and non-Vine reviews to support our statement.

## Extra:

Our average star rating of paid review is 4.20 whereas average star rating of unpaid review is 3.34.

![image](https://user-images.githubusercontent.com/85265816/135020694-6c267be3-8385-4aea-ba07-fa17dea133a6.png)




