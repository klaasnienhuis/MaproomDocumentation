.. _map-location:

Location
========

.. _location-offset:

Offset
------

Each map layer has a location relative to the space of the complete map. This is called *offset*. The map layer uses the location set in the map space and adds an offset to it. By default this offset is set to 0,0. The offset is specified in projected map units which translates roughly to kilometers. If you change the offset of a map layer the location of this layer is calculated in degrees immediately and the map-helper in the scene is move accordingly. You can also move the map-helper in the scene. In that case the location and offset are calculated and displayed. For more on map helpers, go here: :ref:`map-helpers`

.. _offset-pyramid:

Offsetting a map layer comes in handy in several situations. When you're making an animation which zooms in on a particular area, you need to have a sharp map image at every camera position. However, it's impossible to make a map of very large areas at a very high zoomlevel. You can use the offset and push properties of a map layer to create a map *pyramid*. Create multiple layers with increasing zoomlevel and decreasing size which follow the camera motion. This ensures you always have a sharp map. 

.. note:: An automated way to get a zoomable and always sharp map is avaialbe with the new Ripple map type: :ref:`ripple`

.. figure:: _images\MPR_2015-09-10_1603.png

Four map layers "follow" the camera path and provide increasing while the camera moves closer to the map

.. raw:: html

		<iframe width="700" height="394" src="https://www.youtube.com/embed/nMT3g81je4Y?rel=0" frameborder="0" allowfullscreen></iframe>
		
Zooming into a map

.. figure:: _images\2015-09-10_193805.png

At the top: the location of the entire map. At the bottom: the location and offset of an individual map layer

.. note:: Map images from the same map provider might have drastically different colors at different zoomlevels. You can tweak the colors in photoshop or with a color correct map in 3ds Max though to get a consistent look.

Another use of offset is to help find a particular area on a map. You have one, big map and a smaller one on top which has a higher zoomlevel. Now you use the offset on the smaller map to find an area on the bigger map. This is similar to using a magnifying glass.

.. _video_offset:

.. raw:: html

		<iframe width="700" height="525" src="https://www.youtube.com/embed/IsmCjQvJpDY?rel=0" frameborder="0" allowfullscreen></iframe>
		
Finding an interesting area with offset

Area
----

A map layer has an area. The area sets the boundaries for the map data used in this layer. In a terrain layer setting the area to 10x10 for instance will limit the downloaded map tiles to an area of 10x10 projected map units (rougly 10x10 KM). Some data sources will exceed the area, sometimes quite a lot. This happens mainly when using openstreetmap data. the bulk of the downloaded data falls within the area. Large elements, such as railroads or country borders which touch this area might be downloaded entirely. This is done to avoid clipping of elements.

.. figure:: _images\MPR_2015-09-09_1594_01.png

Offset and area

If you specify an area which goes over a threshold, about 25000 KM in either width or height, Maproom will create a worldmap. To get the world dimensions, you can also press the ``Give me the world`` button. A map layer with a world size are offset to latitude longitude 0,0 automatically.

.. figure:: _images\MPR_2015-09-09_1595_01.png

World map dimensions

.. _location-push:

Push
----

When you have multiple map layers, you could move each layer to a separate height to avoid z-fighting. You can do this manually or by using the *push* property in the layers. In the example I've placed three satellite images on top of each other. The base layer is a big map of Berlin and the surrounding area. The second layer covers most of the city and has more detail (i.e. a higher zoomlevel). The third layer is even smaller and more zoomed in. Layer two is pushed 1 unit. Layer three is pushed 2 units. 

.. figure:: _images\MPR_2015-09-09_1596_01.png

Push

.. figure:: _images\MPR_2015-09-09_1598.jpg

Three layers stacked on top of each other

.. figure:: _images\MPR_2015-09-09_1599.jpg

Increasing detail

.. figure:: _images\MPR_2015-09-09_1600.jpg

The smallest area has the highest detail

.. figure:: _images\MPR_2015-09-09_1597.png

The push property in the layer panel

.. figure:: _images\MPR_2015-09-09_1601.png

The stacked layers are pushed apart