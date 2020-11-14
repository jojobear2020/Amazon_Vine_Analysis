# Amazon_Vine_Analysis


### TOOLS


1.	**PySpark** – to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. It was also used to analyze the data.

2.	**pgAdmin** – to create a database for our working data


### ANALYSIS OVERVIEW

In this project we analyzed Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.


We had access to approximately 50 datasets, each one contains reviews of a specific product. For this analysis, I selected a datasaet containing reviews of the baby products.

[](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Baby_v1_00.tsv.gz)


### RESULTS

Questions to answer:

1.	*How many Vine reviews and non-Vine reviews were there?* 

2.	*How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?*

3.	*What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?*


The results :


![](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary.PNG)


![](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary.PNG)



### SUMMARY

•	As we see from the results above, only 463 reviews were paid (Vine).

•	On a contrary, 25,094 reviews were unpaid (non-Vine). 

•	Out of all paid (Vine) reviews only 202 (43.63%) were 5-star.

•	Unpaid (non-Vine) reviews surprisingly show a slightly higher results with 47.95% of all reviews being 5-star (12,033 total).
