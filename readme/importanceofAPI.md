01. why document?
    * everything needed to use the api
    * available endpoints(paths)
        * `/api/recipes`
    * supported methods
        * `GET`,`POST`, `PUT`, `PATCH`, `DELETE`
    * format of payloads (inputs)
        * parameters
        * post json format
    * format of responses (outputs)
        * Response json format
    * authentication process


02. options for documentation
    * Manual
        * word doc
        * markdown
    * automated
        * use metadata from code(comments)
        * generate documentation pages

03. docs in DRF
    * auto generate docs(with third party library)
        * drf-spectacular
    * generates schema
    * browsable web interface
        * make test requests
        * handle auth

04. how it works
    * generate "schema" file
    * prase schema into gui

05. OpenAPI Schema
    * standard for describing apis
    * popular in industry
    * support by most api documentation tools
    * uses popular formats: Yaml/Json

06. using a schema
    * download and run in local swagger instance
    * serve swagger with api

07. installing drf-spectacular?
    * `drf-spectacular>=0.15.1,<0.16`