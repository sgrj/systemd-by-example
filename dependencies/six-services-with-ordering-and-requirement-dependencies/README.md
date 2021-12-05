# Six services with ordering and requirement dependencies

Source code for the example in https://seb.jambor.dev/posts/systemd-by-example-part-2-dependencies/#six-services-with-ordering-and-requirement-dependencies.

Build and run the image with
```
podman build --tag systemd . && podman run --tty --rm --name systemd systemd
```

Then start the services with
```
podman exec systemd systemctl start f.service --no-block
```
or
```
podman exec systemd systemctl start e.service --no-block
```
and check the logs with
```
podman exec systemd journalctl
```
