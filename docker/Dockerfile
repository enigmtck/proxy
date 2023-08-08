FROM alpine:3

SHELL ["/bin/ash", "-c"]

RUN apk update && apk add nginx

COPY docker/files/enigmatick.conf /etc/nginx/http.d/enigmatick.conf
COPY docker/files/nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /srv/enigmatick/public
RUN rm /etc/nginx/http.d/default.conf

CMD ["nginx"]
