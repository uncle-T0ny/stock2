[tags]: <> (sql, column description)
*Select all columns description by type*
```sql
select * from information_schema.columns
where table_schema = 'exchange-local' and DATA_TYPE = 'bigint'
```
[tags-end]: <>

[tags]: <> (sql, like)
*Select all columns description by type*
```sql
select TABLE_NAME, COLUMN_NAME  from information_schema.columns
    where table_schema = 'exchange-local' and COLUMN_NAME like '%country%'
```
[tags-end]: <>