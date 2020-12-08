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

Based on the few queries ran using SQL, the top 10 countries listed as having the lowest rate of deaths from COVID-19 infections are: Kiribati, Samoa, Turkmenistan, Korea (north), Myanmar, New Caledonia, French Polynesia, Belgium, Peru, Spain and Italy. 

Other queries were ran to obtain lists of countries whose food intake is closest to the USDA Center for Nutrition Policy and Promotion. Belgium was listed as 9th in the vegetables Category, while it is worth noting that the United States came in 20th (37.3% Obesity and <2.5% undernorished). Spain came in number 5, Grenada was #1 (20.2% Obesity and 0 reported COVID-19 related Deaths).

For 

The quantity table lists Belgium(24.5%), Peru(19.1%), Spain (27.1%), (Italy 22.9%) as the top 4 highest death rate from COVID-19 infections. 30% is the highest percentage of obesity.  This illustrates that those countries with high obesity rates tend to have high COVID-19 related deaths. 

The highest undernourished percentage is 59% (Central African Republic) which corresponds to 

Belgium (<2.5%), Spain (<2.5%), Italy (<2.5%>) and Peru (9.7%) are considered very low undernourishment rates, which shows that Undernousrishment did not cause the increase in death rates in those countries. 




## Sources-
https://www.kaggle.com/mariaren/covid19-healthy-diet-dataset?select=Food_Supply_Quantity_kg_Data.csv