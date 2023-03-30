1. what  is linting?
    * tool to check code formatting 
    * highlights errors, typos, formatting issues

2. how we'll handling linting 
    * install flake8 package
    * run through docker compose 
    * `docker-compose run --rm app sh -c "flake8"`

3. how to solve lining errors?
    * start from the bottom to up then you can see the error.

4. testing
    * django test suite
    * setup test per django app
    * run tests through docker compose
    * `docker-compose run --rm app  sh -c "python manage.py test"`

5. why you need `requirements.dev.txt`
    * to sperate development code from other users 
    * for other they do not want have flake8
6. `build: \n args: \n - DEV=true` why we put this command
    * it is to say to the dockerfile that we are running in developer mod
    * this command will be ture if only we are runing through docker-compose
7. `ARG DEV=false` what this does?
    * assing dev value as false;
8. `if [ $DEV = "true"]; \ \n then /py/bin/pip install -r /tmp/requirements.dev.txt ; \ \nfi && \` ?
    * this is saying if the  DEV equals to true run this command
    * DEV will be true only when you run with `docker-compose.yml` file only
    * all other times it runs false.


