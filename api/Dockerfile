
FROM python:3.7

ENV PYTHONUNBUFFERED 1

RUN mkdir /app

WORKDIR /app

ADD . /app/

RUN pip install -r requirements.txt

EXPOSE 8000
