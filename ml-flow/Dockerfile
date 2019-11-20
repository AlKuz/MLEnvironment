FROM continuumio/miniconda3:4.7.12

COPY ./environment.yml /
RUN conda update -n base conda -y && conda env update --file environment.yml

WORKDIR /ml-flow

CMD ["mlflow", "server", "--host", "0.0.0.0"]