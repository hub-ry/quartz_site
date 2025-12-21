
- pivots a level of MultiIndex in the rows to become a new level in columns, effectively reshaping the data to be wider. 

Example:

Alice and Bob log their mood every day. The columns are 



Date|Person|Mood
Dec17|Alice|80
Dec17|Bob|20
Dec18|Bob|40
Dec18|Alice|100

df.unstack()

Person|Alice|Bob
Date
Dec17| 75|82
Dec18|68|91
Dec19|79|85


It unstacks the innermost index.






lost? ~ [[Index - Data Engineering]]