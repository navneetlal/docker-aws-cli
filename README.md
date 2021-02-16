# AWS CLI Version 2 + Docker CLI
This is a unified command line tool to interact with aws and docker build on alpine.

# Supported tags and respective `Dockerfile` links
- [1.0.1](https://raw.githubusercontent.com/navneetlal/docker-aws-cli/main/Dockerfile), [latest](https://raw.githubusercontent.com/navneetlal/docker-aws-cli/main/Dockerfile)
- [1.0.0](https://raw.githubusercontent.com/navneetlal/docker-aws-cli/main/Dockerfile)

# When you may want to use this image
## Need a easy way to interact with AWS
```bash
  $ docker run -it navneetlalg/docker-aws-cli sh
  $ aws --version
```
Alternatively, you can use your host configuration file directly.
```bash
  $ docker run --rm -it -v ${HOME}/.aws/credentials:/root/.aws/credentials navneetlalg/docker-aws-cli aws help
```
## Need a simple docker cli tool to interact with docker daemon
```bash
  $  docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock navneetlalg/docker-aws-cli docker ps
```
## Gitlab CI for Docker-in-Docker
Use this image when you want to build and publish docker image to [AWS ECR (Elastic Container Registry)]()

# Issues
In case of any problem, open an issue here at https://github.com/navneetlal/docker-aws-cli/issues/new

# License
Licensed under MIT