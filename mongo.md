[tags]: <> (db, mongo, index)
# Recreate indexes
```
db.links.reIndex()
```
[tags-end]: <>

[tags]: <> (db, mongo, index)
# Create nested index
```
db.collection.links.createIndex({"payload.broadcast_id": 1}})
```
[tags-end]: <>


[tags]: <> (db, mongo, index)

# Create index with unique field
```
db.collection.links.createIndex({"broadcast_id": 1, {"unique": 1}}})
```
[tags-end]: <>

[tags]: <> (db, mongo, performance)

# Create index with unique field
```
// return a list of operations in progress that take more than 3 seconds to perform
db.currentOp({"secs_running": {$gte: 3}})

// get current operations
db.currentOp()

// kill operation
db.killOp(30318806)

// kill all current operation 
db.currentOp().inprog.forEach(function(cop){db.killOp(cop.opid)})

// get amount of current operations 
db.currentOp().inprog.length
```
[tags-end]: <>



