# docker-frontend-repo
It's frontend code repo with docker file.

When you commit anything in repo then action is not triggering automically. We will triger it manual.
In this action file, there are following actions.
 1. It will pick the latest tag from tag.txt file. 
 2. Create new tag of docker image and push in docker hub. 
 3. Increment the tag version of tag file of repo.

At final, we will modify tag version in the docker-compose file of backend repo (https://github.com/kdsmika/docker-backend-repo) with lastest docker images of front end application. 
It's useful to pull the latest docker images from docker hub and deploy into docker server.
