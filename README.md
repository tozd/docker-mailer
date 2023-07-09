# tozd/mailer

<https://gitlab.com/tozd/docker/mailer>

Available as:

- [`tozd/mailer`](https://hub.docker.com/r/tozd/mailer)
- [`registry.gitlab.com/tozd/docker/mailer`](https://gitlab.com/tozd/docker/mailer/container_registry)

## Image inheritance

[`tozd/base`](https://gitlab.com/tozd/docker/base) ← [`tozd/dinit`](https://gitlab.com/tozd/docker/dinit) ← `tozd/mailer`

See also [`tozd/nginx-mailer`](https://gitlab.com/tozd/docker/nginx-mailer).

## Tags

- `ubuntu-trusty`: nullmailer 1.11
- `ubuntu-xenial`: nullmailer 1.13
- `ubuntu-bionic`: nullmailer 2.1
- `ubuntu-focal`: nullmailer 2.2
- `ubuntu-jammy`: nullmailer 2.2

## Volumes

- `/var/log/nullmailer`: Log files when `LOG_TO_STDOUT` is not set to `1`.
- `/var/spool/nullmailer`: Work files (e.g., queue). Persist this volume to not lose state.

## Variables

- `ADMINADDR`: If set, all e-mails to system users inside a container are send to this address.
- `REMOTES`: E-mail relay server the container should be using to send e-mails.
- `LOG_TO_STDOUT`: If set to `1` output logs to stdout (retrievable using `docker logs`) instead to `/var/log/nullmailer`.

## Description

Image with a simple e-mailing out of the container using [nullmailer](http://untroubled.org/nullmailer/).

## GitHub mirror

There is also a [read-only GitHub mirror available](https://github.com/tozd/docker-mailer),
if you need to fork the project there.
