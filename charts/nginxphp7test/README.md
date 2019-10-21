# Nginx & Php7.x-FPM Odiseasoft


## TL;DR; Full default Config. for edit:
```
php.repository = "chialab/php"
php.tag = "7.2-fpm"
php.pullPolicy = IfNotPresent
php.requests.cpu = "100m"
php.requests.memory = "64Mi"
php.limits.cpu = "125m"
php.limits.memory = "128Mi"

nginx.repository = "nginx"
nginx.tag = "1.14.2"
nginx.pullPolicy = IfNotPresent
nginx.requests.cpu = "100m"
nginx.requests.memory = "64Mi"
nginx.limits.cpu = "125m"
nginx.limits.memory = "128Mi"

persistence.enabled = true
persistence.keep = true
persistence.size = 1Gi
persistence.mountPath = /var/www/html/storage/app

service.HTTPPort = 80

ingress.enabled = true
ingress.domain = "test.stdhosting.com"
ingress.ssl = false

repo.server = 190.124.168.41
repo.path = /mnt/global-02/test
repo.zip = benchmark.zip
repo.root = /var/www/html
repo.laravel = false

replicaCount = 1
```

## Laravel Default Config with SSL
```
ingress.ssl = true
ingress.domain = cts-fiber.stdhosting.com
php.limits.cpu = 500m
php.limits.memory = 256Mi
php.requests.cpu = 500m
php.requests.memory = 256Mi
repo.zip = cts.zip
repo.root = /var/www/html/public
repo.laravel = true
```
