Hey guys going to create django-api using tutorial video 

Creating a recipe api

1. API Features:
* user authentication
* creating objects
* filtering & sorting objects
* uploading & viewing images

in this course you will be able to Build a API and Maintain that api as well.
by doing the upgrades

in this course we going to focus to bankend
* 19 API Endpoints - managing users, recipes, tags, ingredients
* user Authentication
* browseable admin interface( Django Admin)
* Browsable API (Swagger)

#### Technologies using 

* using python as the progaramming language
* using Django as the web Framework and handles 
    * url mappings 
    * object relational mapper
    * admin site
    * django rest framework (django-add-on) use for build rest api
* PostgreSQL - Database
* Docker 
    * docker for api 
    * docker for database
* GitHub Actions
    * Automation and linting

* django project structure
    * app/ - django project
    * app/core/ - code shared between multiple apps
    * app/user/ - user related code
    * app/recipe/ - recipe related code

#### Test driven development -TDD

* unit tests code which test the code that we have written.
    * Set up conditions / inputs
    * Runs a piece of code

* many benefits having unittest    
    * Ensures code runs as expected
    * catches bugs
    * imporves reliability
    * provides confidence

* what is TDD?
    * software development process relying on software requirements being converted 
    to test cases before software is fully developed.

* why use TDD?
    * Batter understanding of code
    * make changes with confidence
    * Reduce bugs

* why use Docker?
    * consistent dev and prod environment
    * easier collaboration
        * different version of Python
        * different version of database
        * different version of SDK
        * etc ...
    * capture all dependencies as code
        * python requirements
        * operating system dependencies
    * Easier cleanup

* how we'll use Docker
    * define dockerfile
    * create docker compose configuration
    * run all commands via docker compose

* docker on github actions
    * docker hub introduced rate limit
        * 100 pulls / 6hr for unauthent icated users
        * 200 pulls / 6hr for authenticated users
    * github actions is a shared service
        * 100 pulls / 6hr applied for all users
    * authenticate with docker hub
        * create account
        * setup credentials
        * login before running job
        * get 200 pulls / 6hr for free
