# compmodels/cull

Docker image for culling idle notebook servers. Requires a token from JupyterHub, e.g.

    export token=$(jupyterhub token -f /path/to/jupyterhub_config.py jhamrick)
    docker run -e "JPY_ADMIN_TOKEN=$token" compmodels/cull --timeout=86400 --cull_every=3600 --url=http://[jupyterhub_ip]:8081/hub