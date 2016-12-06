.. _height:

Height
======

Heights can be loaded into a map based on data sources as well. There are several global data sources of which SRTM3 is currently available in Maproom. You can load SRTM3 data in a terrain layer by picking it from the ``Terrain heights`` dropdown.

.. figure:: _images\MPR_2016-10-03_2140.png

*An overview of the available terrain height datasets*

.. raw:: html

	<iframe width="700" height="525" src="https://www.youtube.com/embed/lyZ5c4itN9Y" frameborder="0" allowfullscreen></iframe>
	
*Adding heights to OSM data*

.. _srtm3:

SRTM
----

SRTM is a near global dataset captured by a space shuttle. The resolution or SRTM3 is 3 arc-sec which is about 90m per pixel. SRTM1 is about 1 arc-sec which amounts to roughly 30m per pixel. `You can read more about this here <http://www.webgis.com/srtm3.html>`_

.. figure:: _images\Continent_def.jpg

*An overview of SRTM coverage*

This resolution makes SRTM3 very suitable for medium sized terrains ranging from 500 km to 50 km. This translates to a terrain height map of about 5000 to 500 pixels. It will work just fine on smaller areas but you'll see the data lacks resolution. By default the terrain height map is made smooth but if you switch off the filtering you can see the individual samples. SRTM1 has a resolution of about 9 times as high. This works better for smaller areas.

.. figure:: _images\SRTM3Sample_250km.jpg

*SRTM3: A 250 km area with a terrain map of about 2700*2700 pixels*

.. figure:: _images\SRTM3Sample_50km.jpg

*SRTM3: A 50 km area with a terrain map of about 550*500 pixels*

.. figure:: _images\SRTM3Sample_5km.jpg

*SRTM3: A 5 km area with a terrain map of 53*53 pixels*

.. figure:: _images\SRTM3Sample_5km_unfiltered.jpg

*SRTM3: The same 5 km area with an unfiltered height map*

In the last image you can clearly see the individual height samples.

Mesh density
------------

The level of detail in the terrain not only depends on the size and resolution of the displacement map but also on the density of the mesh. The map object is basically a plane with a turbosmooth modifier applied. By default the turbosmooth iterations value is set to a level relative to the size of your map. If you have a big map, the mesh is subdivided less than when you have a small map. This avoids crashing max by using unrealistic turbosmooth values.

You can finetune the mesh density by using the ```Terrain mesh density``` slider. This sets the number of segments on the map plane. You can also manually go into the map object and alter the turbosmooth subdivisions.

.. figure:: _images\MPR_2016-10-03_2141.png

*Finetune the terrain mesh density*

Here's a series of renders of the same terrain with increasing detail (i.e. decreasing subdivision). Each render uses the same SRTM1 terrain and displacement map of about 4800*4800 pixels.

.. figure:: _images\MPR_Etna_SRTM1_10.jpg

*Terrain mesh density: 10*

.. figure:: _images\MPR_Etna_SRTM1_25.jpg

*Terrain mesh density: 25*

.. figure:: _images\MPR_Etna_SRTM1_40.jpg

*Terrain mesh density: 40*

.. figure:: _images\MPR_Etna_SRTM1_10_wire.jpg

*Terrain mesh density: 10*

.. figure:: _images\MPR_Etna_SRTM1_25_wire.jpg

*Terrain mesh density: 25*

.. figure:: _images\MPR_Etna_SRTM1_40_wire.jpg

*Terrain mesh density: 40*

