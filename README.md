# Privacy Sandbox Builders

Build tools and docker images used by the [Privacy Sandbox](https://github.com/privacysandbox)
open-source ecosystem.

## Building Docker Images

To build a docker image directly, you can use the `tools/get-builder-image-tagged` tool.

Alternatively, you can use `docker buildx build` to create the image using a
command like this:

```sh
tar --create --dereference --gzip --directory=images/build-debian . | \
  docker buildx build - --tag privacysandbox/builders/build-debian:latest`
```

