1. fatal: refusing to merge unrelated histories
    * `--allow-unrelated-histories` stackoverflow
2. what happen when you add README.md and readme.md 
    * these files will confuse VSCode so delete this file from the repository
    * in order to delete use `git rm --cached README.md`
    * push the commit to the origin to take effect.
3. `failed to solve with frontend dockerfile.v0: failed to read dockerfile: open /var/lib/docker/tmp/buildkit-mount1896257663/Dockerfile: no such file or directory`
    * mostly this happen if you make the file name 
    * `DockerFile`(this will not work),  `Dockerfile`(this will work)
4. `failed to compute cache key: "/app" not found: not found`
    * for this create folder in the working directory
5. `[ $DEV = "true"]` ?
    * `sh: flake8: not found` this will give you this error
    * `[ $DEV = "true" ]` have the space that will go away
6. `services.db Additional property enviorment is not allowed`
    * you have to change `enviorment` to `environment`
7. problem with docker compose
    * using `depends_on` ensures service starts but doesn't ensure application is running
    * solution for this?
        * make django "wait for db"
            * check for database availability
            * continue when database ready
        * create custom django management command
    * when is this an issue?
        * running docker-compose locally
        * running on deployed environment
        