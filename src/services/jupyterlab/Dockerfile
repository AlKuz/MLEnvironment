FROM jupyter/tensorflow-notebook

RUN pip install mlflow missingno
RUN jupyter labextension install -y \
    @jupyter-widgets/jupyterlab-manager jupyter-leaflet \
    @lckr/jupyterlab_variableinspector \
    @oriolmirosa/jupyterlab_materialdarker \
    && jupyter lab build \

WORKDIR /home/jovyan/work

CMD jupyter lab \
    --ip=0.0.0.0 \
    --port=8888 \
    --allow-root
