# tozd/mailer

<https://gitlab.com/tozd/docker/mailer>

Available as:

- [`tozd/mailer`](https://hub.docker.com/r/tozd/mailer)
- [`registry.gitlab.com/tozd/docker/mailer`](https://gitlab.com/tozd/docker/mailer/container_registry)

## Image hierarchy

[`tozd/base`](https://gitlab.com/tozd/docker/base) ← [`tozd/runit`](https://gitlab.com/tozd/docker/runit) ← `tozd/mailer`

See also [`tozd/nginx-mailer`](https://gitlab.com/tozd/docker/nginx-mailer).

## Volumes

- `/var/log/nullmailer`: log files
- `/var/spool/nullmailer`: work files (e.g., queue), persist this volume to not lose state

## Variables

- `ADMINADDR`: If set, all e-mails to system users inside a container are send to this address.
- `REMOTES`: E-mail relay server the container should be using to send e-mails.

## Description

Image with a simple e-mailing out of the container using [nullmailer](http://untroubled.org/nullmailer/).
