#NOTES
#Exploring Docker [2] - Docker Compose With Node & MongoDB
# https://www.youtube.com/watch?v=hP77Rua1E0c&t=973s
Great posts about using Docker:
https://blog.codeship.com/category/docker-commands/
https://blog.codeship.com/using-docker-push-to-publish-images-to-dockerhub/



https://karlcode.owtelse.com/blog/2017/01/25/push-a-docker-image-to-personal-repository/


https://stackify.com/docker-build-a-beginners-guide-to-building-docker-images/


https://gist.github.com/bradtraversy/89fad226dc058a41b596d586022a9bd3

docker container run -d -p 8080:80 -v ${pwd}:/usr/share/nginx/html --name mynginx nginx

********
docker run -v ${pwd}:/app/ -w /app/ -i -t hashicorp/terraform:light --version

If you want to reference a variable (such as calling your pwd) to mount the local fs.. In powershell you'll want to use ${pwd} vs $(pwd).. I'm putting this out there just in case anyone else stumbles across this thread.

docker run -v ${pwd}:/app/ -w /app/ -i -t hashicorp/terraform:light --version



# Docker Node MongoDB Example

> Simple example of a dockerized Node/Mongo app

## Quick Start

```bash
# Run in Docker
docker-compose up
# use -d flag to run in background

# Tear down
docker-compose down

# To be able to edit files, add volume to compose file
volumes: ['./:/usr/src/app']

# To re-build
docker-compose build
```
