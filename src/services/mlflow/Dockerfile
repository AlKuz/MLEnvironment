FROM python:3.11-slim-buster

ARG DOCKER_USER=mlflow
RUN addgroup -S $DOCKER_USER && adduser -S $DOCKER_USER -G $DOCKER_USER
USER $DOCKER_USER

RUN pip install mlflow psycopg2-binary
RUN mkdir -p /home/${DOCKER_USER}/artifacts

CMD mlflow server \
    --backend-store-uri "postgresql+psycopg2://${POSTGRES_USER}:${POSTGRES_PASSWORD}@db:5432/${POSTGRES_DB}" \
    --default-artifact-root /home/${DOCKER_USER}/artifacts \
    --host 0.0.0.0 \
    --port 5555
