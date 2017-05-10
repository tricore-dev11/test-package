# Health Check

The health check package is designed to be an easy to ease base class
to allow you to easily add health checks to your project.

### Installation
Add the following in composer.json
```
"repositories": [
    ...
    { "type": "git", "url": "git@github.com/EcommElite/health-check.git"}
],
```

```
"require": {
    ...
    "ecommelite/health-check": "dev-master"
},
```

Add the HealthCheckServiceProvider to the providers array in config/app.php:
```php
EcommElite\HealthCheck\HealthCheckServiceProvider::class,
```
Register CheckHealthToken middleware in app/Http/Kernel.php:
```php
'CheckHealthToken' => \EcommElite\HealthCheck\Http\Middleware\CheckHealthToken::class,
```
