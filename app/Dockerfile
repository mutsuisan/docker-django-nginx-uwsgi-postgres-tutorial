FROM python:3.6.4
ENV PYTHONUNBUFFERED 1

RUN mkdir /docker_app
WORKDIR /docker_app
COPY . /docker_app

RUN pip install --upgrade pip
RUN pip install -r requirements.txt
# RUN pip install  -i  https://pypi.python.org/simple/  -r requirements.txt