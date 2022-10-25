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
# prueba de esfuerzo en el servidor
```
#docker run -d python-ddos
```
# instalamos Apache Benchmarck para stresar el servidor
```
apt install apache2-utils gnuplot
```
# lanzamos el contenedor
```
sudo docker run -it --memory="6m" --cpus="0.1" -p 80:80 nginx
```
# ponemos las stats
```
docker stats
```
# lanzamos la prueba de stress
-k Enable the HTTP KeepAlive feature
-n (Number) of requests
-c (Concurrency) Number of multiple requests to perform at a time
-t (Timelimit) Maximum number of seconds to spend
-r Don't exit on socket receive errors.
-H custom-header
```
ab -k -n100000000 -c1000 -t 1000 -r -H 'Accept-Encoding: gzip,deflate' http://localhost/
```
