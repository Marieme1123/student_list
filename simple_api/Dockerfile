FROM python:3.13-slim

LABEL maintainer="marieme@example.com"

RUN apt update -y && apt install -y \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    gcc

COPY student_age.py /
COPY requirements.txt /

RUN pip3 install -r /requirements.txt

RUN mkdir /data
VOLUME /data

EXPOSE 5000

CMD [ "python3", "./student_age.py" ]
