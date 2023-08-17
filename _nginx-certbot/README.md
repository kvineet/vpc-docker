# Nginx with Let’s Encrypt on docker-compose

> Extented from `https://github.com/wmnnd/nginx-certbot.git` which is also accompanied by a [step-by-step guide on how to
set up nginx and Let’s Encrypt with Docker](https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71).

`init-letsencrypt.sh` fetches and ensures the renewal of a Let’s
Encrypt certificate for one or multiple domains in a docker-compose
setup with nginx.
This is useful when you need to set up nginx as a reverse proxy for an
application.

## Prerequisites
- [docker-compose](https://docs.docker.com/compose/install/#install-compose).

## Installation
1. Clone this repository: `git clone https://github.com/kvineet/vpc-certbot.git .`

2. Modify configuration:
- Add server declarations in `data/nginx/app.conf`
- Add email addresses to `init-letsencrypt.sh`

4. Run the init script:

        ./init-letsencrypt.sh

5. Run the server:

        docker-compose up
