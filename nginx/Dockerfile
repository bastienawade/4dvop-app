FROM ubuntu:latest
RUN apt update -y && apt install nginx -y && apt install git -y
RUN rm /var/www/html/*
WORKDIR /var/www/html
RUN git clone https://github.com/diranetafen/static-website-example.git .
RUN sed -i 's/80 default_server/8080 default_server/g' /etc/nginx/sites-enabled/default
EXPOSE 8080
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
