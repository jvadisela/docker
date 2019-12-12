#FROM python:2.7-alpine
#RUN apk add --no-cache --upgrade bash
#RUN mkdir /app
#COPY requirements.txt /app/requirements.txt
#RUN cd /app && pip install -r requirements.txt
#COPY . /app
#CMD ["/bin/bash", "-c", "/app/healthcheck.sh"]
#CMD ["./app/healthcheck.sh"]

FROM python:2.7-alpine
RUN apk add --no-cache --upgrade bash
WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY . .
#CMD ["/bin/sh", "-c", "/app/healthcheck.sh"]
#CMD ["pwd"]
#CMD ls -l
CMD ["./healthcheck.sh"]

