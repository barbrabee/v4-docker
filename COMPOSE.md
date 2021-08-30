# Compose

Compose file: [httpd-php.yml](docker-compose/httpd-php.yml)

* `LICENSE` your [Chevereto license key](https://chevereto.com/pricing).

```sh
LICENSE=yourLicenseKey \
docker-compose \
    -p chevereto-v3 \
    -f docker-compose/httpd-php.yml \
    up
```

[localhost:8830](http://localhost:8830)
