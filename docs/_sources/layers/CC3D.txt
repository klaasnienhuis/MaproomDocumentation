CyberCity 3D
============

.. note:: The CyberCity 3D feature is not included yet.

A CyberCity 3D layer adds low resolution 3D buildings to your map. These buildings are created by `CyberCity 3D <http://www.cybercity3d.com/>`_ (CC3D) based on aerial photography. The buildings are lightweight but have accurate roof shapes and building shapes. They don't have facade detail or textures. This makes them perfect for visualisations on a city scale. All CyberCity 3D buildings are precisely constructed with up to 4 inch accuracy to reflect real world dimensions from the roof down.

.. figure:: ..\_images\cc3d_amsterdam_overview.jpg

*Amsterdam central station and the inner city on the foreground with CyberCity 3D buildings. In the background you can see extruded openstreetmap buildings. None of these buildings have been hand modeled.*

Available buildings
-------------------

CC3D has over 1.25 million buildings available in over 90 cities. Their focus is on the US, but they also have lots of buildings in Europe and other cities. Check out their coverage `here <http://www.cybercity3d.com/3d-library>`_. This content is available immediately. They can also create the buildings or an area of your choice on demand. Maproom lets you easily define the area you need and communicate with CC3D about that.

Premium content
---------------

The CC3D buildings are premium content. You can order the buildings through Maproom and orders are processed by CC3D themselves. Maproom let's you easily integrate these buildings in your maps. CC3D charges for their buildings per square kilometer. Once you've purchased an area, you can use this in as many maps as you like.

Off the shelf buildings, 1 km2 minimum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* $400/km2

New buildings, 2 km2 minimum
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* $1800/km2

Terms of use for the CyberCity 3D content
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When you first open a cyberCity 3D map layer you are greeted by a notification. It draws your attention to the terms and conditions related to the CC3D data. The toc are laid out below. You need to agree with these terms to be able to use the CC3D data.

.. figure:: ..\_images\MPR_2016-12-09_2216.png

*The toc notification*


These "Terms of Use" set forth the terms and conditions that apply to your use of CyberCity 3D, Inc. 3D building models (the "data"). By using the data, you agree to comply with all of the Terms of Use set forth herein. The right to use the data is personal to you and is not transferable to any other person or entity.

**Copyrights and Trademarks**

A. All information contained in the data are Copyright CyberCity 3D, Inc., 2016. All rights reserved.
B. No person is authorized to distribute or sell the data to any other person(s) or organization(s) under any circumstances.  Use of the data outside of Maproom plug-in for the Autodesk 3ds Max application is prohibited.

**Changes to These Terms of Use**

CyberCity 3D, Inc. reserves the right to change these Terms of Use at any time by posting new Terms of Use at this location. You can send e-mail to CyberCity 3D, Inc. with any questions relating to these Terms of Use at info@cybercity3d.com.

Overview
--------

When you want to use CC3D buildings in a map, you can either use the CyberCity3D map preset to start a new map, or add a CyberCity3D layer to an existing map. A CC3D layer has two sections. The first section deals with the CC3D buildings you already own. The second section shows you the areas available through CC3D and it also enables you to order CC3D buildings directly.

.. figure:: ..\_images\MPR_2016-12-09_2217.png

*Two sections: My CyberCity 3D models and the CyberCity 3D library*

Sample data
^^^^^^^^^^^

After you've agreed to the terms you're greeted by yet another notification (I know, I'm sorry about this...). CyberCity 3D has made three sample areas of their data available to use in Maproom, for free! Even if you're a user of the free version of Maproom, you can use this data and evaluate it.

If you want this data, press the ``Get this data now`` button. It takes you to the settings page where you can request the sample data. More on that here: :ref:`sampledata`.

.. figure:: ..\_images\MPR_2016-12-09_2215.png

*The sample data notification*

Once you've downloaded the sample data, you need to "install" these zipfiles into your repository: :ref:`cc3drepo`

Adding buildings to a map
^^^^^^^^^^^^^^^^^^^^^^^^^

Let's assume you already have buildings purchased and installed in the repository you can select them from the list and add them to the map by pressing the ``Place selected`` button. As with all other map layers, an area of the data is added to your map. If you have an area of 5 by 5 km of buildings and you set the area of your map layer to 1 by 1 km, only the smaller section will be added to your map. This reduces waiting times if you only need a smaller part of your buildings as importing many buildigns takes a bit of time.

Each building is placed geographically accurate and it's also projected in the current map projection. This means that if the map space is set to a location in London and I add buildings from New York these buildings will appear quite far away in 3dsMax. 3dsMax will not like this as it has a hard time dealing with large distances (between London and New York) and high accuracy (the 3D buildings are very accurate) at the same time. Make sure that if you're placing New York buildings your map space is also set to New York or somewhere near.

.. _cc3drepo:

Building repository
^^^^^^^^^^^^^^^^^^^

The building repository is the place to put your CC3D buildings. Once placed there, Maproom is able to use them in maps. If you've just downloaded buildings from CC3D, you need to install them into your repository. Whether you're using the free sample data, or a purchased area, the procedure is the same.

.. figure:: ..\_images\MPR_2016-12-09_2217_A.png

*Install new CC3D models in your repository. Press* ``Add new model...``

.. figure:: ..\_images\MPR_2016-12-09_2218.png

*Pick a zip file you've received from CC3D*

.. figure:: ..\_images\MPR_2016-12-09_2219.png

*The data is placed in your repository and ready to use*

If you need to make manual adjustments to your repository, you can press the ``Open...`` button. Keep in mind that Maproom relies on a strict folder structure with naming conventions. 

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

*Chicago inner city in extruded openstreetmap buildings. OSM contains some height information in dense urban areas which is used by the stylesheet to extrue the buildings to the correct height.*

.. figure:: ..\_images\cc3d_chicago_center_cc3d.jpg

*The same area with buildings from CC3D. All CyberCity 3D buildings are precisely constructed with up to 4 inch accuracy to reflect real world dimensions from the roof down.*

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