
groupby() lets you split your data into groups and then perform operations on each group separately.

Basic Example:


```
import pandas as pd

df = pd.DataFrame({
    'Name': ['Alice', 'Bob', 'Alice', 'Bob', 'Alice'],
    'Subject': ['Math', 'Math', 'English', 'English', 'Science'],
    'Score': [85, 78, 92, 88, 90]
})
```

`df.groupby('Name')['Score'].mean()`

Result:
```
Name
Alice    89.0
Bob      83.0
```






lost? ~ [[Index - Data Engineering]]