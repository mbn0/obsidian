---
id: Starting With Building API's
aliases: []
tags: []
---


 senior suggested that i learn how to create API's since I am still doing nothing.
# Overview:
To learn how to create API's on dotnet, i will have to learn about REST, Postman(for testing), some network protocols, some [Docker](Docker/Starting|Starting), [[Using SQL Servers inside a docker container]] and about JSON Web Tokens ([JWT](https://jwt.io/introduction)). it is a heavy topic to tackle but i believe everything would be extremely beneficial.

# Resources that would be used
[Microsoft official documentation and tutorial ](https://dotnet.microsoft.com/en-us/apps/aspnet/apis)
[This YouTube tutorial](https://www.youtube.com/playlist?list=PL82C6-O4XrHfrGOCPmKmwTO7M0avXyQKc)
and sense SQL server is not supported on Ubuntu 24, we will use a [docker image ](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver16&tabs=cli&pivots=cs1-bash)for it
[Another YouTube tutorial](https://www.youtube.com/watch?v=AhAxLiGC7Pc)
To check for dependencies: [[API packages needed]]

# Starting

check [[Starting with dotnet|Starting with dotnet]] if you did not download dotnet yet. 
use `dotnet new webapi -n <name>` to open a new project.

not all API's need a database, it depends on the API we are building. in case of a need for a database, SQL servers from Microsoft is the go-to database, because of its compatibility with C# (fuck Microsoft).

use `dotnet watch run` to run the it, "watch" keyword includes the ability to watch over files meaning any updates in the code would immediately be updated in the browser.

# [[Architecture]] 

