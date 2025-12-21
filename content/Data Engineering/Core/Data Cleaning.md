
Handling Duplicates:

``duplicated()`` ~ method

by default, .duplicated() keeps the first piece of data in the series of duplicates. 

.duplicated() returns a boolean series. It essentially marks each row true or false whether or not it is a repeat. It returns **true** 

***removing duplicates:***

1. you could use:
	`df_employee.loc[df_employee.duplicated() == False]`

	since df_employee.duplicated() will return the list of repeats set as True, we want to just keep the list without repeats, so we set the index to be only the ones that == False.


***finding missing values:***

`df_grades.isnull().sum()`

This totals the number of cells that are NULL.
You can use it like:

`df_grades[df_grades.Test2.isnull()]`

This creates a new table with only columns with missing grades for Test2


***ForwardFill and BackFill:***

Sometimes we can replace empty entries with 0, but if our data is dependent on averages, 0 is a bad default value and will have a notable impact.

`df_weather.fillna(method='ffill')`

`df_weather.fillna(method='bfill')`


***Interpolate:***

If your data is generally related from one element to the next, use interpolate.

`df_weather.interpolate()`

df_weather.interpolate(method='time')


***Binning - Assigning Values to Bings***

`bins=[0,59,69,79,89,100,110]`
`letter_grades = ['F', 'D', 'C', 'B', 'A', 'A+']`
`df_final['Final Grade'] = pd.cut(df_final.Grade, bins, labels=letter_grades)`


***Remove Missing Data:***

`dropna()`




lost? ~ [[Index - Data Engineering]]