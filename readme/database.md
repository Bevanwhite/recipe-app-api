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

3. steps for congfiguring database?
    1. configure django 
        * tell django how to connect
    2. install database adaptor dependencies 
        * install the tool django uses to connect
    3. update python requirements

4. what  django needs to know?
    * engine (type of database)
    * hostname (ip or domain name for database)
    * port
    * database name
    * username
    * password

5. how to use enviroment variables
    * pull config values from environment variables
    * easily passed to docker
    * used in local dev or prod
    * single place to config project
    * easy todo with python

6. what is Psycopg2?
    * most popular postgreSQL adaptor for python
    * supported by django

7. installation options
    1. psycopg2-binary
        * ok for development
        * not good for production
    2. psycopg2
        * compiles from source
        * required additional dependencies
        * easy to install with docker
    
8. installing psycopg2
    * list of package dependencies in docs
        * C complier
        * python3-dev
        * libpq-dev
    * equivalent packages for alpine
        * postgresql-client
        * build-base
        * postgresql-dev
        * musl-dev
    * found by searching and trial and error
    * docker best practice
        * clean up build dependencies

