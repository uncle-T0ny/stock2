[tags]: <> (sql, mysql, column description)
*Select all columns description by type*
```sql
select * from information_schema.columns
where table_schema = 'exchange-local' and DATA_TYPE = 'bigint'
```
[tags-end]: <>


[tags]: <> (sql, mysql, like)
*Select all columns description by type 1*
```sql
select TABLE_NAME, COLUMN_NAME  from information_schema.columns
    where table_schema = 'exchange-local' and COLUMN_NAME like '%country%'
```
[tags-end]: <>


[tags]: <> (sql, mysql, drop column)
*Drop column by name*
```sql
alert table tableName drop column columnName, algorithm=INPLACE, lock=NONE;
```
[tags-end]: <>

