.. _layer-shapefile:

Shapefile
=========

The shapefile is a format created by ESRI for GIS systems. It's widely adopted. A shapefile is usually a collection of files, containing geometric data (points, lines) and other data such as labels and tags. You can use your own shapefiles but the support in Maproom is rather limited. Maproom has been tested with the shapefiles from `Natural Earth <http://www.naturalearthdata.com/>`_. They maintain very good shapefiles which are exceptionally well suited to make large scale and world maps.

.. figure:: ..\_images\MPR_2015-09-14_1621.png

A map with two shapefile layers: global coastlines and international airpoirts

.. figure:: ..\_images\MPR_2015-09-14_1622.png

Notice the coastline is made for large scale maps. Also, some data from the shapefiles is loaded into maproom such as the airport names in this case.

Interface
---------

Pick a shapefile and press ``Place shapefile``. The shapefile is placed in your scene. In some cases data from the shapefile is retained. In the above example for instance the names of the airports or below the names of countries.

.. figure:: ..\_images\MPR_2015-09-26_1656.png

Press ``Pick...`` to open a file dialog and find the shapefile you want

.. figure:: ..\_images\MPR_2015-09-26_1658.png

This shapefile contains the coutnries at 1:110 million scale

.. figure:: ..\_images\MPR_2015-09-26_1659.png

Each shape has the name of the country it actually represents: very handy!