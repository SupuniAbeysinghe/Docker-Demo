# syntax=docker/dockerfile:1
FROM python:3.10-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY python/requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
COPY python/app.py .
CMD ["flask", "run", "--debug"]


# FROM python

# WORKDIR /user/app/src

# COPY python/demo.py $WORKDIR
# CMD [ "python", "./demo.py"]




# FROM ubuntu

# RUN apt-get update
# RUN apt-get -y install nginx


# COPY html /var/

# CMD [ "echo", "Hello"]