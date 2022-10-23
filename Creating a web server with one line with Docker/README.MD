#RUN NGINX IN ONE LINE
docker run -d -p 80:80 nginx
#FROM DOCKERFILE
docker build .
docker images
docker run -d -p 80:80 [image-id]