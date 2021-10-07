# Compose

Compose file: [httpd-php.yml](../httpd-php.yml)

## Up

* `YOUR_V3_LICENSE_KEY` your [Chevereto license](https://chevereto.com/panel/license) key.

Run this command to spawn (start) Chevereto.

```sh
LICENSE=YOUR_V3_LICENSE_KEY \
docker-compose \
    -p chevereto-v3 \
    -f httpd-php.yml \
    up --abort-on-container-exit
```

[localhost:8830](http://localhost:8830)

## Stop

Run this command to stop Chevereto.

```sh
docker-compose \
    -p chevereto-v3 \
    -f httpd-php.yml \
    stop
```

### Down (uninstall)

Run this command to down Chevereto (stop containers, remove networks and volumes created by it).

```sh
docker-compose \
    -p chevereto-v3 \
    -f httpd-php.yml \
    down --volumes
```
