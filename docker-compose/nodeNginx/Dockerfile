FROM nginx:1.15-alpine

# 사용자 지정
USER root

#Nginx
#COPY ./sites-available /etc/nginx/sites-available
COPY ./data/nginx/config/sites-enabled /etc/nginx/sites-enabled
COPY ./data/nginx/config/nginx.conf /etc/nginx/nginx.conf


