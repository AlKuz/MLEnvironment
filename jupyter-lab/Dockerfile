FROM continuumio/miniconda3:4.7.12

RUN conda install -y -c conda-forge jupyterlab \
    jupyterhub \
    jupyterlab-git \
    mlflow \
    ipyleaflet && \
    conda install -c creditx nbresuse

RUN jupyter labextension install -y \
    @jupyter-widgets/jupyterlab-manager jupyter-leaflet \
    @lckr/jupyterlab_variableinspector \
    @jupyterlab/toc \
    @oriolmirosa/jupyterlab_materialdarker \
    jupyterlab-drawio \
    && jupyter lab build

COPY ./environment.yml .
RUN conda env update --file environment.yml

WORKDIR /project

CMD jupyter lab \
    --ip=0.0.0.0 \
    --port=8888 \
    --allow-root