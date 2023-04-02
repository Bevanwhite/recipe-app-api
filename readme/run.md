1. how to run the docker file
    * run `docker-compose up`
    * to cancel or close it press `ctrl+c`

2. before run git hub what you need to check
    * `docker compose run --rm app sh -c "flake8"`
    * `docker compose run --rm app sh -c "python manage.py test"`
    
3. how to remove docker file?
    1. `docker images -a`
    2. `docker images --filter "dangling=true"`
    3. `docker rmi $(docker images -f "dangling=true" -q)`
    4. `docker ps`
