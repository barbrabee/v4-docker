# Dev

To develop Chevereto it will require to install Chevereto source.

* chevereto-source [v3](https://github.com/chevereto/v3)

## docker-compose

Compose file: [httpd-php-dev.yml](docker-compose/httpd-php-dev.yml)

* `SOURCE` is the absolute path to the chevereto source project.

```sh
SOURCE=~/git/chevereto/v3 \
docker-compose \
    -p chevereto-v3-dev \
    -f docker-compose/httpd-php-dev.yml \
    up
```

[localhost:8930](http://localhost:8930)

* Clear volumes

```sh
SOURCE=~/git/chevereto/v3 \
docker-compose \
    -p chevereto-v3-dev \
    -f docker-compose/httpd-php-dev.yml \
    down --volumes
```

## Sync with application code

Run this command from the Docker host:

```sh
docker exec -it chevereto-v3-dev_bootstrap \
    bash /var/www/sync.sh
```

> TIP: press up arrow key to call the command again.

## Composer

Use `composer` to manage dependencies.

```sh
docker exec -it --user www-data chevereto-v3-dev_bootstrap \
    composer install
```

```sh
docker exec -it --user www-data chevereto-v3-dev_bootstrap \
    composer update
```
