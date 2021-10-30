# base image
FROM python:2.7

#maintainer
LABEL maintainer="Rohit Roy Chowdhury"

# copy files from the host to the container
COPY ./techtrends .

#WORKDIR location
WORKDIR /techtrends

#Installing requirements
RUN pip install -U pip wheel setuptools && pip install -r requirements.txt

#exposing in port 3111
EXPOSE 3111

#initializing database
RUN python init_db.py

#Executing at the container start
CMD ["python", "app.py"]
