

| Feature     | pivot()                  | pivot_table()         |
| ----------- | ------------------------ | --------------------- |
| Duplicates  | NO!                      | Handled               |
| Aggregation | None                     | Yes                   |
| Speed       | Faster                   | Slower                |
| Use case    | 1-1 Mapping (clean data) | Real World Messy data |


```
df.pivot_table(index='Date', columns='Person', values='Mood', aggfunc=['mean', 'max', 'count'])
```









lost? ~ [[Index - Data Engineering]]