# Pebble

[![CircleCI](https://circleci.com/gh/letsspeak/Pebble.svg?style=svg)](https://circleci.com/gh/letsspeak/Pebble)


## Docker

### Run in Docker and Build

1. `git clone https://github.com/letsspeak/Pebble.git && cd Pebble`
1. `docker build ./Docker/ci/` or `docker pull letsspeak/pebble-ci:latest`
1. `export CID=$(docker run -d -it -p 8080:8080 letsspeak/pebble-ci:latest bash)`
1. `docker cp . $CID:/var/pebble`
1. `docker exec $CID bash -c 'swift build -c release'`

### Start Server

1. `docker exec $CID ./.build/release/Run serve --hostname 0.0.0.0`
1. open `http://localhost:8080` on your web browser

### Stop Server

1. `docker exec $CID pkill -U root -x Run`

