# Docker
```bash
docker run -it <image_name>
# Running an image multiple times
docker run -it --name="<new_name>" <image_name>
# Running an image parallely
# To know the container if
docker ps
docker exec -it <container_id> /bin/bash
```
## References
1. https://www.digitalocean.com/community/questions/how-to-run-multiple-containers-of-the-same-image-and-expose-different-ports
2. https://www.makeuseof.com/run-ubuntu-as-docker-container/
