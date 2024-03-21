- docker run <image-name>:tag ex : docker run ubuntu:latest
- docker ps (for all running container)
- docker run -it ubuntu /bin/bash
- docker ps -a (for all container running)
- docker stop <container-name or ID>
- docker rm <container-name or ID> ex : docker rm 1234 3456 -> remove
   multiple container in single command
- docker run -d ubuntu:latest --name mydocker (for detach mode)
- docker images (for docker image)
- docker rmi <image name> (for remove image)
- docker pull ubuntu (pull the image for future run container)
- docker exec <cotainer-name or ID> cat /etc/*release* (for execute command in running container)

 - to check version of OS - cat /etc/*release*

------------- Advance command --------------

-> Port mapping
- docker run -d -p 80:80 nginx

-> Volume mapping
- docker run -v /opt/datadir:/var/lib/mysql mysql (store data in outside container)

-> docker inspect <container-name or ID>
- inspect the container and get all details of container in JSON format

-> Container logs
- docker logs <container-name or ID>

-> build image & Run
- docker build . -t kundankukadiya/my-simple-app (from DockerFile)
- docker run kundankukadiya/my-simple-app

-> push on docker hub
- docker login
- use docker username and token for login
- docker push kundankukadiya/my-simple-app

--- CMD && ENTRYPOINT
- CMD is the default set of arguments that are supplied to the ENTRYPOINT process
- CMD command param1 --> CMD sleep 5
- CMD ["command","param1"] --> CMD ["sleep","5"]

- ENTRYPOINT - sets the process that’s executed when your container starts
- ENTRYPOINT is the process that’s executed inside the container
- ENTRYPOINT ["sleep"]
