# Ubuntu 18.04 LTS Docker Image with systemd

[![Build](https://github.com/eniocarboni/docker-ubuntu-systemd/actions/workflows/build.yml/badge.svg?branch=18.04)](https://github.com/eniocarboni/docker-ubuntu-systemd/actions/workflows/build.yml) [![GPL License](https://img.shields.io/badge/license-GPL-blue.svg)](https://www.gnu.org/licenses/) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/EnioCarboni)

Ubuntu 18.04 LTS Docker container with systemd, useful for tests with `ansible` especially with `molecule`

## Tags

  - `20.04`, `focal` `latest` on main branch
  - `18.04`, `bionic` on 18.04 branch
  - `16.04`, `xenial` on 16.04 branch


## How to Build

  * Verify if [Docker is installed](https://docs.docker.com/install/).
  * Run on main branch: `docker build -t docker-ubuntu-systemd:20.04 -t docker-ubuntu-systemd:latest .`
  * Run on 18.04 branch: `docker build -t docker-ubuntu-systemd:18.04 -t docker-ubuntu-systemd:bionic .`
  * Run on 16.04 branch: `docker build -t docker-ubuntu-systemd:16.04 -t docker-ubuntu-systemd:xenial .`
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
