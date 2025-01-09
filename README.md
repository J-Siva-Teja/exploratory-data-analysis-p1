**Exploratory Data Analysis**

Goal of the Project

Analysing data and to generate insights which help an OTT Platform in deciding which type of shows/movies to produce and how they can grow business in different countries.

**Analysis Approach**

**1. Insights about the dataset**

The first step towards generating useful insights from the data was to understand the data, data prepartion, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset can be performed to generate insights.

In the data cleaning step the data quality of the dataset was first assesed. After a data quality assessment the following insights were observed and the necessary process to mitigate the issues was followed :

a) Total no of records in dataset is 8807.

b) There are 12 columns in the Dataset of which 11 are of Object Type and 1 is of integer type.

c) Out of 12 columns, 6 columns are with NaN or None values for which imputation is required.

d) date_added column to be in Date Time format hence formatting is required.

e) In rating column, 3 values are related to duration column and those values are to be replaced with appropriate values.

f) In the given dataset only two columns i.e., show_id and title are with unique values and other columns have repeated values

Pre-processing of dataset i.e., unnesting the columns of Cast and Country has been carried out. With the help of unnested data Null values in Cast and Director columns have been imputed using the combination of Cast and Country, Director and Country respectively.

**2. Missing Value and Outlier Check**

a) Using isna() missing values in the columns have been detected and those values have been imputed with appropriate values by analysing other values in the dataset.

b) Using boxplot and describe() function outliers for "added_year" and "duration" have been identified using statistics like mean, lower quartile, median and upper quartile.

![image](https://github.com/user-attachments/assets/354c8059-8b90-440f-a98f-d7e641f38bef)

As per the above boxplot quite a few outliers are appearing below the year 2015. represented by black coloured circles indicating that addition of content is minimal in those year before 2015.

**3. Visual Analysis**

a) Distribution of the content type has been analysed using pie plot which shows that 69.62 % content type is of Movies and 30.38 % is of TV Shows.

![image](https://github.com/user-attachments/assets/bd561083-4e79-40a9-8f71-95abda5816b0)

b) Distribution of Movies & TV Shows every year has been analysed using histogram plot. The curve is left skewed with more content being added in a period of 2016-2020. This shows that the platform started becoming popular from 2016 with increase in internet usage worldwide.

![image](https://github.com/user-attachments/assets/ad340a6e-e2bf-4b10-9dd3-37c880813b6c)

c) Month wise trend of Movies / TV Shows being added has been analysed using line plot which shows that most of the content is being added in the months of January, July and December.

![image](https://github.com/user-attachments/assets/fd426b44-a2e1-4f7e-b1b6-aa9fa5ebb489)

d) Top 5 countries based on No.of Movies/TV Shows produced has been analysed using bar plot indicating that United States(41.73 %) tops the chart followed by India(9.66 %), UK(7.42 %), Canada(4.11 %) and France(3.63 %).

![image](https://github.com/user-attachments/assets/00c903a9-1fc7-4ec9-b881-205c536426e1)

![image](https://github.com/user-attachments/assets/84ec4ad5-8a24-43d3-b26c-506cd30b4af8)

e) Genre wise content made by actors and directors has been analysed using dodged countplot which shows that actors and directors are more interested in making International Movies/TV Shows, Dramas and Comedies.

![image](https://github.com/user-attachments/assets/2e147ec8-9461-420a-9067-009dcf12bfff)

d) Correlation between the variables “Genre” and “Rating” has been analysed using heatmap plot and found that most popular genres are rated TV-MA, TV-14 and R which are intended for mature audience and are to be watched under strong parental guidance.

![image](https://github.com/user-attachments/assets/b55a9183-b138-428e-b2c7-e25ab0b89b8d)

e) To analyse the distribution of “duration” of the Movies and TV Shows boxplot has been used and 5 point estimates for Movie and TV Show are as under :

**For Movie :**
i) Minimum Duration , excluding outlier is around 50 min

ii) Maximum Duration, excluding outlier is around 160 min

iii) 25th Quantile : around 90 min

iv) Median : 105 min

v) 75th Quantile : around 120 min

**For TV Shows :**
i) Minimum Duration and 25th Quantile, excluding outlier is 1 Season

ii) Maximum Duration , excluding outlier is 3 Season

iii) Median and 75th Quantile : 2 Seasons

![image](https://github.com/user-attachments/assets/b436bfd7-5322-4716-b1f1-c9ca5c815a9a) ![image](https://github.com/user-attachments/assets/a70bad4f-05ff-4beb-a344-2a9ee7baa0f7)

**4. Recommendations**

a) As 70 % of the content type includes Movies and 30 % is of TV Shows, OTT Platform should also start focussing on TV Shows more considering  the increasing interest towards TV Shows among Millennials and Gen Z.

b) As per the histogram it is evident that content addition to the platform was peaked in 2019 and is showing a declining trend in past 2 years. Improved focus towards new content addition is required considering the competition from other platforms.

c) Month wise addition of content has been analysed using line plot which indicates that the new content addition has peaked every three months i.e., Jan, July and December. By combining the mentioned insight along with bar plot showing Top 5 countries in terms of Movies/TV Shows produced it is recommended to explore the holiday period of India i.e, starting from Aug to Nov as it is in 2nd Place in the list of Top 5 countries.

d) As per the non graphical analysis made on actors and directors it is observed that :

Out of 36436 actors less than 1 % of the actors constitutes for 60.0 % of total Movies or TV Shows
Out of 4527 directors less than 10 % of the directors constitutes for 51.0 % of total Movies or TV Shows

And hence it is recommended to check the interesting and good quality content that is being made by other actors and directors too which helps in improving the subscription rate.

e) By combining dodged countplot and heatmap it is evident that International Movies/Shows, Dramas genre dominates the content which are with rating TV-MA, TV-14 and R targeting only matured audience. It is recommended to increase focus on Reginal Movies/Shows which are being produced in India, UK, Canada and France too. As other similar platforms are attracting Kids and Children ad the content related to them is also to be produced to improve the subscribers base.

f) As per boxplot the median duration for Movies is 105 min and TV shows is 2 Seasons. It could be increased to 150 min for Movies and 4 Seasons for TV Shows which may improve the intention to continuous subscription as time required for completion of TV Shows or Movies increases.

**Dataset Used**

The datasets used include:

1. ott_dataset.csv

**Tools and Technologies used**

The tools used in this project include:

**Python** - This was needed to conduct Data Quality Assessment and also for Data Cleaning processes. With Python libraries **pandas, matplotlib, seaborn** exploratory data analysis of the datasets and to gain useful insights from the data was possible.

**Built With**

Python 3.10.12

**Authors**

J Siva Teja













