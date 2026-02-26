# SQL WINDOWS FUNCTIONS 

In SQL,
window functions (also known as analytic functions) perform calculations across a set of rows related to the current row without "collapsing" them into a single summary row. 
While a standard GROUP BY reduces your output to one row per group, a window function keeps every individual row intact while adding a new column for the calculation. 

#### start the docker compose before to run the queries:
```
docker compose up
```

- [LAG](https://github.com/robsonoduarte/learn-sql/blob/main/window-functions/LAG.sql)
