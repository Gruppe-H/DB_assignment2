# DB_assignment2
SPA - Study points assigment for Database

## MongoDB

### 1. Explore the data and formulate considerations about a hosting database.
We chose to do minimal cleaning of the data, since MongoDB handles unstructered data well. 

### 2. Design and develop proper database structure of the requested type.
##### JSON
We made all the datasets into JSON files to import them into the mongodb.
* dataframe_1.json
* dataframe_2.json
* dataframe_3.json
* dataframe_4.json
* dataframe_5.json


### 3. Ingest the data into the database, include pre-processing of it, if necessary.
We pre-processed the data slightly, to make sure all objects in the database have the same field called 'Organisation' instead of 'Organization' or 'Account' etc. We did the same with 'City', 'C40 City' and 'Organisation Number' and more. Then we created JSON files for each data set and used MongoBD Compass to import the data directly from the files.


### 4. Design and develop operations for maintenance of the database.
We have implemented sharding and replica sets for maintaining the database

### 5. Formulate ten relevant questions for extracting information from the database, design and develop database functionality for implementing the information extraction (for the relevance consult the instructor).
1. Is there a correlation between population and total emissions?
2. From 2016 to 2017, has there been a reduction in base emissions?
3. From 2016 to 2017, what change has there been in target emission?
4. Is there a difference in the target reduction emissions based on whether or not the city is a member of C40 or GCoM?
5. What difference is there between each region and their target emission?
6. Which organization plans to reduce the most in %?
7. For each country, how many cities in that country is represented in the data?
8. How many countries are represented in the data?
9. How many have a desired target emission without a base emission?
10. What is the most commeon sector?

Answers for the questions can be found in the frontend, _see Frontend code._


### 6. Design and implement a model for scaling the database, considering ACID and/or CAP theorem rules.
We have implemented horizontal scaling by sharding and using replica sets. We added all the data almost without changing anything, since MongoDB can handle the unstructured data.

### 7. Validate and test all database operations.
We tested it with the aggregation pipelines and by using CRUD operations on some data.

### 8. Evaluate the database’s performance and suggest measures for improving it.
* Not really needed, as the amount of data is still too low to need these measures/optimizatioins (only at most some 2000 rows in a table)
* Potentially something to look into, if one wants to scale the database further (say hypothetically, the database were to be updated yearly, how much data would be added?)


### 9. Document your work, describing the product and the process. Apply graphical notation (diagrams), when it is possible.
We used Jupyter Notebook to create some JSON files from the data to import into our MongoDB collection. We created the MongoDB to have 2 shards each with 3 replica sets, and we created 2 mongo routers and 3 config servers, following this [tutorial](https://ankitkumarakt746.medium.com/mongodb-sharded-cluster-with-replica-set-in-docker-81322c903513). Then we created some aggregation pipelines to answer our 10 questions, and made a very simple Node.js frontend, where the answers to each question, and also the aggregation pipelines in this [folder](https://github.com/Gruppe-H/db2_frontend/blob/master/aggregations/aggregations.js), can be found.  

### 10. Formulate conclusions and recommendations.

Answers for the questions can be found under images where the result of stored prosedures and views are.
* Here is the conslusion and recommendation for question 1.

## Frontend code
Simple Node.js frontend

Github [link](https://github.com/Gruppe-H/db2_frontend)
