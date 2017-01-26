Map Presets
===========

Maproom comes with a few map presets to make starting a map easier. A map preset is basically a map with a number of layers. Each map preset can also be made by starting with an empty map and adding these layers yourself.

Once a map preset has been loaded you need to request the actual data by pressing the "Update..." buttons from the individual layers. This will download the actual data and make maps of them.

Satellite
---------

The Satellite preset has a single terrain layer enabled with OSMmapnik as raster source. The default settings give you a map of Berlin and its surroundings.

.. figure:: _images\MPR_2015-09-08_1590.jpg

Berlin and its surroundings

.. figure:: _images\MPR_2015-09-08_1591.png

The *Satellite* preset default settings

Satellite and Terrain
---------------------

The Satellite and Terrain preset uses a single terrain layer with OSMmapnik as raster source and SRTM3 as source for heights. The default settings result in a piece of the Grand Canyon.

.. figure:: _images\Satallite_terrain.jpg

The Grand Canyon

.. figure:: _images\MPR_2015-09-08_1592.png

The *SatelliteTerrain* preset default settings

OSM
---

The openstreetmap preset uses a single osm layer which is set to download buildings. You can easily switch it to download other shapes from openstreetmap. The default settings give you the buildings located around Central Park in Manhattan.

.. figure:: _images\OSM_manhattan.jpg

Manhattan

.. figure:: _images\MPR_2015-09-08_1593.png

.. _preset-demo:

Demo presets
------------

There are three demo presets, available in Maproom Pro and Free. These are ``Demo New York``, ``Demo London`` and ``Demo Miami``. These three presets contain a satellite, openstreetmap and cyberCity 3D layer. The location and size of each preset is fixed, but you can experiment all you want with the different layers. 
The *osm* preset default settings

.. figure:: _images\MPR_2017-01-26_2270.png

*The Demo presets, also available in Maproom Free*

For the description of each maplayer check :ref:`cc3d`, :ref:`layer-osm` and :ref:`layer-satellite` . To work with the cyberCity 3D data you first need to download the free sample data, it's very easy: :ref:`cc3dsampledata`. Once you have it you can make maps exactly like these. These have been created with the Demo map presets.

.. figure:: _images\Maproom_CyberCity3D_London_small.jpg

*London Demo preset*

.. figure:: _images\Maproom_CyberCity3D_Miami_small.jpg

*Miami Demo preset*

.. figure:: _images\Maproom_CyberCity3D_NewYork_small.jpg

*New York Demo preset*

