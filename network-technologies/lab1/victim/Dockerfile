FROM alpine:latest

RUN apk add --no-cache nginx curl \
    && mkdir -p /run/nginx /usr/share/nginx/html \
    && printf '<h1>Victim server is alive</h1>\n' \
       > /usr/share/nginx/html/index.html

COPY nginx/default.conf /etc/nginx/http.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
