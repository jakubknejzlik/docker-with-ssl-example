# docker-with-ssl-example

Example docker-compose configuration for running http service behind SSL using Let's Encrypt

# Installation

1. clone this repository
1. replace `example.com` to your domain in `default.conf` and `docker-compose.yml`
1. in case you want specific subdomain replace `www` to your subdomain in `default.conf` and `docker-compose.yml`
1. in case you don't want to generate certificate for root subdomain, update `ONLY_SUBDOMAINS=false` to `ONLY_SUBDOMAINS=true` (for example you don't have access to root domain DNS config)
1. update `app` service to your specific needs in `docker-compose.yml` (or add any other service)

# Running

Start server by running:

```
run `docker-compose up -d`
```

You can observe your app logs/stats by running:

```
// container stats
docker stats
// container logs
docker-compose logs -f
```
