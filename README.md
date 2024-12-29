# T20_World_cup_Analysis

Have done Data analysis in 4 steps:

Data Extraction - From scraping.

Data Transformation - We transformed the data using PowerQuery.

Data Modeling - Now with the help of DAX we have Modeled the data and Build parameters.

Dashboard - Building Dashboards and insight collection.

The Data I have downloaded from Kaggle having 4 Datasets.

Data Transformation (Power Query)

Now we will do Data Transformation with the help of PowerQuery.

1. **Players Information with Images**:
   
   a. This comprises information related to Players eg. Match Name, Batsman Name, Batting position, RUN, Out, NOT Out, 6s and 4s, Strike Rate, Out or not.
   
   b. In bating summary batsman name uses some words in bracket for the role he is playing eg. Caption(C), Wicket keeper(WK) so we have removed them as to maintain the 
      consistency in names.
   
   c. In the Add Column tab under From Text group use the Extract Text before delimeter fuction to remove the unwanted characters.
   
   d. Then Trim it and remove duplicates values as these may affect our analysis.
   
3. **Match Summary**
   
   a. Applied all the basic operations for data cleaning from removing null values to removing duplicate values and changing the column Data types.
   
   b. Now we have created the new column named as **Stage** to bifercate rows based on its stage. i.e Super12 or Qualifier.
   
5. **Bowling summary**
   
   a. Given relevent column names, like o's = Zeros, 1's = Ones and so on.
   
   b. Created a column named Balls from Overs column. (How many balls he has bowled)
   
   c. Renamed out/Not out column and replaced 2 text values into binary as it will help us during analysis.
   
7. **Batting Summary**
   
   a. All the basic cleaning and renaming steps including changing DataTypes.

**Data Modeling**:

a. Now we have modelled the data on the basis of Fact and Dimension Table.

   Facts: These are the parameters. Store quantitative data for analysis, Contains Primary Key, surrounded by Dimension table. {Batting and Bowling Summary}
   
   Dimension: These are the attributes. Descriptive attributes that provide context for the Fact tables. {Match summary and Players information}
   
b. Now we will match the Star schema One to many(*).

**Dax Measures**: For Dashboard making

Now I have created 14 measures and 2 Calculated columns these will helpus in dashboard making.

**Batting Key Measures**:

Total Runs

Total Innings Batted

Total Innings Dismissed

Batting Average

Total balls Faced

Strike Rate

Batting Position

Boundary %

Avg. balls Faced

**Bowling Key Measure:**

Wickets

balls Bowled

Runs Conceded

Bowling Economy

Bowling Strike Rate

Bowling Average

**Calculated columns**

Boundary runs

Boundary runs bowling

Custom Batting Order
