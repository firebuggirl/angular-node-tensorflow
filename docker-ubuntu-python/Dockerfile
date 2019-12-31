FROM ubuntu

LABEL MAINTAINER="Juliette Tworsey"

RUN apt-get update

RUN apt-get install -y python

RUN apt-get install -y python-pip

RUN apt-get install -y vim

COPY . /app

WORKDIR /app

RUN pip install -r requirements.txt
RUN pip install tensorflowjs

ENTRYPOINT ["python"]

CMD ["app.py"]


# NOTE: this took awhile
# docker build -t python-ubuntu:v1 .

# docker run -d -p 5000:5000 python-ubuntu:v1


# Run w/ bind mount

# cd ./docker-ubuntu-python
# docker run -d -it --name python-ubuntu-container -p 5000:5000 --mount type=bind,source="$(pwd)",target=/app python-ubuntu:v1
