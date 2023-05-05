1. user API
    * user registration
    * creating auth token
    * viewing/updating profile

2. endpoints
    * `user/create/`
        * `POST` - register a new user
    * `user/token/`
        * `POST` - create new token
    * `user/me/`
        * `PUT/PATCH` - update profile
        * `GET` - view profile

3. how to create a user startapp
    * `docker-compose run --rm app sh -c "python manage.py startapp user"`