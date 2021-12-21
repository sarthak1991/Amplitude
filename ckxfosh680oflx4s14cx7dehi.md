## Setup Postgres docker container quick!!

> Docker remains the quickest way of setting up a Postgres database server. Here's how to do so.

Sometimes, we just need to set up a postgres database server, and if you have docker - spinning up a container is always the quickest and cleanest way of setting up a Postgres server

For example, when you need to quickly setup a Express Rest API server using PostGres with Prisma, like I need to do today. Here's how you do it. 

```
docker run --rm --name postgres-db -p 5432:5433 -e POSTGRES_PASSWORD=mysecretpassword -d postgres:13-alpine
``` 
***Please Note:*** we're mapping port *5432* to *5433*. This is intentional and serves to drive understanding of how ports works. The explanation is below: 

- ```postgres-db``` is the name of the container you spin up. 
- ```5432``` is the default port at which postgres runs. You can, if you so wish, map your system's port to container's port. In this case, ```5433``` is the port at which you will find the server on your local machine. 
- ```mysecretpassword``` is the **password** to log in to the db server
- ```postgres```  is the **default user AND default Database**. It is not mentioned in the docker command posted above.
- ```postgres:13-alpine``` is the image we're pulling. 

Assuming everything runs without an error, you can connect to the server using the connection string in the following format: ```postgresql://default_user:password@localhost:5432/default_db?schema=public```

Therefore, your string becomes

```
postgresql://postgres:mysecretpassword@localhost:5433/postgres?schema=quotes
```

And that's it. 

If you'd like to know how to connect to this (or any) postgres server using Shell/Terminal, you can find it in an upcoming blog. 

