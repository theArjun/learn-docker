FROM ubuntu:latest

WORKDIR /tmp

ENV PORT=8000

RUN apt-get update
RUN apt-get install -y python3-pip
RUN apt-get install -y subversion

RUN pip3 install gunicorn django

RUN svn checkout https://github.com/thearjun/django-projects/trunk/weather-project .

CMD ["gunicorn", "weather.wsgi:application", "--bind", "0.0.0.0:8000"]

