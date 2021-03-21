**DEPRECATED** Please use https://hub.docker.com/r/hexpm/erlang instead.

# Erlang/OTP on Alpine Docker image

This repo provides a Dockerfile for building Alpine Docker image with Erlang/OTP installed.

The Dockerfile is almost an exact copy of the one at https://github.com/bitwalker/alpine-erlang:
all credits go to Paul Schoenfelder and contributors to that repo.

Docker images are hosted at [Dockerhub](https://hub.docker.com/r/arkgil/alpine-erlang).

## Why another Alpine-based Erlang Docker image?

This image was mainly created for running in CI services like [CircleCI](https://circleci.com),
which can use Docker images as a base for running tasks.

The difference between this and [bitwalker's](https://hub.docker.com/r/bitwalker/alpine-erlang) and
[offical](https://hub.docker.com/_/erlang) is the versioning scheme - see below for more information.

## Versioning

Docker image tags are exactly the same as versions of the OTP release they include. This means that
there is no image tagged `21`, but there is `21.0`. The intention here is that the user knows exactly
which version of Erlang/OTP they're using (if they care about this kind of stuff).

Dockerfile for each major OTP release is kept on its own branch (i.e. all versions from `20` release
line are kept on branch `20`) and particular versions are marked with git tags. Dockerfile for the
current release line is kept on `master`.

## License

MIT.
