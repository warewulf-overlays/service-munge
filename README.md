# warewulf-overlay-munge
Munge setup overlay for Warewulf


This overlay assumes the `munge` and optionally `munge-devel` rpms are
installed in the container.


Due to the way WW templates work, the last byte in the munge key file matters.
This will produce a key which works with this overlay:

```
dd if=/dev/urandom | base64| head -c 1024 > /etc/munge/munge.key
echo >> /etc/munge/munge.key
```

