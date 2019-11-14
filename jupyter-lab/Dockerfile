FROM continuumio/miniconda3:latest

COPY ./jupyter-lab/environment.yml /
RUN conda update -n base conda -y && conda env update --file environment.yml

COPY ./project/environment.yml /project/environment.yml
RUN conda update -n base conda -y && conda env update --file /project/environment.yml

WORKDIR /project

CMD [ "jupyter", "lab", "--ip=0.0.0.0", "--allow-root" ]