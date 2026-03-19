# SQL WINDOWS FUNCTIONS 

In SQL,
window functions (also known as analytic functions) perform calculations across a set of rows related to the current row without "collapsing" them into a single summary row. 
While a standard GROUP BY reduces your output to one row per group, a window function keeps every individual row intact while adding a new column for the calculation. 

Key Components: The OVER() Clause
Every window function requires an OVER() clause, which defines the "window" of data to look at. It has three main parts: 

 - PARTITION BY: Divides the rows into groups (similar to GROUP BY).
 - ORDER BY: Sorts rows within each group, which is essential for things like rankings or running totals.
 - ROWS/RANGE: (Optional) Defines a specific "frame" or subset of rows relative to the current row (e.g., "current row and the 2 preceding rows")

### Common Function Types:
- [LAG](https://github.com/robsonoduarte/learn-sql/blob/main/window-functions/LAG.sql) Gets a value from a previous row (great for calculating "change vs last month").
- [NTILE]()Divides data into N approximately equal groups and numbers each group. Useful for creating categorized rankings, such as performance quartiles or percentiles.


#### start the docker compose before to run the queries:
```
docker compose up
```


