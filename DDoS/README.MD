# RUN THE DOCKERFILE
```
#docker build . -t python-ddos
Sending build context to Docker daemon  3.072kB
Step 1/4 : FROM python:3
 ---> f05c8762fe15
Step 2/4 : WORKDIR /usr/src/app
 ---> Using cache
 ---> 7d6e7ad7c10a
Step 3/4 : COPY . .
 ---> 2e1a04123864
Step 4/4 : CMD [ "python", "./python-ddos.py" ]
 ---> Running in 9e41b669666d
Removing intermediate container 9e41b669666d
 ---> dbbf5fef11c2
Successfully built dbbf5fef11c2
Successfully tagged python-ddos:latest
```

```
#docker run -d python-ddos
```