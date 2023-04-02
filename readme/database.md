## using PostgreSQL

* Popular open source DB
* integrates well with django

* we will using docker compose to configuare our database.
    * defined with project(re-usable)
    * presistent  data using volumes
    * handles network configuration
    * environment variable configuration

1. how we setup this ?
    * set `depends_on` on `app` service to start `db` first
    * docker compose creates a network
    * the `app` service can use `db` hostname

2. how about volumes?
    * presistent data
    * maps directory in container to local machine