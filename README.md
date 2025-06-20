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
- `ubuntu-noble`: nullmailer 2.2

## Volumes

- `/var/log/nullmailer`: Log files when `LOG_TO_STDOUT` is not set to `1`.
- `/var/spool/nullmailer`: Work files (e.g., queue). Persist this volume to not lose state.

## Variables

- `ADMINADDR`: If set, all e-mails to system users inside a container are send to this address.
- `REMOTES`: E-mail relay server the container should be using to send e-mails.
- `LOG_TO_STDOUT`: If set to `1` output logs to stdout (retrievable using `docker logs`) instead of log volumes.

## Description

Image with a simple e-mailing out of the container using [nullmailer](http://untroubled.org/nullmailer/).

When `LOG_TO_STDOUT` is set to `1`, Docker image logs output to stdout and stderr. All stdout output is JSON.

This image primarily serves as a base image for other images which need to send e-mails out.
It does not really deliver e-mails to wide Internet, but just relays it to the e-mail server
you configure in `REMOTES`. But programs in your extended images do not have to worry
about all that and can just use `sendmail` program locally.

If you need sending e-mails to wide Internet, consider using [`tozd/postfix`](https://gitlab.com/tozd/docker/postfix)
Docker image. You can also then set `REMOTES` to send all e-mail to a `tozd/postfix` container.

## GitHub mirror

There is also a [read-only GitHub mirror available](https://github.com/tozd/docker-mailer),
if you need to fork the project there.
