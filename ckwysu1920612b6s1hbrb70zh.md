## Run Mysql docker container on Apple M1 macs.

Apple's M1 chip has a different architecture than Intel or AMD and as such, not all containers run on it smoothly. One such docker container is MySQL. If you try to create and run a docker container on M1 mac, the platform it looks for are ```linux/arm64/v8```
And you get the following error: ```docker: no matching manifest for linux/arm64/v8 in the manifest list entries.```

You can still run the docker container by explicitly stating the platform, such that your run command becomes 
```
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=admin --platform=linux/x86_64 -d mysql
```

And now your container should form and run smoothly. 

Caveats --> 
This is not an ideal approach. If you'd like me to discuss problems with this approach and ideal solutions, let me know and I'll write another blog about it. R