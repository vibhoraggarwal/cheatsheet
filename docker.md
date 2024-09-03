# Docker
```bash
docker run -it <image_name>
# Running an image multiple times
docker run -it -w /app -v $PWD:/app --name="<new_name>" <image_name>
# Running an image with bin bash
docker run -it -w /app -v $PWD:/app <image_name> /bin/bash
# Running an image parallely
# To know the container if
docker ps
docker exec -it <container_id> /bin/bash
# Saving and sharing an image
docker save -o <path for created tar file> <image name>
docker load -i <path to docker image tar file>
```
## Build a new docker image
### Interactive method
```bash
docker commit -m "<commit message>" <container-id> <repository-path>:<tag>
docker push <repository-path>:<tag>
```

## Removing the unnessary docker images
```bash
docker rm $(docker ps -a -q)
docker rmi $(docker images -a -q)
docker volume prune -f
docker network prune -f
docker system prune -a --volumes -f
```

### Dockerfile method
## References
1. https://www.digitalocean.com/community/questions/how-to-run-multiple-containers-of-the-same-image-and-expose-different-ports
2. https://www.makeuseof.com/run-ubuntu-as-docker-container/
3. https://stackoverflow.com/questions/24482822/how-to-share-my-docker-image-without-using-the-docker-hub
4. https://jfrog.com/devops-tools/article/understanding-and-building-docker-images/
