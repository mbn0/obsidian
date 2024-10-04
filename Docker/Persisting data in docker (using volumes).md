to make data persistent i will be using [this guide](https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-docker-container-configure?view=sql-server-ver16&pivots=cs1-bash#persist).

Use this command to create a volume:
```bash
docker volume create <Volume-name>
```

then when creating a container use the ```
```bash
-v <volume-name>:/var/opt/mssql \
```
 command in the creation(the backslash at the end is to write a newline).
for example:
```bash
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=youdummydontput ur password inside ur notes" \
   -p 1433:1433 --name sql1 --hostname sql1 \
   -v sqlvolume:/var/opt/mssql \
   -d \
   mcr.microsoft.com/mssql/server:2022-latest
```
To check if its mounted correctly use:
```bash
docker inspect <container>
```
