CyberCity 3D
============

.. note:: The CyberCity 3D feature is not included yet.

A CyberCity 3D layer adds low resolution 3D buildings to your map. These buildings are created by `CyberCity 3D <http://www.cybercity3d.com/>`_ (CC3D) based on aerial photography. The buildings are lightweight but have accurate roof shapes and building shapes. They don't have facade detail or textures. This makes them perfect for visualisations on a city scale.

.. figure:: ..\_images\cc3d_amsterdam_overview.jpg

*Amsterdam central station and the inner city on the foreground with CyberCity 3D buildings. In the background you can see extruded openstreetmap buildings. None of these buildings have been hand modeled.*

Available buildings
-------------------

CC3D has over 1.25 million buildings available in over 90 cities. Their focus is on the US, but they also have lots of buildings in Europe and other cities. Check out their coverage `here <http://www.cybercity3d.com/3d-library>`_. This content is available immediately. They can also create the buildings or an area of your choice on demand. Maproom lets you easily define the area you need and communicate with CC3D about that.

Premium content
---------------

The CC3D buildings are premium content. You can order the buildings through Maproom and orders are processed by CC3D themselves. Maproom let's you easily integrate these buildings in your maps. CC3D charges for their buildings per square kilometer. Once you've purchased an area, you can use this in as many maps as you like.

Off the shelf buildings
^^^^^^^^^^^^^^^^^^^^^^^

* 0-10 km2: $500/km2
* 10+ km2: $300/km2

New buildings, 2 km2 minimum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* $1800/km2

Overview
--------

When you want to use CC3D buildings in a map, you can either use the CyberCity3D map preset to start a new map, or add a CyberCity3D layer to an existing map. A CC3D layer has two sections. The first section deals with the CC3D buildings you already own. The second section shows you the areas available through CC3D and it also enables you to order CC3D buildings directly.

.. figure:: ..\_images\MPR_2016-12-02_2210.png

*Two sections: My CyberCity 3D models and the CyberCity 3D library*

Adding buildings to a map
^^^^^^^^^^^^^^^^^^^^^^^^^

Let's assume you already have buildings purchased and placed in the repository you can select it from the list and add them to the map by pressing the ``Place selected`` button. As with all other map layers, an area of the data is added to your map. If you have an area of 5 by 5 km of buildings and you set the area of your map layer to 1 by 1 km, only the smaller area will be added to your map. This reduces waiting times if you only need a smaller part of your buildings as importing many buildigns takes a bit of time.

Each building is placed geographically accurate and it's also projected in the current map projection. This means that if my map space is set to a location in London and I add buildings from New York these buildings will appear quite far away in 3dsMax. 3dsMax will not like this as it has a hard time dealing with large distances (between London and New York) and high accuracy (the 3D buildings are very accurate) at the same time. Make sure that if you're placing New York buildings your map space is also set to New York or somewhere near.

Building repository
^^^^^^^^^^^^^^^^^^^

In you've just ordered and received buildings from CC3D, you need to place them into your repository. To do this, press the ``Open...`` button in the ``My CyberCity 3D models`` section. This opens your repository. Then navigate to the ``Purchased``. In there you can make a new folder with a descriptive name of the area you've bought, for instance ``Amsterdam, trainstation area``. In that folder you need to make two more folders, one called ``model``, the other called ``outline``. You can unzip your models in the ``model`` folder. The zip you've received from CC3D should contain two folders and a file: ``dae_images`` (usually empty), ``dae_models`` (contains a list of collada files, the actual 3D models) and a csv file. If you've received an outline, you need to put that in the folder ``outline`` you've just created yourself. The outline is a shapefile which actually consists of a bunch of files, one of which has an extension ``.shp``. Just place all of the files you've gotten in this folder.

When you restart Maproom and create a CC3D map layer, your new'y added folder will appear in your models list.

.. figure:: ..\_images\MPR_2016-12-02_2209.png

*The resulting folder structure of a single area of CC3D buildings*

The CyberCity 3D library
------------------------

The second section of the map layer shows you the CC3D library. It contains outlines of all available building CC3D has in their library. This makes it easy to evaluate if they have buildings you can use right now in your projects. Just pick a city from the list and press ``Show selected`` and an outline is placed in your map. You can also press ``Show all`` to see each available area in your map.

.. figure:: ..\_images\MPR_2016-12-02_2211.png

*A sample of the available buildings*

Ordering CC3D buildings
^^^^^^^^^^^^^^^^^^^^^^^

You order CC3D buildings directly from them CC3D. There are two ways you can order: either order one of the available cities or order a custom area. A custom area can either be part of an existing city, a new area or a combination of both. You can specify the custom area by creating a closed shape, select it and press ``Order custom area``. It helps if you first create a satellite map of the area you're interested in and then draw on top of that. 

Either way, using an existing city or custom outline, the area is sent to CC3D and you'll receive a confirmation email of your order. CC3D will further process your order and get in touch with you. They also might modify the outline of your area to avoid split buildings. Payment is also arranged directly with CC3D.

Example
-------

Here's an example which shows how you can combine CC3D buildings with openstreetmap buildings and bing satellite images.

.. figure:: ..\_images\cc3d_chicago_center_osm.jpg

*Chicago inner city in extruded openstreetmap buildings. OSM contains quite a bit of accurate height information which is used by the stylesheet to extrude the buildings to the correct height*

.. figure:: ..\_images\cc3d_chicago_center_cc3d.jpg

*The same area with buildings from CC3D*

.. figure:: ..\_images\cc3d_chicago_close_osm.jpg

*Closeup with osm*

.. figure:: ..\_images\cc3d_chicago_close_cc3d.jpg

*Closeup with CC3D. Here the benefit of the CC3D buildings is really visible*

.. figure:: ..\_images\cc3d_chicago_center_combo.jpg

*OSM and CC3D combined. CC3D in the center and OSM around the edges. The buildings blend nicely.*

.. figure:: ..\_images\cc3d_chicago_combo_bing.jpg

*The same buildings on top of a bing satellite map*

.. figure:: ..\_images\cc3d_chicago_combo_roofs_bing.jpg

*And finally the roof surfaces mapped with the same satellite images as used on the ground*