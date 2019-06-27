[tags]: <> (linux)
# Get free/used memory of the container
```
df -h

or 

free -m
```
[tags-end]: <>


[tags]: <> (linux, text, find)
# Find text matches in all the files
```
grep -iRl "your-text-to-find" ./
```
[tags-end]: <>


[tags]: <> (linux, text, find)
# Show open ports
```
lsof -i -P -n | grep LISTEN
```
[tags-end]: <>


[tags]: <> (linux, nano, linenumber)
# Go to line number
```
Ctrl+w+t
```
[tags-end]: <>

[tags]: <> (ssh, scp, copy)
# Copy folder to remote server
```
scp -r * remoteuser@remoteserver:/remote/folder/
```
[tags-end]: <>
