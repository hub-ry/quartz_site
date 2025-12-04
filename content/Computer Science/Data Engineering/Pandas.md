
#### Pandas Essentials

- Pandas is a third party tool to work with tabular data. 
-  CSV, excel, JSON easily – XML is a little more difficult.

- Everything you do in [[Pandas]], you can do in python... though it would be more difficult.



	[Installing Pandas](https://pandas.pydata.org/docs/getting_started/install.html)
#### Structures in Pandas

- Series: A one dimensional data structure, similar to an array.
- DataFrame: A two dimensional data structure, like a table. 
- Panel: A three dimensional multi-indexed structure.

#### How to use Pandas

```
import pandas as pd

# construct a data frame from the existing structure

data = {'Asia': ['$43567', '$28945', '$36900', '$67890'],  
'Africa': ['$13459', '$12005', '$14589', '$57894'],  
'Americas': ['$40045', '$44589', '$52398', '$107890'],  
'Australia/Oceania': ['$27890', '$34569','$45690','$78930'],  
'Europe': ['$33569', '$45700', '$56890', '$66003']}

data_sales = pd.DataFrame(data)

```

##### Now if we want to Display this new DataFrame
```
print(data_sales) # prints the text
display(data_sales) # prettify it

```


##### Most of Data Engineering will be **reading** 

###### Reading from CSV example:

```
import pandas as pd

data_oscar = pd.read_csv("oscar_age_female.csv")

# print
data_oscar

# to set indexes
Index(['Index', 'Year', 'Age', 'Name', 'Movie'], dtype='object')
```

Data Frames: 

Access by Row, Column, Cell, Subset

	Accessing Data

	data_frame['Column_Name']  # is the most common way to access 

	if the column name is a single word you can also do:   data_frame.Name
	

##### Accessing data (head & tail method):

	.head(k) ~ returns the first k rows of a column

	data_frame.['Age'].head(5) ~ returns ages 0-4

	.tail(k) is the opposite

###### Slicing:

Slicing is similar (think python syntax for this.)

	print(data_file[3:15:4]) ~ from index 3 up to 14, counting by 4

###### loc and iloc

	They are very simple and useful, the best way to learn is just to see.

```
loc

dataframe.loc[<row index range>, <column names>]

so the first parameter can be a number, slice, list
the second can only be one more more of the Column Names

If you use slicing for rows, like 1:7:1, this is includes 7, so it returns 1-7

iloc

dataframe.iloc[<row index range>, <column index range>]

both can use number, slice, list. In a slice, 1:7:1 7 is NOT included
```


When you are 