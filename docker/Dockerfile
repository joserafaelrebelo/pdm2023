FROM nvidia/cuda:11.8.0-devel-ubuntu22.04

RUN apt-get update && \
    apt-get install -y software-properties-common && \
    add-apt-repository -y ppa:deadsnakes/ppa && \
    apt-get update && \
    apt install -y python3.10 python3-pip git

RUN python3.10 -m pip install \
    kaggle transformers \
    datasets accelerate \
    torchinfo evaluate  \
    jupyterlab notebook

RUN git clone https://github.com/joserafaelrebelo/pdm2023.git

WORKDIR /pdm2023

CMD ["jupyter", "notebook", "--allow-root"]