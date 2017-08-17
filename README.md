jupyter notebook with some extras..

For a good docker/kubernetes notebook, mount:

* /usr/local/sbin
* /home/jovyan/.ipython
* /home/jovyan/.jupyter
* /home/jovyan/work
* /opt/conda/envs
* /home/jovyan/.conda


A good `jupyter_notebook_config.py` for keeping it behind a secure reverse proxy is:

```
c.NotebookApp.default_url = '/tree'
c.NotebookApp.token = ''
c.FileContentsManager.root_dir = 'work'
```
