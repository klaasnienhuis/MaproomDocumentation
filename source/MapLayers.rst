.. _map-layers:

Map Layers
==========

A single map can have one or more map layers. You can use the same type of layers or mix different types together. For instance use two openstreetmap layers, one with buildings and the other one with roads. Or use a map with a satellite layer and an osm layer. Each layer can be offset [#]_ individually. When stacking multiple layers in a map, you need to take care of the z-fighting. Map layers by default are placed on the ground plane. You can push [#]_ maplayers to the front or to the back to get the right order in the map.

Check out the different types of layers you can use here :ref:`layers-toc`.


.. _updating-map-layers:

Building maps and updating them
-------------------------------

Generally you build a map by creating a maplayer, specifying the data you want to use and pressing the "build" or "update" button. Maproom will then get the data for you and make map geometry in your scene. Obviously the first map is never the final map and you need to update the map a few times. For instance change the zoomlevel on a terrain map, add heights, change the openstreetmap data. In addition to these changes you also can change the location of the map and the size of the area.

Maproom does not update your maps in real time. If you make any of these changes you have to press the "build" or "update" button again and the map is updated. To help you with this, Maproom will indicate if there are changes which need to be pushed to the map.

.. figure:: _images\MPR_2015-09-26_1636_cr.png

The basic state of a satellite map layer.

.. figure:: _images\MPR_2015-09-26_1637_cr.png

The zoomlevel has changed. The yellow border appears to indicate a change has been made and the "Update map images" button is highlighted. Press this button to apply these changes and update the map.

.. figure:: _images\MPR_2015-09-26_1638_cr.png

The area of the map has been altered. The yellow border indicates the location settings have changed and the "Update map images" button is highlighted. Press this button to update the map.

If you don't update the map and close Maproom, some changes will be reset and other changes will be remembered. In general: changes to the location (area, offset, push) are sticky. If you close Maproom and open it, the yellow border reappears to indicate you should update the map. Map layer changes (image source, zoom, terrain heights) are not sticky. If you close and open Maproom, any changes which have not been applied, will be forgotten.

Multiple layers in one map
--------------------------

Having multiple layers of different types in a single map is very powerful. It's easy to add an extra layer. Each layer has its own location controls.

.. figure:: _images\MPR_2015-09-10_1607.png

Start with a new map. Press "Add a new layer..."

.. figure:: _images\MPR_2015-09-10_1608.png

Pick a new layer type

.. figure:: _images\MPR_2015-09-10_1609.png

The new layer has been added

.. figure:: _images\MPR_2015-09-10_1606.png

Example: a satellite and shapefile layer

.. rubric:: Footnotes

.. [#] More about offset here: :ref:`location-offset`.
.. [#] More about push here: :ref:`location-push`.