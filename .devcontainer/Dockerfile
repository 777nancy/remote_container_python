FROM python:3.9-slim

COPY requirements.txt /tmp/requirements.txt

RUN apt-get update -y \
	&& apt-get upgrade -y \
	&& apt-get install -y git \
	&& apt-get autoremove -y \
	&& apt-get clean \
	&& rm -rf /usr/local/src/* \
	&& pip install --no-cache-dir -r /tmp/requirements.txt \
	&& rm -rf /tmp/requirements.txt