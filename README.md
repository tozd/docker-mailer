# tozd/mailer

<https://gitlab.com/tozd/docker/mailer>

Available as:

- [`tozd/mailer`](https://hub.docker.com/r/tozd/mailer)
- [`registry.gitlab.com/tozd/docker/mailer`](https://gitlab.com/tozd/docker/mailer/container_registry)

## Image inheritance

[`tozd/base`](https://gitlab.com/tozd/docker/base) ← [`tozd/runit`](https://gitlab.com/tozd/docker/runit) ← `tozd/mailer`

See also [`tozd/nginx-mailer`](https://gitlab.com/tozd/docker/nginx-mailer).

## Tags

- `ubuntu-trusty`: nullmailer 1.11
- `ubuntu-xenial`: nullmailer 1.13
- `ubuntu-bionic`: nullmailer 2.1
- `ubuntu-focal`: nullmailer 2.2
- `ubuntu-jammy`: nullmailer 2.2

## Volumes

- `/var/log/nullmailer`: log files
- `/var/spool/nullmailer`: work files (e.g., queue), persist this volume to not lose state

## Variables

- `ADMINADDR`: If set, all e-mails to system users inside a container are send to this address.
- `REMOTES`: E-mail relay server the container should be using to send e-mails.

## Description

Image with a simple e-mailing out of the container using [nullmailer](http://untroubled.org/nullmailer/).
