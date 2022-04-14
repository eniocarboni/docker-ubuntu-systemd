# Ubuntu 20.04 LTS Docker Image with systemd

Ubuntu 20.04 LTS Docker container with systemd, useful for tests with `ansible` especially with `molecule`

## Tags

  - `20.04`, `focal` `latest`


## How to Build

  * Verify if [Docker is installed](https://docs.docker.com/install/).
  * Run `docker build -t docker-ubuntu-systemd:20.04 -t docker-ubuntu-systemd:latest .`
  * Verify image: `docker images`

## How to Use

  * `docker pull eniocarboni/docker-ubuntu-systemd:latest` (or use the image you built earlier).
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro eniocarboni/docker-ubuntu-systemd:latest`

View the run container with

  * `docker ps`

Enter in the container with:

  * `docker exec -it <container_id> bash`

Kill container with:

  * `docker kill <container_id>`

Remove container with:

  * `docker image rm -f <container_id>` 

## Author

Created in 2022 by Enio Carboni

## License

GNU GENERAL PUBLIC LICENSE (see [LICENSE](LICENSE) file)
