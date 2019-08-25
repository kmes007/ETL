
Extract* 
Two .csv files were imported to Jupyter for this project from Kaggle. BreweriesData and the Population data from the U.S. Census, both from 2014. These would be used to create a relationship between population data and the number of breweries per state. 




Transfer*
First a df.info was done to get an overview of the data in order to determine if there were any missing values. There
were extraneous columns in the Breweries csv file so the columns were filtered to show only the necessary data. The 
names of the breweries were removed. There was also an unnamed column in the brewery file which was the index of the 
original which was no longer necessary when placed in a Pandas dataframe. The city column was kept in order to determine if the information would be valueable for analysis. Next, the dataframe was passed into the value_counts() function by state in order to determine how many breweries were in each state. 

Another dataframe was made with the Population data from the U.S. Census. This .csv file was brought 
into the notebook and removed all information to simply look at population by state. The two tables were combined on 
the state code through pd contcat. There were two columns named state, so the state column from the Population data file was renamed. Also the columns with the brewery count and population count were renamed and reordered to facilitate the concat process as well as to provide a common key (state) for importation into SQL. 


Load*
Using SQL alchemy, a table was created called Brewery Count. Now we have a new table created to be used for future. 
This way if we wanted to add more data rows, perhaps the next time the census comes out, we can continue to use this 
DB. Additionally the two previous data frames containing population data and brewery count data were also loaded into 
SQL to facilitate future analysis if more data were to become available. 
