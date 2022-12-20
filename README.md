# byceps-nginx
byceps with nginx in a docker

**note:** this is a sample repository


## First install
Please first take a look in the `.env` file to configure your site and secret key.
The `SECRET_KEY` can be set in the `byceps-app/config/production.toml`.

In `byceps-nginx/byceps-admin.conf` and `byceps-nginx/byceps-site.conf` set your domain.

First start the PostgreSQL only to initialize the database `docker-compose up -d byceps-db`.

Then `docker-compose run --rm byceps-app-admin bash` to enter go inside the admin container.

Execute `byceps initialize-database` and `byceps create-superuser` inside the container from previous step.

At last you can use `docker-compose up -d` to run the byceps with database and nginx in front.