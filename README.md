# DB_assignment2
SPA - Study points assigment for Database

## MongoDB

### 1. Explore the data and formulate considerations about a hosting database.
##### We explored the data and made considerations for which columns to keep and discard. We have chosen to discard:
* Questionnaire
* Increases/decreases since last year
* Reasons for incr/decr
* Last update
* City short name
We didn’t see it necessary to include these because they don't hold any important information about the emissions.
* Think about how to clean/pre-process the datasets (lots of recurring data that’s partially the same). Likely to do with Python and pandas.

### 2. Design and develop proper database structure of the requested type.
##### JSON

We made all the datasets into JSON files to import them into the mongodb.
* dataframe_1.json
* dataframe_2.json
* dataframe_3.json
* dataframe_4.json
* dataframe_5.json


### 3. Ingest the data into the database, include pre-processing of it, if necessary.
* We need to clean the data before we ingest it into the database
* Starting off with finding and getting all unique Organization numbers and Organization name (names of these 2 ‘columns’ varies a bit in all datasets, also cases of same org number but slightly different names, such as 3417 ‘City of New York’ vs 3417 ‘City of New York, NY’)


### 4. Design and develop operations for maintenance of the database.

# TODO! above^

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

Answers for the questions can be found under images where the result of stored prosedures and views are.


### 6. Design and implement a model for scaling the database, considering ACID and/or CAP theorem rules.

# TODO! above^

### 7. Validate and test all database operations.

### 8. Evaluate the database’s performance and suggest measures for improving it.
* Not really needed, as the amount of data is still too low to need these measures/optimizatioins (only at most some 2000 rows in a table)
* Potentially something to look into, if one wants to scale the database further (say hypothetically, the database were to be updated yearly, how much data would be added?)


### 9. Document your work, describing the product and the process. Apply graphical notation (diagrams), when it is possible.

# TODO! above^

### 10. Formulate conclusions and recommendations.

Answers for the questions can be found under images where the result of stored prosedures and views are.
* Here is the conslusion and recommendation for question 1.

## Backend code
Spring framework backend 

* REST API
* Endpoints
* Postman (frontend)

Github link: https://github.com/Gruppe-H/DB_assignment2 
