gcloud project create prj-jupiter
export PROJECT_ID=prj-jupiter
gcloud config set project prj-jupiter
docker pull jupyter/datascience-notebook
gcloud auth configure-docker 
docker tag jupyter/datascience-notebook eu.gcr.io/prj-jupiter/jupyter:v1
docker push eu.gcr.io/prj-jupiter/jupyter:v1
docker ps

# local jupiter notebook server, with persistance on host
docker exec -it 8777339c165 jupyter notebook list
sudo docker run -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v /home/sdgo/git/jupiter/data:/home/jovyan/work  -d jupyter/datascience-notebook


docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes -v ""/home/sdgo/git/jupiter/data:/home/ jupyter/datascience-notebook:33add21fab64

