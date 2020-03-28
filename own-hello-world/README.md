### Build Docker Image using Docker File


```shell
docker build .
```

We can also build the docker image specifying custom image name.
```shell
docker build . -t custom-name
```

Running the instance of the container.

```shell
docker run custom-name
```

Removing the container.

```shell
docker rm custom-name
```