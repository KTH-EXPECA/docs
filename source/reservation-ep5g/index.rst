.. _reservation-ep5g:

===================
Reservation of EP5G
===================

This guide will walk you through the steps of looking up EP5G (Ericsson Private 5G) resource and
reserving it.

Step 1: Check Hardware discovery
================================

* From the ExPECA home page, click *Hardware discovery*
* Look up EP5G. Note the "segment ID" for it. You will use it later to make your reservation.

.. figure:: hw_discovery_ep5g.png
  :alt: Hardware discovery, EP5G
  :figclass: screenshot

Step 2: Reserving EP5G
======================

We need to reserve EP5G for our use.
When you create a reservation for EP5G, only you
and other users on your project will be able to use it for the time
specified. We will create a single day reservation for EP5G.

* In the sidebar, click *Reservations* -> *Leases*

.. figure:: lease01.png
  :alt: Main lease view
  :figclass: screenshot

* Click *Network Calendar*. This shows the current EP5G reservations (identified by "segment ID") in the system. Make sure EP5G
  is not reserved for the time you need it.

.. figure:: network_calendar.png
  :alt: Network calendar
  :figclass: screenshot

* Go back to the main lease page
* Click on the *+ Create Lease* button in the toolbar
* Type *my_ep5g_lease* for the lease name (or any name you want to call it)
* Make sure you always select a Start Date

.. figure:: create_lease01.png
  :alt: Create lease, image 1
  :figclass: screenshot

* Check the *Networks* -> *Reserve Network* box
* Type *ep5g_network* for the network name (or any name you want to call it)
* Find the *Networks* -> *Resource Properties* section. In the dropdown below *vlan_id*, select the "segment ID" you have for ep5g.
* Click the *Next* button, and then *Create*

.. figure:: create_lease02.png
  :alt: The Create Lease, image 2
  :figclass: screenshot

The reservation will start shortly, at which point you can continue.

.. note::

   When you set taday as start date and *now* as start time, the reservation will start as soon as possible
   and will last one day.

.. important::

   Do not attempt to stack reservations to circumvent the 7-day lease
   limitation. Your leases may be deleted. Please refer to the `best practices
   <https://www.chameleoncloud.org/learn/frequently-asked-questions/#toc-what-are-the-best-practices-of-chameleon-usage->`_
   if you require a longer reservation.

