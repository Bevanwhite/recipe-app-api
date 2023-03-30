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
