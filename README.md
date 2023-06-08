# GCP_deploying_a_python_app_docker

#Cloud Computing projects #GCP #DOCKER

#DOCKERFILE
first specifying the baseimage from Dockerhub documentation

COPY
copying the file unto the location when creating the image

WORKDIR work directory

RUN installing python libraries needed to deploy the application

COPY copying from local directory to the dicrectory where the application files will be

ENTRYPOINT telling the DOCKER which instructions to use to deploy

CMD file responsible for the app

#requrements.txt
specifying the libraries needed for deployment

Zip the files the were locally created .zip to upload in the cloud shell

#GCP cloud shell

unzip app-en.zip

cd app

docker build -t app:1.0 .

docker container run --name app -p 5000:5000 app:1.0

docker container ls

docker conainer ls --all

CRT C

docker container start app

docker contsiner stop app

docker tag app.1.0 us.gcr.io/dotted-rookery-321921/app

docker image ls

docker push us.gcr.io/dotted-rookery-321921/app

#check container registry for the image you ve created
#deploy to Cloud Run from the container image registry
#fill in the configuration

#create

#cloud run
delete container
