An uncleaned moves dataset is cleaned and the numerics are correlated in this project using Python programming language.

## Tools/libraries Used

Tool | Purpose 
--- | --- 
.csv | Raw movies data comes in .csv file 
jupyter notebook | To develop python scripts in an interactive way
Pandas | pandas functions are used for cleansing data in the Data Frame 
Numpy | np.mean() function is used to calculate the % of null values in the columns
Seaborn | To plot the graphical display of the correlations
Matplotlib | To plot the graphical display of the correlations

## Process
![alt text](https://github.com/smvishnu/Movies-Data-Correlation-Python-Project/blob/main/movies_data_corr1.png "Movies data correlation")

1. Read the dataset from 'movies.csv' file using pandas.read_csv() method. The method retuns an pandas DataFrame with all the values read from csv.
2. DATA CLEANING - Check for any missing data (or null or empty data) in each column and calculate the mean of the empty values. In case a column is completely empty then the result will be 1.0% and that column can be ignored in the further processes. Mean values are calculated using numpy.mean() method
3. DATA CLEANING - Since the dataset is quite big (there are 7669 rows), I am not considering rows with any Null values. Hence, removing the rows with Null values using Pandas dropna() method.
4. DATA CLEANING - Some of the values in column 'Year' is not matching with values 'Released' column. Creating a new column 'CorrectYear' with values parsed from 'Released'. The 'CorrectYear' values with have 100% match with 'Released' values
5. DATA CLEANING - Drop any duplicates in the 'Company' column
6. CORRELATION - Scatter plot for Budget vs Gross
7. CORRELATION - Display seaborn plot for Budget vs Gross
8. CORRELATION - Display correlation for numeric values in a matrix structure
