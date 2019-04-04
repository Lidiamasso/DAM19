# **Assignment: Get Familiar with S3**
#### **Task:**
 ● **Online Travel Company uses S3 to store statistics on successful and failed searches data for the hotel reservation. As a data analyst you will help the Head of Product.**
 
●**Head of Product wants to know: What is the estimated monthly cost, the company needs to pay for storing this data?**

● **You should answer the question and prepare a brief summary that justify your answer.**

#### **Useful context:**
● **The company operates approximately with 5000 different destinations and 5 years (60 months) of data.** 

● **Searches are stored by location and time. Every location and month is represented by a file similar to:** 
*s3://data.public.bdatainstitute.com/dam18/search_logs/2018/09/2018_09_18452212_log.json*  
*(filename contains: Year, Month and ServiceID)*

Getting the sizes of files:

~~~
aws s3 ls s3://data.public.bdatainstitute.com/dam/query_logs/ --human-readable --recursive
~~~
| August | September | Average Monthly
| ---------- | ---------- |----------|
| 272 KiB   | 227.5 KiB   | 249,75 KiB |
| 138 Bytes   | 133 Bytes   |135,5 Bytes|
Results for 1 month and 1 destination

With **60 months** of data and **5000** destinations:
Storage in Kib ~ 115,575,000 KiB
Storegae in Bytes ~ 40,650,000 Bytes
Sotarage total in GB = 76,7 GB

### Find out the price to storage in Amazon S3 ###

In this [link](https://calculator.s3.amazonaws.com/index.html) you can calculate the  **monthly** price of your storage

**First**
    : Chose the region --> EU(Paris)
    
**Second**
: Write down the Storage in GB -->76,7

**Result**
: $1.73

There are different prices for each region. Let's see some different regions:
- Asia Pacific (Tokio): $3,64
-  US East (N.Virginia): $5,42
-  South America (Sao Pablo):$ 8,53


















 

