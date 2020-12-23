# Nodejs Auth Server with Docker, Nginx and Certbot 

This is an example of my [nodejs jwt auth](https://github.com/wms2537/nodejs-jwt-auth) with SSL through [letsencrypt](https://letsencrypt.org).

# Usage
You have to set environment variables in the docker compose file as stated [here](https://github.com/wms2537/nodejs-jwt-auth#environment-variables). You can also set them in your machine.

Change the `example.org` in [init-letsencrypt.sh](init-letsencrypt.sh) and [data/nginx/app.conf](data/nginx/app.conf) to your domain. You need to configure the DNS of your domain to point to your server.
```sh
find ./ -type f -readable -writable -exec sed -i "s/auth.example.org/<your domain>/g" {} \;
```