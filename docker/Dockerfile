FROM openresty/openresty

RUN apt-get update &&\
    apt-get install -y curl

COPY nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

CMD ["/usr/bin/openresty", "-g", "daemon off;"]
