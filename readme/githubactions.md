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

