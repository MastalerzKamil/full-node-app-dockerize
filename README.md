
## How to delete all exisitng containers/images in one comand

```bash
# delete all containers
docker rm -vf $(docker ps -a -q)

# delete all images
docker rmi -f $(docker images -a -q)
```