# sinopia docker image

##Install image##
docker pull euprogramador/sinopia:latest

## Create container ##
docker run --name sinopia -d -p 4873:4873 euprogramador/sinopia:lastest

## External configuration ##

the image creates a directory at the root called /sinopia containing config.yaml and storage, to set up a production environment suggest turning this into mount volume points and fix version. Example:

docker run --name sinopia  --restart=always -p 4873:4873 -v /sinopia:/sinopia -dt euprogramador/sinopia:1.4.0

