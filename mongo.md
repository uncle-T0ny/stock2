[tags]: <> (db, mongo, index)
# Recreate indexes
```
db.links.reIndex()
```
[tags-end]: <>

[tags]: <> (db, mongo, index)
# Create nested index
```
db.links.createIndex({"payload.broadcast_id": 1}})
```
[tags-end]: <>


[tags]: <> (db, mongo, index)

# Create index with unique field
```
db.conversions.createIndex({broadcastId: 1, reference: 1}, {background: true})
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

[tags]: <> (mongo, update)
# Update multiple items in collection by query(condition)
```
db.getCollection('links').update(
    // query 
    {
        batch: 'b83a291c-be95-4b0e-a0f0-05845648777b'
    },
    
    // update 
    {
        $set: {longLink: "http://track.mandrumfit.com/a6d01bce-e053-4a21-b3cc-fc985f2c5cbb"}
    },
    
    // options 
    {
        "multi" : true,  // update only one document 
        "upsert" : false  // insert a new document, if no existing document match the query 
    }
);
```
[tags-end]: <>

