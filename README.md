# Blocky OCI

Container images of Blocky, fast and lightweight DNS proxy as ad-blocker.

## Goal

To provide a rootless image with no capabilities set.
For the block lists take a look at [AdGuard Home data container](https://gitlab.flakybit.net/fb/blocky/agh-data).

## Images

Images are based on distroless base images, use official binaries and published in [Quay](https://quay.io/repository/flakybitnet/blocky-server),
[GHCR](https://github.com/flakybitnet/blocky-oci/pkgs/container/blocky-server), [AWS](https://gallery.ecr.aws/flakybitnet/blocky/server) and [GitLab](https://gitlab.flakybit.net/fb/blocky/oci/container_registry) registries.

## Usage

Usage is not different from [the official images](https://0xerr0r.github.io/blocky/latest/installation/#run-with-docker). So, you can run the server by one of the commands:

```
$ docker run -v /path/to/config.yml:/app/config.yml -p 4000:4000 -p 1053:1053/udp quay.io/flakybitnet/blocky-server
$ docker run -v /path/to/config.yml:/app/config.yml -p 4000:4000 -p 1053:1053/udp ghcr.io/flakybitnet/blocky-server
$ docker run -v /path/to/config.yml:/app/config.yml -p 4000:4000 -p 1053:1053/udp public.ecr.aws/flakybitnet/blocky/server
$ docker run -v /path/to/config.yml:/app/config.yml -p 4000:4000 -p 1053:1053/udp registry.flakybit.net/fb/blocky/oci/server
```

## Source

Source code are available at [GitLab](https://gitlab.flakybit.net/fb/blocky/oci) and mirrored to [GitHub](https://github.com/flakybitnet/blocky-oci).
