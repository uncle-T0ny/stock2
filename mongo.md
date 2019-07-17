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
