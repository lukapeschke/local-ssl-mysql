# Local MySQL + SSL docker-compose deployment

## First set up

This will generate a few certs and keys. You just need to run it once.

```
docker-compose run mysql /gen_ssl.sh
```

Note: This is done in the MySQL container rahter than on the host to ensure OpenSSL version compatibilities, especially concerning
RSA key formats.

## Starting the service

```
docker-compose up -d
# MySQL takes ~10s to start
```

MySQL should now be available on port 3306
