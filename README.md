# Machine-Learning-Projects

#Pandas Data Frame
1.import pandas as pd
2. data = [[10, 18, 11], [13, 15, 8], [9, 20, 3]]
    df = pd.DataFrame(data)
3. df= pd.read_csv('file name')
4. df.info()- returns number of columns, column labels, column data types, memory usage, range index, and the number of cells in each column (non-null values).
5. df.shape- returns number of rows and columns of the df
6. df.values- returns values of the columns
7. df.columns- returns column names
8. df.index- returns index range, step
9. df.head()- returns top 5 rows
10. df.head(10)- returns top 10 rows
11. df.tail()- returns bottom 5 rows
12. df.column_name- returns a specific column
13. df.['column name']- for a column with space in its name, it is one dimensional representation
14. df.[['column name']]- two dimensional representation
15. df.column_name.head(6) - returns top 6 rows of a specific column
16. df[['column1', 'column2']] - returns multiple columns. two brackets because first one creates a list of columns, second bracket is for the data frame.
17. df['column1'].sort_values() - sorts the values of column1 in ascending order. ascending is default value.
18. default value check- shift+tab
19. df['column1'].sort_values(ascending=False) - sorts in descending order
20. df.sort_values('column1','column2') - multiple column sorting

#Statistical Analysis in Data Frame
1. df.describe() - If the DataFrame contains numerical data, the description contains these information for each column:

count - The number of not-empty values.
mean - The average (mean) value.
std - The standard deviation.
min - the minimum value.
25% - The 25% percentile*.
50% - The 50% percentile*.
75% - The 75% percentile*.
max - the maximum value.
*Percentile meaning: how many of the values are less than the given percentile.

#correlation
1. df.corr() - returns correlation values of the columns
2. import seaborn as sns
3. sns.heatmap(df.corr(), annot= True) - creating heat map with correlation values

#subsetting rows
1. getting the values of rows with some condition
2. df['column1'] > 50 - returns the rows of column1 that are greater than 50 as True or smaller than 50 as False
3. df[df['column1'] > 50] - returns the rows of column1 that are greater than 50 in value

#subsetting using string value conditions
1. df[df['column1'] == 'string value'] - returns columns1 values with 'string value' as value
2. df[(df['column1'] == 'value 1') | (df['column1'] == 'value 2')] - multiple condition

#subsetting using isin function
1. df['column1'].isin(['value 1', 'value 2']) - returns rows in True or False
2. df[def['column1'].isin(['value 1', 'value 2'])] - returns rows of column1 with value 1 and value 2

- df.column1.unique() - returns all the unique values in column1
- df.column1.replace([value1, value2],[newvalue1, newvalue2]) - replaces values
- new_df= df.drop('column1',axis=1) - deletes column1 from df. axis=1 when working with the column, axis=0 when working with rows.
- df = pd.concat([new_df, df], axis=1) - adds a new column to df
