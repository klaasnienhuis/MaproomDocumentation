.. _map-space:

Map Space
=========

Each map has a few global settings which are called the *Map space*. These options are

* Location
* Projection

Location
--------

The location determines where on earth the map is located. It's stored as decimal degrees in longitude and latitude. If you want to set or change the location of the entire map you can type in a new location, paste a location you got from somewhere else or use the **Find location** feature. After you've changed the location you need to update the space to commit these changes. If you change your mind you can discard the changes.

Find location
-------------

Instead of typing in location values yourself, you can just type the name of a location. Maproom will get the location itself. This process is called *geocoding* by the way.

.. figure:: \_images\MPR_2016-05-18_2026.png

A new map starts with a default location. Change it by typing in new coordinates or by finding a location by name

.. figure:: \_images\MPR_2015-10-26_1693.png

Find a location by typing a country, state, street or any info you have

.. figure:: \_images\MPR_2015-10-26_1694.png

You can refine your search or focus it on a specific country

.. figure:: \_images\MPR_2016-05-18_2027.png

After you've found your location you can either discard or commit your changes.

If you've changed the location, you need to update your maplayers. This is not done automatically. Check out :ref:`updating-map-layers` to see how to update a map layer.

Projection
----------

The projection of a map determines how the piece of earth you're mapping is unfolded into a flat plane. Online the most common projection is Mercator. This projection has a big distortion when zoomed out a lot. Areas near the poles are much larger than they actually are. Notice the size of Greenland?

That's why Maproom introduces multiple map projections to choose from. Changing the map projection influences how the entire map looks. It also has to be committed once changed.

.. figure:: \_images\MPR_2016-05-18_2028.png

Here's an overview of some of the projections available

.. figure:: \_images\MPR_2016-05-18_2025.png

A quick example shows how big an impact the chosen projection has on a map. From left to right: Equidistant Cylindrical, Gall Stereographic and Mercator

For more info on map projections read on: :ref:`projection-intro`.

Procedures
----------

Changing the location
^^^^^^^^^^^^^^^^^^^^^

#. Open the Map space layer of a map
#. Press the "Find location" button
#. Type in a location of a part of it and press "Lookup"
#. Doubleclick the location you want
#. in the Map space panel either press "Update space" to use this new location or press "Discard changes" to keep the original location.