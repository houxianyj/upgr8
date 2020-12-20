# upgr8
Simple Laravel v8.0, PHP v8.0, Composer v2.0 and xDebug v3.0 docker setup.

## Setup
#### #1
Add this script to your composer.json so your composer container will automatically install the packages.

```JSON
"scripts": {
    "docker-setup": [
        "composer self-update --stable",
        "composer check-platform-reqs",
        "composer diagnose",
        "composer clear-cache",
        "composer dump-autoload --optimize",
        "composer install --dev"
    ],
}
```

#### #2
Copy the environment file which suits your project type.

###### Custom
```
$ cp .env.generic .env
```

###### Laravel
```
$ cp .env.laravel .env
```

#### #3
Run this command to build your container.
```
$ docker-compose up --build
```

#### #4
Happy Coding!
