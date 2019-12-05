FROM python:3.6-alpine

RUN apk update
RUN apk add curl

COPY . /app

WORKDIR /app

COPY healthcheck.sh /healthcheck.sh

RUN pip install -r requirements.txt

#HEALTHCHECK --interval=5s --timeout=3s --retries=3 CMD ["/bin/sh", "-c", "/healthcheck.sh"]
HEALTHCHECK --interval=10s --timeout=3s --retries=3 CMD curl --fail http://localhost:5000/ || exit 1

CMD ["python", "app.py"]
