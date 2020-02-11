# pull official base image
FROM python:3.8.0-alpine

# set working directory
WORKDIR /usr/src/app

# set environment varibles
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# add and install requirements
COPY ./requirements.txt .
RUN pip install --upgrade pip setuptools wheel &&\
    apk update && apk --no-cache add gcc make uwsgi libc-dev linux-headers &&\
    pip3 install -r requirements.txt

# add app
COPY . .

# run server
CMD make prod-test
