# COVID-19_and_Healthy_Diet

## Question 1 
Does a healthy diet give countries an advantage against COVID-19 infection?

## Question 2
Do countries with high Obesity rates have higher COVID-19 deaths?

* Expected results
If a healthy diet gives countries an advantage against COVID-19 infections then countries that eat a healthy diet have less COVID-19 deaths.

If a healthy diet does not gives countries an advantage against COVID-19 infections then countries that eat a healthy diet do not have less COVID-19 deaths.

* We selected Data sets from Kaggle about COVID-19 and healthy diet across several countries around the world. 
* We had one week to completely Extract, Transform, and Load data.
* The USDA Center for Nutrition Policy and Promotion recommends a very simple daily diet intake guideline: 30% grains, 40% vegetables, 10% fruits, and 20% protein.


### Extraction

We used Python to load the csv files into a dataframe using Panda. 

### Transformation

We conbined the food categories into the main 5 main categories: Grains, Vegetables, Fruits, Proteins, and Miscellaneous. We created two tables to compare the data called food_covid_df and quantity_df. We set index in both Tables to Country(170 total).

We cleaned the dataframe by dropping any unwanted columns. The food_covid_df inlcudes the food categories and the COVID-19 death, infection and recovery data. The quanity_df includes Obesity, under-nourished and COVID-19 death, infection and recovery data. 

### Loading
We created tables in PgAdmin in order to load the data in tables into the database, called food_covid data base. We then estalished a connection between Python and SQL to load the tables data into SQL database.

SQL, by default, listed our table columns in lowercase, which caused an error when we attempted the load. Therefore, we had to rename our table columns in Python to lowercase and re-set the index for both data sets.

### Analysis



## Sources-
https://www.kaggle.com/mariaren/covid19-healthy-diet-dataset?select=Food_Supply_Quantity_kg_Data.csv