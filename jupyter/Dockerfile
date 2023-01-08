FROM jupyter/scipy-notebook

USER root

RUN apt-get update
RUN apt-get install -y libpq-dev python3-dev gcc

# Install OpenJDK-11
RUN apt-get update && \
    apt-get install -y openjdk-11-jre-headless && \
    apt-get clean

# Fix certificate issues
RUN apt-get update && \
    apt-get install ca-certificates-java && \
    apt-get clean && \
    update-ca-certificates -f

COPY ./requirements.txt .
RUN pip install -r requirements.txt