FROM continuumio/miniconda3:4.7.12

RUN conda install -y -c conda-forge jupyterhub \
    jupyterlab \
    jupyterlab-git \
    mlflow
RUN jupyter labextension install -y @jupyterlab/hub-extension
RUN jupyter lab build

WORKDIR /project

CMD [ "jupyter", "lab", "--ip=0.0.0.0", "--allow-root" ]