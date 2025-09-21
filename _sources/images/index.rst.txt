.. _images:

====================
ExPECA Docker Images
====================

This guide provides an overview of Docker images stored in the **ExPECA Docker Hub repository** (``expecahub``).

When pulling or running these images, use the following format::

   expecahub/<image-name>:<version>

The images here are "multi-architecture" images (amd64/arm64), and can be loaded onto our Dell workers as well as our Raspberry Pi workers.

-----------------
Available Images
-----------------

base
----

**Image:** ``expecahub/base:latest``

A lightweight base image that provides:

- **SSH support** - Allows secure access into the container using either a public or private IP address.
- **Docker-in-Docker (DIND)** - Enables running Docker inside the container.

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

**Toolbox**

The image includes a "/root/toolbox" directory, under which you can find various scripts with corresponding user guides. These include:

- **Netfilter Tables script** - Allows a container to forward traffic to another destination. Can, for example,
  be used to do port-forwarding of traffic coming in to a public IP address. 
- **Network Emulator script** - This script simulates network conditions using Linux tc (Traffic Control). 
  It supports delay, jitter, loss, duplication, corruption, reordering, and rate limiting.


visual
------

**Image:** ``expecahub/visual:latest``

A visualization image with integrated monitoring and networking capabilities:

- **Grafana, InfluxDB, and MQTT** - Data visualization, database, and data broker/streaming applications.
- **SSH support** - Allows secure access into the container using either a public or private IP address.
- **Docker-in-Docker (DIND)** - Enables running Docker inside the container.

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

See "Data Visualization" user guide for more information about usage.
