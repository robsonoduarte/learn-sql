## COMMON TABLE EXPRESSIONS (CTE)

A CTE (Common Table Expression) is a temporary result set that exists only during query execution. It makes complex queries more readable and organized.

#### SYNTAX
```sql
WITH cte_name AS (
    SELECT column1, column2
    FROM table
    WHERE condition
)
SELECT * FROM cte_name;
```

A recursive CTE references itself to work with hierarchical data (org charts, categories, trees).

#### SYNTAX
```sql
WITH RECURSIVE cte_name AS (
    -- ANCHOR MEMBER (executed once)
    SELECT columns
    FROM table
    WHERE initial_condition
    
    UNION ALL
    
    -- RECURSIVE MEMBER (repeats until condition fails)
    SELECT columns
    FROM table
    JOIN cte_name ON join_condition
    WHERE recursive_condition
)
SELECT * FROM cte_name;
```

#### Exemples:

 * [CTE](https://github.com/robsonoduarte/learn-sql/blob/aa99d568c7f277fa3be23945b960890576c6443c/cte/CTE.sql#L1-L64)
 * [CTE Recursiva](https://github.com/robsonoduarte/learn-sql/blob/aa99d568c7f277fa3be23945b960890576c6443c/cte/CTE.sql#L67-L152)


#### start the docker compose before to run the queries:
```
docker compose up
```


