FROM jupyter/scipy-notebook

USER root

RUN apt-get update
RUN apt-get install -y libpq-dev python3-dev gcc

COPY ./requirements.txt .
RUN pip install -r requirements.txt