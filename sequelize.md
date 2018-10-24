[tags]: <> (sequelize, create table from model definition)

```javascript
 up(queryInterface, DataTypes) {
    DataTypes.useCLS(nsHooked);
    const { sequelize } = queryInterface;

    const [ definition ] = BtcDeposits.definition();
    return sequelize.transaction(async () => queryInterface.createTable(TABLE_NAME, definition));
  }
```
  
[tags]: <>  
  
