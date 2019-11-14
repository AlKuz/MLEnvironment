FROM continuumio/miniconda3:latest

COPY ./environment.yml /
RUN conda update -n base conda -y && conda env update --file environment.yml

WORKDIR /ml-flow

CMD ["mlflow", "server", "--host", "0.0.0.0"]