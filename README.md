Nginx Docker for git://ci
=========================

This nginx container needs to be running linked with the other containers in
order to resolve the host names.

Artifact Server
===============

The artifact server needs to be running before the nginx one.

* Hostname: `storage`
* Shared volumes in read only mode:
    * /mnt/artifacts
    * /mnt/artifacts-static

If more artifacts server are needed, number them and update the
`artifact-servers.conf` file with multiple upstream servers.

Hawkbit
=======

Run the Hawkbit container as normal.

* Hostname: `hawkbit`

LAVA
====

This needs to be tested.

* Hostname: `lava-titan`


TODO
====

* The hostname on each website configuration needs to be updated.
