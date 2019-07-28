# Docker PHP-FPM 7.3 & Composer 1.8.6 & Nginx 1.16 on Alpine Linux
PHP-FPM 7.3 & Composer 1.8.6 & Nginx 1.16 setup for Docker, build on [Alpine Linux](http://www.alpinelinux.org/).
The image is only +/- 50MB large.

Repository: https://github.com/ArthurPai/docker-php-nginx


* Built on the lightweight and secure Alpine Linux distribution
* Very small Docker image size (+/-50MB)
* Uses PHP 7.3 for better performance, lower cpu usage & memory footprint
* Optimized for 100 concurrent users
* Optimized to only use resources when there's traffic (by using PHP-FPM's ondemand PM)
* The logs of all the services are redirected to the output of the Docker container (visible with `docker logs -f <container name>`)
* Follows the KISS principle (Keep It Simple, Stupid) to make it easy to understand and adjust the image

[![Docker Pulls](https://img.shields.io/docker/pulls/arthurpai/alpine-nginx-php7.svg)](https://hub.docker.com/r/arthurpai/alpine-nginx-php7/)
[![Docker image layers](https://images.microbadger.com/badges/image/arthurpai/alpine-nginx-php7.svg)](https://microbadger.com/images/arthurpai/alpine-nginx-php7)
![nginx 1.16.1](https://img.shields.io/badge/nginx-1.16-brightgreen.svg)
![php 7.3](https://img.shields.io/badge/php-7.3-brightgreen.svg)
![Composer 1.8.6](https://img.shields.io/badge/composer-1.8.6-brightgreen.svg)
![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)

## Usage

Start the Docker container:

    docker run -p 80:80 arthurpai/alpine-nginx-php7

See the PHP info on http://localhost

Or mount your own code to be served by PHP-FPM & Nginx

    docker run -p 80:80 -v ~/my-codebase:/var/www/html arthurpai/alpine-nginx-php7
