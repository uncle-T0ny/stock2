[tags]: <> (redis)
# Show all the keys
keys *

# get value by key
get "key"

# delete value by key
del key
[tags-end]: <>


[tags]: <> (docker, redis-cli)
# connect to the docker with redis cli
docker exec -it redis_container_name redis-cli

[tags-end]: <>


[tags]: <> (redis, redis-cli)
# remove all the entries in db
FLUSHDB

[tags-end]: <>

