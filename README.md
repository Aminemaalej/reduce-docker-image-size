## Layer Optimization: Every Byte Counts

```
RUN apt-get update && apt-get install -y python3-pip python3-dev && \
    pip3 install numpy pandas && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
```

## Use Docker Buildkit

```
DOCKER_BUILDKIT=1 docker build -t myapp . 
```

## Always Run Containers as Non-Root Users

```
RUN adduser --disabled-password --gecos "" appuser
USER appuser
```

## Limit the network exposure of your container by restricting the ports and IP addresses

```
docker run -p 127.0.0.1:8080:8080 myimage 
```

## Regularly scan your Docker images for known vulnerabilities

```
docker scan your-image:tag
```

## Links
### Scratch Image

` https://hub.docker.com/_/scratch `

### Google Distroless Images

`https://github.com/GoogleContainerTools/distroless`

### Docker BuildKit

` https://docs.docker.com/build/buildkit/`

### Image Analysis Tools

`https://github.com/wagoodman/dive`

`https://github.com/slimtoolkit/slim`

`https://github.com/aquasecurity/trivy`




