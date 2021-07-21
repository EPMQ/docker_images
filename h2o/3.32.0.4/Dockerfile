ARG BASE_IMAGE_TAG=3.8.11
FROM python:$BASE_IMAGE_TAG

# install - packages
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    default-jre \
    git-all

# install - requirements.txt
COPY requirements.txt /tmp/requirements.txt
RUN python3 -m pip install -r /tmp/requirements.txt --quiet --no-cache-dir \
    && rm -f /tmp/requirements.txt