.. _images:

====================
ExPECA Docker Images
====================

This guide provides an overview of Docker images stored in the **ExPECA Docker Hub repository** (``expecahub``).

When pulling or running these images, use the following format::

   expecahub/<image-name>:<version>

-----------------
Available Images
-----------------

base
----

**Image:** ``expecahub/base:latest``

A lightweight base image that provides:

- **SSH support** - allows secure access into the container using either a public or private IP address.
- **Docker-in-Docker (DIND)** - enables running Docker inside the container.

**Environment Variables**

+----------------+------------------------+----------+
| Variable       | Description            | Required |
+================+========================+==========+
| ``PASS``       | Root password          | Yes      |
+----------------+------------------------+----------+
| ``DNS_IP``     | Custom DNS server      | No       |
+----------------+------------------------+----------+
| ``GATEWAY_IP`` | Custom network gateway | No       |
+----------------+------------------------+----------+



visual
------

**Image:** ``expecahub/visual:latest``

A visualization stack image with integrated monitoring and networking capabilities:

- **Grafana, InfluxDB, and MQTT** - for visualization (see ExPECA user guides for setup details).
- **SSH support** - allows secure access into the container using either a public or private IP address.
- **Docker-in-Docker (DIND)** - enables running Docker inside the container.

**Environment Variables**

+---------------+--------------------------------+----------+
| Variable      | Description                    | Required |
+===============+================================+==========+
| ``PASS``      | Root password                  | Yes      |
+---------------+--------------------------------+----------+
| ``MQTT_USER`` | Username for the MQTT broker   | Yes      |
+---------------+--------------------------------+----------+
| ``MQTT_PASS`` | Password for the MQTT broker   | Yes      |
+---------------+--------------------------------+----------+
| ``DNS_IP``    | Custom DNS server              | No       |
+---------------+--------------------------------+----------+
| ``GATEWAY_IP``| Custom network gateway         | No       |
+---------------+--------------------------------+----------+

