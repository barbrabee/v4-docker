# Compose

Compose file: [httpd-php.yml](docker-compose/httpd-php.yml)

## Up

* `LICENSE` your [Chevereto license key](https://chevereto.com/pricing).

Run this command to spawn (start) Chevereto.

```sh
LICENSE=yourLicenseKey \
docker-compose \
    -p chevereto-v3 \
    -f docker-compose/httpd-php.yml \
    up
```

[localhost:8830](http://localhost:8830)

## Stop

Run this command to stop Chevereto.

```sh
docker-compose \
    -p chevereto-v3 \
    -f docker-compose/httpd-php.yml \
    stop
```

### Down (uninstall)

Run this command to down Chevereto (stop containers, remove networks and volumes created by it).

```sh
docker-compose \
    -p chevereto-v3 \
    -f docker-compose/httpd-php.yml \
    down --volumes
```
