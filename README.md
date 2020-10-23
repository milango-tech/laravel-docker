# Docker Compose environment for Laravel

This is a project that you can use in existing projects or new projects.

Download this repository's contents and add the files to the root of your Laravel project.

### Initial run

When running this for the first time in a project, start the environment with the following command:

```bash
$ docker-compose up --build -d
```

This will ensure the PHP Docker image to build and when completed, it will start the Docker environment.

### Start the environment

If you've already built the image, you can just type:

```bash
$ docker-compose up -d
```

### Stop the environment

To stop the environment, but keeping volume data, run the following:

```bash
$ docker-compose stop
```

### Removing the environment

To stop the environment and remove volume data (eg. for starting over):

```bash
$ docker-compose down -v
```

##Helping commands

There's been added to containers that can interact directly with the environment to utilize Composer and Artisan within the docker network.

Examples:

```bash
$ docker-compose run artisan migrate:refresh
$ docker-compose run artisan queue:work --once
$ docker-compose run composer require laravel/sanctum
$ docker-compose run composer dump
```



