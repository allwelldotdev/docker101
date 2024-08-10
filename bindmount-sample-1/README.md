# Setting up Bind Mount for Docker Containers - Jekyll

In this exercise, I learned how to setup bind mounts on Docker containers connection/synchronizing a local directory on my machine to a directory in the Jekyll container served from Docker Hub [`bretfisher/jekyll-serve:latest`](https://hub.docker.com/r/bretfisher/jekyll-serve).

I used this command to run container and bind mount to container directory:
```bash
$ docker run -d --name jekyll-demo -p 80:4000 -v $(pwd):/site bretfisher/jekyll-serve:latest
# where $(pwd) resolved to my current working directory which was set
# to this folder 'bindmount-sample-1/'
```