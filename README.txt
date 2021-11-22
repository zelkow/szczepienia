Ploting current vaccination rates in Poland

# Data sources
Data are taken from open data portal
https://dane.gov.pl/en/dataset/2476,odsetek-osob-zaszczepionych-przeciwko-covid19-w-gm

# Date : 2021-11-11
https://dane.gov.pl/en/dataset?categories%5Bid%5D%5Bterms%5D=147

# Python is started using Jupyter notebook

# Jupiter notebook is settup using local container based on jupyter/datascience-notebook

https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html

# this download and run the container :

docker run -e CHOWN_HOME=yes -e CHOWN_HOME_OPTS='-R'  --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v $HOME/git/szczepienia:/home/jovyan jupyter/tensorflow-notebook

# Data

The cvs file is downloaded to ./data repo and loaded to a dataframe

