# Amazon_Vine_Analysis



### ANALYSIS OVERVIEW

In this project we analyzed Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.


We had access to approximately 50 datasets, each one contains reviews of a specific product. For this analysis, I selected dataset containing reviews of the baby products.

[](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Baby_v1_00.tsv.gz)

________________


### TOOLS


1.	**PySpark**:
* perform the ETL process to extract the dataset
* transform the data
* connect to an AWS RDS
* load the transformed data into pgAdmin
* analyze the data

2.	**pgAdmin**: 
* to create the database for our working data for further analysis

________________________

### RESULTS

Questions to answer:

1.	*How many Vine reviews and non-Vine reviews were there?* 
2.	*How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?*
3.	*What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?*


Results :


![](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary.PNG)


![](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary.PNG)

____________


### SUMMARY

•	As we see from the results above, only 463 reviews were paid (Vine).

•	On a contrary, 25,094 reviews were unpaid (non-Vine).

•	Out of all paid (Vine) reviews only 202 (43.63%) were 5-star.

•	Unpaid (non-Vine) reviews surprisingly show a slightly higher results with 47.95% of all reviews being 5-star (12,033 total).

____________


### ADDITIONAL ANALYSIS & OBSERVATIONS

Check if there is any correlation between bias (high/low-ranked) review and reward (paid/unpaid).

1.  Our data is quite disproportional with the number of paid Vine reviews much smaller than unpaid non-Vine reviews.
2. Our results vary; however, the lowest 1-star reviews are 2x higher %-wise in paid Vine 1-star reviews vs. unpaid non-Vine reviews (see the bottom picture in this section).
3. Given the results, we may need more data to see is there is any strong bias in paid vs non-paid reviews. 
4. Another option to see if there is any bias is to compare our results from this dataset with the results from one or few more datasets for different product types (e.a. - add data for sports, software, shoes, pet products, etc.).


________________________


* **4 star**

    ![4 star Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary_4star.PNG)

    ![4 star non-Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary_4star.PNG)



* **3 star**

    ![3 star Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary_3star.PNG)

    ![3 star non-Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary_3star.PNG)



* **2 star**

    ![2 star Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary_2star.PNG)

    ![2 star non-Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary_2star.PNG)



* **1 star**

    ![1 star Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/paid_vine_reviews_summary_1star.PNG)

    ![1 star non-Vine](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_reviews_summary_1star.PNG)
    
    ____________________________
    
    
    ### PGADMIN TABLES
    
1. vine_table

![vine_table](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/vine_table_detail.PNG)
     
     
2. customer_table

![customer_table](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/customers_table_detail.PNG)
    
    
3. product_table

![products_table](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/products_table_detail.png)
    
 
4. review_id_table

![review_id_table](https://github.com/jojobear2020/Amazon_Vine_Analysis/blob/main/images/review_id_table_detail.png)
