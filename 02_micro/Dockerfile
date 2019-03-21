FROM alpine
LABEL author: Marisol Giraldo Cobo
LABEL email: marisol.giraldo@correo.icesi.edu.co

RUN apk add --no-cache bash python py2-pip \
	&& pip2 install --upgrade pip \
        && pip2 install flask

COPY app.py app.py

EXPOSE 8080
CMD ["/usr/bin/python", "app.py"]:
