FROM nginx
ENV AUTHOR=Docker

WORKDIR /usr/share/nginx/html
USER root
COPY Hello_docker.html /usr/share/nginx/html
RUN chown -R nginx:nginx /usr/share/nginx/html
RUN chmod 777 /usr/share/nginx/html/Hello_docker.html 

CMD cd /usr/share/nginx/html && sed -e s/Docker/"$AUTHOR"/ Hello_docker.html > index.html ; nginx -g 'daemon off;'
