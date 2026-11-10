.. _container-vs-telenor:

========================================
Running a container towards Telenor Edge
========================================

This guide will walk you through the steps of defining networking for Telenor Edge.
This will allow worker node containers, SDR networks (actually containers running on worker nodes), and EP5G to communicate with Telenor Edge applications.

.. figure:: telenor_netw.png
  :alt: Telenor Edge networking
  :figclass: screenshot

Step 1: Reserve a worker node
=============================

See the "reservation of a worker node" section.


Step 2: Create a container
==========================

Here, we connect a container application, running on a worker node, to the Telenor Edge. This involves including the container in the "telenor-shared-net" network
when starting the container.

* From the ExPECA home page, click *Container* -> *Containers*

.. figure:: container_run1.png
  :alt: Containers main page
  :figclass: screenshot

* Click *+ Create Container*
* See "Running a basic container" for the steps involved. We will here only focus on the data entered for network connection.
* Under "Networks" tab, bring "telenor-shared-net" to the top
* Under "Labels" tab, enter IP subnet and address to connect to the "telenor-shared-net" network, and to provide routing towards the Telenor Edge.
 
.. figure:: container_run2.png
  :alt: Containers networks page
  :figclass: screenshot
.. figure:: container_run3.png
  :alt: Containers labels page
  :figclass: screenshot

* Click *Create*

.. figure:: container_run4.png
  :alt: Containers main page
  :figclass: screenshot

* You should now be able to ping Telenor edge from within your container.
* In this case, we only ping the CPE Router (gateway to Telenor Edge), but you should be able to ping all the way to whatever application you have running on Telenor Edge.

.. figure:: container_run5.png
  :alt: Container console page
  :figclass: screenshot

