# Five services with `Wants=`, `Requires=`, and `Conflicts=`

Source code for the example in https://seb.jambor.dev/posts/systemd-by-example-part-2-dependencies/#five-services-with-wants-requires-and-conflicts.

Build and run the image with
```
podman build --tag systemd . && podman run --tty --rm --name systemd systemd
```

First start `d.service` with
```
podman exec systemd systemctl start d.service --no-block
```
and check the logs with
```
podman exec systemd journalctl
```

Then start `a.service` with
```
podman exec systemd systemctl start a.service --no-block
```
and check the logs again.
