FROM continuumio/miniconda3:4.7.12

RUN conda install -c conda-forge mlflow \
    && conda install -c anaconda psycopg2 \
    && mkdir -p /mlflow/artifacts \
    && mkdir -p /mlflow/db

CMD mlflow server \
    --backend-store-uri /mlflow/db \
    --default-artifact-root /mlflow/artifacts/ \
    --host 0.0.0.0 \
    --port 5555
