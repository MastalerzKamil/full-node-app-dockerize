
## How to delete all exisitng containers/images in one comand

```bash
# delete all containers
docker rm -vf $(docker ps -a -q)

# delete all images
docker rmi -f $(docker images -a -q)

# docker-compose down wit removing containers and volumes
docker-compose down -v --rmi all --remove-orphans

# removing all exisiting volumes
docker volume rm $(docker volume ls -q -f 'dangling=true') 
```
