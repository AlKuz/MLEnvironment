ML Environment
==============

Description
-----------

There is DevOps environment for Data Science and Machine Learning. The aim is to make easier my life (or yours). It allows you to run the environment in a remote server and work in the browser.

Install
-------

1. [Install Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
2. [Install Docker-Compose](https://docs.docker.com/compose/install/)
3. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
4. `cd /path/what/you/want`
5. `git clone https://github.com/AlKuz/MLEnvironment.git`
6. `cd MLEnvironment`
7. `docker-compose up`
8. Use port 5000 for MLFlow and 8888 for Jupyter-Lab

Remarks
-------
MLFlow works only via [REST API](https://www.mlflow.org/docs/latest/rest-api.html) now becouse of conflicts in the libraries