FROM jupyterhub/jupyterhub:1.0

COPY jupyterhub_config.py /etc/jupyterhub

CMD jupyterhub -f /etc/jupyterhub/jupyterhub_config.py \
    --ip 0.0.0.0 \
    --port 8000
