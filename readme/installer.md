* installing specific django version in python to match to the project
* at last we will upgrade it to the latest version
* in requirements.txt contians all the python dependencies

what are we doing in the docker file?
* using alpine image it is light weight image
* maintainer how will be the maintainer or the website

what the code say in docker file?
* `ENV PYTHONUNBUFFERED 1` this is recommaned setting when you running python in docker container
* you can see log that will be get to the console to your terminal without any delay
* `COPY ./requirements.txt /tmp/requirements.txt` adding the requirements file to the docker image
* `COPY ./app /app` we copy the app directory to docker image
* `WORKDIR` is the working directory
* `EXPOSE 8000` this app is going to use the port 8000
* `RUN` what this command will do?
    * this will run a command on our alpine image when we are building are image.
    * we have create one run block using `&& \` this to break to new line.
    * we can use spearate run command then it will create layers in docker image
* why we need venv?
    * if there is conflicts on the code their will be error
    * `python -m venv`  create a docker vartual environment 
* why we remove `rm -rf /tmp` to make docker light weight as possible
* why adding a user ?
    * default user is the root user to aviod that we creating another user
    * because root user have every privilege then  it becomes a security issue.
    * `django-user` is the username of the alpine image
* `ENV PATH="/py/bin:$PATH"` in this we add python to path file in linux so it can run automatically
* `docker build .` will run the docker file