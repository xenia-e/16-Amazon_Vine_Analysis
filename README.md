# 16-Amazon_Vine_Analysis
analyzing Amazon reviews written by members of the paid Amazon Vine programm

# Purpouse

Purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members in provided dataset.

## Methods 

Use **PySpark** to perform the **ETL process** to extract the dataset, transform the data, connect to an **AWS RDS instance**, and load the transformed data into **pgAdmin**. Next, you’ll use **PySpark** to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

### Deliverables
__Deliverable 1:__ Perform ETL on Amazon Product Reviews ([Amazon_Reviews_ETL.ipynb](https://github.com/xenia-e/16-Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ETL.ipynb))
__Deliverable 2:__ Determine Bias of Vine Reviews([Vine_Review_Analysis.ipynb](https://github.com/xenia-e/16-Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb))
__Deliverable 3:__ A Written Report on the Analysis [(README.md)](https://github.com/xenia-e/16-Amazon_Vine_Analysis/blob/main/README.md)

### Resourses
a dataset from the [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) (Musical_Instruments)



#Results

Using  PySpark we performed analysis to determine if there is any bias towards reviews that were written as part of the Vine program. Perforomed calculations lead us to folowing conclusions (see figure 1 and 2):

- Total number of Vine reviews: 60, while total number of NON-Vine reviews: 14477

- There were 34  5-stars Vine reviews  vs 8212 non-Vine reviews  5 stars.

- There were about 57% of 5-stars reviews from both Vine and non-Vine reviewers

![Vine revewes summary table](https://github.com/xenia-e/16-Amazon_Vine_Analysis/blob/main/analysis/vine_summary.png)

>Figure 1 - Vine revewes summary table

![non-Vine revewes summary table](https://github.com/xenia-e/16-Amazon_Vine_Analysis/blob/main/analysis/non_vine_summary.png)

>Figure 2 - non-Vine revewes summary table


#Summary

As we can see percentage of positive reviews is same for Vine and non-Vine user. So it is safe to asume that there is no positivity bias for reviews in the Vine program for current dataset. 

Taking into account that comon users are moe likely to leave review after negative experience we can assume that in our case all Vine users reviews are trustforthy.

Additionally we could analyse the statistical distribution (mean, median and mode) of the star rating for the Vine and non-Vine reviews. So as analize texts of reviews for similarity, usage of similar word constructions and style, to eliminate fake rewies
