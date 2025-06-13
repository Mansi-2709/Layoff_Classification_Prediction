# Layoff_Classification_Prediction

![image](https://github.com/user-attachments/assets/0af5f8f0-7dd8-4175-8d1c-15ff9801252c)

Tech firms around the globe are fighting the economic slowdown. The slow consumer spending, higher interest rates by central banks and strong dollars overseas are hinting towards possible recession and tech firms have started laying employees off. This economic slowdown has made Meta recently fire 13% of its workforce, which amounts to more than 11,000 employees.

The data availability is from when COVID-19 was declared as a pandemic i.e. 11 March 2020 to present (21 Apr 2025).<br> The data has following information:
- company : Name of the company
- location : Location of company headquarters
- total_laid_off : Number of employees laid off
- date : Date of layoff
- percentage_laid_off : Percentage of employees laid off
- industry : Industry of the company
- source : URL of news item
- stage : Stage of funding
- funds_raised : Funds raised by the company (in Millions $)
- country : Country

In this project we will predict at what satge of funding the startup is given all the above information. The processes we have followed are listed below:
- Data Collection
- Exploratory Data Analysis(EDA)
- Preprocessing
- Data Implementation and Evaluation

## Data Collection
We have used the kaggle data set and loaded it into our notebook as pandas dataframe. 

## Exploratory Data Analysis
We find all null and duplicate values. There are no duplicate values but there are some null values which need to be handled.<br>
We find count values of all categorical columns to find the most common and least common categories.<br>
Make graphs for total_laid_off and percentage_laid_off to find the trend of the layoffs.<br>

## Preprocessing
We change the data type of date and date_added column to datetime, change coulmn percentage_laid_off, funds_raised datatype into int data type. <br>
We handle the categorical column by replacing  null values with most common values and we handle the numerical null values using Random Imputation method.<br>
We encode the categorical columns using Label Encoder.<br>
There are outliers as well but we do not remove outliers in this problem statement because there may be some huge companies which have fired in large chunks,so this data may be outlier but are useful for us.

## Data Implementation and Evaluation
- We use AdaBoostClassifier and RandomForestClassifier to predict the 'stage' variable.
- AdaBoost gives us just an accuracy of 40% and RandomForest gives us 80% accuracy. Hence we suggest using RandomForest algorithm for this problem statement.
- We have predicted the best parameters for both algorithms and used accuracy score and classification report for evaluating the algorithms.
