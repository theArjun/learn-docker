FROM ubuntu:latest

WORKDIR /workspace


RUN apt-get update && apt-get install -y \
    git python3-pip

RUN git clone https://github.com/theArjun/python-codes 
RUN pip3 install pylint
RUN pylint python-codes