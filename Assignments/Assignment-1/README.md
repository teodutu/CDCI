# Assignment 1: Google SLO-Generator 2.0.0 - Code Execution

Use the `Makefile` in the `container` folder to deploy the environment:
```
studetn@cdci container $ make run  # Connect to the container
[...]

root@... # cd root  # Navigate to the exploit location

root@... # ./run_exploit.sh  # Profit!
```

A detailed list of the rules in the `Makefile` is:

- `make build`: create a Docker image based on `ubuntu:latest` that has all the tools and scripts needed to run the exploit
- `make run`: start a container from the image created with `make build` and get a shell inside it
- `make stop` stop the container created with `make run`
- `make clean`: remove the container and its underlying image


## Docker Hub

This image is also available on [Docker Hub](https://hub.docker.com/repository/docker/teodordutu/slo-generator-2.0.0-exploit).
To pull and run it from there, use the following command:
```
studetn@cdci ~ $ docker run -it teodordutu/slo-generator-2.0.0-exploit:cve-2021-22557 /bin/bashc
```
