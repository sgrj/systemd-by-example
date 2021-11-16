# A minimal example

A minimal systemd setup.

Build the image with
```
podman build --tag systemd .
```
and then run the container with
``` {.bash .execution}
podman run --rm --name systemd systemd
```
