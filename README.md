# bitlbee Dockerfile
This repository contains **Dockerfile** of [*bitlbee*](https://github.com/bitlbee/bitlbee), for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/mbologna/bitlbee/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

## Base Docker image

* buildpack-deps/jessie-curl

## Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/mbologna/docker-bitlbee/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull mbologna/docker-bitlbee`

   (alternatively, you can build an image from Dockerfile: `docker build -t="mbologna/docker-bitlbee" github.com/mbologna/docker-bitlbee`)

## Usage

### (optional and only for those who build the image) configure bitlbee

customize etc/bitlbee/bitlbee.conf to suit your needs

### run bitlbee

`docker run -d --name bitlbee -p 16667:6667 --restart=always mbologna/docker-bitlbee`

### run bitlbee with persistent config file (`username.xml`)

`docker run -d --name bitlbee -p 16667:6667 --restart=always -v <data-dir>:/var/lib/bitlbee mbologna/docker-bitlbee`

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
