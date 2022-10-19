# docker_ur5e

Docker of a development environment for Universal Robots UR5e.

## Requirements (tested)

- Ubuntu 20.04
  - RTX3080
    - NVIDIA Driver 460.91.03
  - docker 20.10.12
  - docker-compose 1.29.2
  - nvidia-docker2 2.8.0-1

## Installation

    $ git clone git@github.com:Osaka-University-Harada-Laboratory/docker_ur5e.git

## Usage
#### Host machine
    $ cd docker_ur5e
    $ docker-compose build
    $ docker-compose up
    $ xhost +
    $ docker exec -it ur5e_container bash

## Author / Contibutor

[Takuya Kiyokawa](https://takuya-ki.github.io/)

## License

This software is released under the MIT License, see [LICENSE](./LICENSE).
