# Docker Typesafe Activator
Docker image which provides a typesafe activator 1.3.2, designed to launch play applications.

## Image inheritance
This docker image inherits from the [dalekurt/java7](https://registry.hub.docker.com/u/dalekurt/java7/)

## Usage

Your play app has to be mounted in the container in the '/opt/app' directory. Should you want to publish your app port to the host, you must use the -p argument.
Here is an example of a docker run command:
```
docker run -d \
  -v /path/to/your/play/app:/opt/app:rw \
  -p 80:9000 \
  dalekurt/activator
```

