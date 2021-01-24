[tags]: <> (linux, memory, free, usage)
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


[tags]: <> (ssh, scp, copy)
# Copy folder from remote server
```
scp -r remoteuser@remoteserver:/remote/folder/ /localfolder
```
[tags-end]: <>

[tags]: <> (linux, ports, lsof)
# Show open ports
```
lsof -i -P -n
```
[tags-end]: <>

[tags]: <> (linux, screen, session, process)
# start screen session 
```
screeen 
```

# out from session
```
Ctrl + A + Z
```


# show sessions
```
sudo screen -ls
```

# connect to the session 
```
screen -r session_name
```
[tags-end]: <>


[tags]: <> (linux, bash, loop, for)

```
#!/bin/bash

for ((i=1;i<=100;i++)); 
do 
   echo $i
done
```
[tags-end]: <>

[tags]: <> (linux, keygen, ssh, generate)
# Generate ssh key

```
ssh-keygen -t rsa -b 4096 -m PEM -C account.name@email.io
```
[tags-end]: <>

[tags]: <> (linux, chown, owner, permission)
# Change owner of specifyed folder

```
sudo chown -R $(whoami) folder
```
[tags-end]: <>


