1. Features in recipe api
    * create
    * list
    * view detail
    * update
    * delete

2. ednpoints
    * `/recipes/`
        * `GET` - list all recipes
        * `POST` - create recipe
    * `/recipes/<recipe_id>/`
        * `GET` - view details of recipe
        * `PUT/PATCH` - update recipe
        * `DELETE` - delete recipe

3. what is a view?
    * handles a request made to a URL
    * Django uses functions
    * DRF uses classes
        * Reusable logic
        * override behaviour
    * DRF also supports decorators
    * `APIView` and `Viewwsets` = DRF base classes

4. APIView
    * focused around HTTP methods
    * class methods for HTTP methods
        * `GET, POST. PUT, PATCH, DELETE`
    * provide felxibility over urls and logic
    * useful for non CURD APIs
        * avoid for simple Create, Read, Update, Delete APIs
        * Bespoke logic(eg: auth, jobs, external apis)

5. Viewsets
    * focused around actions
        * retrieve, list, update, partial update, destory
    * Map to Django models
    * use rousters to generate URLs
    * greate for crud operations on models