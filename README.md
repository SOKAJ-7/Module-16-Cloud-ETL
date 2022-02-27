# Module-16-Cloud-ETL

## Overview
The purpose of this project is to create a database of reviews of products bought from Amazon (in this case, video games) using an Amazon web services database, PySpark, PostgreSQL, and Google Colab notebooks. Using the same dataset, we will then determine whether the status of the reviewers 'Vine' membership has any impact on the reviews given.

## Challenges
Unfortunately, Module 1 was not able to be completed as part of this project. Upon creating the AWS relational database, I was unable to connect and copy my dataframes to the RDS. In my first attempt, the error I recieved upon running the code below (Figure 1) was "FATAL: database does not exist.". I checked to make sure my entered endpoint, port, and name were correct as well as the syntax. These checks did not reveal any obvious errors in my code. I then checked my database security and availability setting within AWS. Again, nothing seemed to be wrong. Lastly, I decided to create a new database from scratch and carefully follow instructions from the module as well as use stack exchange and similar resources for aid. This time however, I got a different error upon trying to write my dataframes to my RDS: "The connection attempt failed.". After trying many different troubleshooting methods with no success, I decided to move on to deliverable 2 and give up on setting up my SQL database. Therefore, deliverable 1 is incomplete for this assignment. 

![M16_failure](https://user-images.githubusercontent.com/93050931/155895884-86ba9e86-6890-4ffe-a090-484405b9a822.png)

(**Figure 1**: The code and error recieved as mentioned above, the login and connection credentials are not hidden as the database has since been deleted.) 

## Results
**How many Vine reviews and non-Vine reviews were there?**
There were 94 paid (Vine) reviews and 39,915 unpaid reviews.

**How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?**
There were 48 5-star reviews by Vine members and 15,556 5-star reviews by un-paid reviews.

**What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?**
51.06% of Vine reviews were 5-star reviews and 38.97% of unpaid reviews were 5-star reviews.

## Summary
I would say there is some bias uncovered by these results. The difference in the percentage of 5-star reviews between the non-Vine and Vine reviews is sizeable at ~10%. One thing to keep in mind however is that there are vastly more non-paid reviews than paid. This may impact our conclusions. One way to test if this difference is statistically significant would be to conduct a two sample t-test to determine whether the difference between the percentage of 5-star reviews is statistically significant. 
