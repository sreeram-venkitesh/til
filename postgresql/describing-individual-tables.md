The following command can be used from inside `psql` to describe a particular table

```
\d+ table_name
```

This can be used to get a list of the column names and their datatypes

---

If you need the same in the form of an SQL query, you can use the following snippet

```sql
SELECT
    column_name,
    data_type
FROM
    information_schema.columns
WHERE
    table_name = 'table_name';
```