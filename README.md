# byceps-nginx
byceps with nginx in a docker

**note:** this is a sample repository


## First install
First start the PostgreSQL only to initialize the database `docker-compose up -d byceps-db`.

Then `docker-compose run --rm byceps-app-admin bash` to enter go inside the admin container.

Execute `byceps initialize-database` and `byceps create-superuser` inside the container from previous step.

At last you can use `docker-compose up -d` to run the byceps with database and nginx in front.