# whatwedo base image - Postgres

In this image is a basic PostgreSQL database server installation available.

## Usage

```
docker run -p 5432:5432 -e PG_ROOT_PASSWORD=mysecretpassword whatwedo/postgres 
```

## Environment Variables

* `PG_ROOT_PASSWORD` This is the one environment variable that is required. This environment variable should be what you want to set the password for the root user to be. In the above example, it is being set to "mysecretpassword".
* `CONTAINER_TIMEZONE` - timezone which should be used, default: `Europe/Zurich` ([see Wikipedia](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones))

## Volumes

* /var/lib/postgresql
* /etc/firstboot

## Exposed Ports

* 5432

## Built

Because we are using several base images with recurring tasks in the Dockerfile, we are using a script to include commands. This script is available under [https://github.com/whatwedo/docker-base-images/blob/master/docker-builder.sh](https://github.com/whatwedo/docker-base-images/blob/master/docker-builder.sh)

## Bugs and Issues

If you have any problems with this image, feel free to open a new issue in our issue tracker [https://github.com/whatwedo/docker-base-images/issues](https://github.com/whatwedo/docker-base-images/issues)

## License

This image is licensed under the MIT License. The full license text is available under [https://github.com/whatwedo/docker-base-images/blob/master/LICENSE](https://github.com/whatwedo/docker-base-images/blob/master/LICENSE).

## Further information

There are a number of images we are using at [https://whatwedo.ch/](whatwedo). Feel free to use them. More information about the other images are available in [our Github repo](https://github.com/whatwedo/docker-base-images).