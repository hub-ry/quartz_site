Note: PANDAS MERGE IS ALWAYS SMART ABOUT MATCHING COLUMN NAMES

***Inner Joins*** - Default merge

`df_join=pd.merge(df_student, df_gpa)`

- In no columns to merge are specified, merge identifies columns with matching names. 

- Inner join preserves the order of the left keys.

***Left Joins + Right Joins:***

`df_join=pd.merge(df_student, df_gpa, how='left')`


`df_join=pd.merge(df_student, df_gpa, how='right')`

Creates one big data frame where it adds the columns of df_gpa either to the left or right of the columns of df_student. It uses index to do so.


***Outer Join:***

Keeps all parts of your data, fills in the rest with NaN, sort keys lexicographically.

`df_join=pd.merge(df_student, df_gpa, how='outer')`


sooo much documentation on merging... https://pandas.pydata.org/docs/reference/api/pandas.merge.html




lost? ~ [[Index - Data Engineering]]