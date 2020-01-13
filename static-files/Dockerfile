FROM nginx
ENV AUTHOR=Docker

WORKDIR /usr/share/nginx/html
USER root
COPY Hello_docker.html /usr/share/nginx/html
RUN chown -R nginx:nginx /usr/share/nginx/html
RUN cd /usr/share/nginx/html && sed -e s/Docker/"$AUTHOR"/ Hello_docker.html > index.html && chmod 777 index.html
CMD nginx -g 'daemon off;'
