[tags]: <> (sql, column description)
*Select all columns description by type*
```sql
select * from information_schema.columns
where table_schema = 'exchange-local' and DATA_TYPE = 'bigint'
```
[tags-end]: <>
