# RUN NGINX IN ONE LINE
```
#docker run -d -p 80:80 nginx
```
 
# FROM DOCKERFILE
```
#docker build .
Sending build context to Docker daemon  4.096kB
Step 1/3 : FROM nginx:latest
 ---> 5d58c024174d
Step 2/3 : RUN apt update -y && apt install vim -y
 ---> Using cache
 ---> e7be692f35f1
Step 3/3 : COPY ./index.html /usr/share/nginx/html
 ---> Using cache
 ---> 86daeef503ce
Successfully built 86daeef503ce
```
```
#docker images
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
<none>       <none>    86daeef503ce   25 hours ago   196MB
```

```
#docker run -d -p 80:80 [IMAGE ID]
```
