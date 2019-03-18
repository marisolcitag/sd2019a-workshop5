FROM alpine
LABEL author: Marisol Giraldo
LABEL email: marisol.giraldo@correo.icesi.edu.co

RUN apk add --no-cache apache2 && \
    echo "ServerName 127.0.0.1" > /etc/apache2/conf.d/custom.conf && \
    mkdir -p /run/apache2 && \
    apk update && \
    apk add ca-certificates && \
    cd /var/www/localhost/htdocs && \
    wget -O icesi.html http://www.icesi.edu.co && \
    echo "<html><body><h1>Marisol Giraldo Cobo</h1></body></html>" > /var/www/localhost/htdocs/studente.html
EXPOSE 80

ENTRYPOINT ["/usr/sbin/httpd"]
CMD ["-D","FOREGROUND"]
