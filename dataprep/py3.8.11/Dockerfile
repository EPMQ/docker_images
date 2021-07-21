ARG BASE_IMAGE_TAG=3.8.11
FROM python:$BASE_IMAGE_TAG
# FROM kubeflownotebooks/jupyter:v0.2.92

# RUN pip3 install --upgrade pip && \
#     # XXX: Install enum34==1.1.8 because other versions lead to errors during
#     #  KFP installation
#     pip3 install --upgrade "enum34==1.1.8" && \
#     pip3 install --upgrade "jupyterlab>=2.0.0,<3.0.0" && \
#     pip3 install --upgrade kubeflow-kale && \
#     jupyter labextension install kubeflow-kale-labextension

# install - requirements.txt
COPY requirements.txt /tmp/requirements.txt
RUN python3 -m pip install -r /tmp/requirements.txt --quiet --no-cache-dir \
    && rm -f /tmp/requirements.txt