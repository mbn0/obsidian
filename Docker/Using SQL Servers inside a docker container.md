
[Guide used.](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver16&tabs=cli&pivots=cs1-bash)
[how to make data in the container persistent](https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-docker-container-configure?view=sql-server-ver16&pivots=cs1-bash#persist)
Forgot how to use docker? [[Starting with docker]]

to enter the container's bash:
```
docker exec -it sql1 bash
```

to enter sqlcmd(may have some issues): 
```
/opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P 'YourStrong@Passw0rd'
```

try this(-C idk wtf it does but it worked for me):
```
/opt/mssql-tools18/bin/sqlcmd -S localhost -U sa -C
```
