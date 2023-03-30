1. what is github actions?
    * it is automation tool
    * similar to travis-Cl, GitLab Cl/CD, Jenkins
    * run jobs when code changes
    * automate tasks

2. what are the common use of github actions?
    * Deployment
    * Code linting
    * unit testing

3. git hub actions charges?
    * charge per mintues
    * 2000 free mintues

4. How we'll configure github actions
    * create a config file at `.github/workflows/checks.yml`
        * set trigger
        * add steps for running testing and linting
    * configure dockerhub auth   
        * docker hub
            * needed to pull base images
            * rate limits
                * anonymous: 100/6h
                * authenticated: 200/6h
        * github actions uses shared ip address
            * limit applied to all users
            * authenticate with docker hub
                * 200 pulls per 6h all to ourselves!
                * more than enough for most projects

5. how to authenticate with dockerhub?
    * register account on https://hub.docker.com/
    * use dosker login during our job
    * add secrects to github projects
    * secrects are encrypted
6. what does the checks.yml file do?
    * this is a github actions workflow file that defines a job named "test-lint" which runs on a push eventon any branch. the job runs on an job runs on an ubuntu 20.04 virtual machine and consists of for steps:
        1.  login to docker hub using the docker/login-action@v1 action.it uses the docker hub username and access token stored in github secrets.
        2. checkout the current repository code the actions/checkout@v2 action.
        3. run tests using the "docker-compose run" command to execute the "python manage.py test" command in a docker container
        4. run a linting tool using the "docker compose run" command to execute the "flake8" command in a docker container 
