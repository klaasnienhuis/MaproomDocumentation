.. _cc3d:

CyberCity 3D, Inc. (CC3D)
=========================

The CyberCity 3D layer in Maproom adds highly accurate 3D buildings to your map. CC3D creates these buildings with its patented modeling technology utilizing photogrammetry of stereo imagery. These lightweight buildings include accurate roof and building geometry. This makes them perfect for city-wide visualizations. CC3D constructs all its buildings precisely with up to four-inch accuracy to reflect real world dimensions from the roof down.

.. note:: You must purchase Maproom Pro to use CyberCity 3D data in Maproom. Sample CC3D data is available to all Maproom users.

.. figure:: ..\_images\cc3d_amsterdam_overview.jpg

*Amsterdam Central Station in the foreground. CyberCity 3D buildings adjacent with extruded OpenStreetMap (OSM) buildings in the background. None of these buildings have been hand-modeled.*

.. raw:: html

		<iframe width="700" height="500" src="https://www.youtube.com/embed/_-arLoGjOM4?rel=0" frameborder="0" allowfullscreen></iframe>


3D Coverage
-----------

CC3D offers more than 1.25 million building in over 90 cities. The Company’s focus is in the U.S., but they have also modeled numerous international cities. Check out CyberCity 3D’s off-the-shelf library `here <http://www.cybercity3d.com/3d-library>`_; this data is immediately available. CC3D also creates other city models around the globe on demand. Maproom enables you to easily define the area you need and communicate that information to CC3D.

Ordering Process
----------------

It’s easy to order 3D buildings through Maproom. CyberCity 3D will then process each request directly. CC3D charges on a per square kilometer basis. Once you’ve purchased an area, you may use it in as many maps as you like.

* Off-the-Shelf Buildings, 1 km :sup:`2` minimum, $400/km :sup:`2`
* New Build, 2 km :sup:`2` minimum, $1,800/km :sup:`2`

.. _cc3dterms:

CyberCity 3D Content Terms of Use
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

CyberCity 3D, Inc. building data is copyrighted. To utilize CC3D data, you must read and agree to the terms laid out on this website. When you first open a CC3D map layer, you are greeted by a notification that takes you to those terms and conditions. 

.. figure:: ..\_images\MPR_2016-12-09_2216.png

*The notification*

**Terms of Use**

These "Terms of Use" set forth the terms and conditions that apply to your use of CyberCity 3D, Inc. 3D building models (the "data"). By using the data, you agree to comply with all of the Terms of Use set forth herein. The right to use the data is personal to you and is not transferable to any other person or entity.

**Copyrights and Trademarks**

* All information contained in the data are Copyright CyberCity 3D, Inc., 2016. All rights reserved.
* No person is authorized to distribute or sell the data to any other person(s) or organization(s) under any circumstances.
* Use of the data outside of Maproom plug-in for the Autodesk 3ds Max application is prohibited.

**Changes to These Terms of Use**

CyberCity 3D, Inc. reserves the right to change these Terms of Use at any time by posting new Terms of Use at this location. You can send e-mail to CyberCity 3D, Inc. with any questions relating to these Terms of Use at info@cybercity3d.com.

Overview
--------

There are two methods to bring CC3D buildings into Maproom.  

1. Use the CC3D map preset to start a new map.
2. Add a CC3D layer to an existing map. 

A CC3D layer includes two sections. The first deals with the CC3D buildings you already own. The second shows you other areas available through CC3D, and enables you to order them from the off-the-shelf library. Other "New build" cities across the world can also be ordered directly from CyberCity 3D.

.. figure:: ..\_images\MPR_2016-12-09_2217.png

*Two sections: My CyberCity 3D models and the CyberCity 3D library*

.. _cc3dsampledata:

Sample data
^^^^^^^^^^^

After agreeing to the Terms and Conditions, you’ll get another notification that offers three free sample areas of CyberCity 3D data ready to use in Maproom. Even users of the free version of Maproom can access this sample data and evaluate it.

.. figure:: ..\_images\London_CC3D_sample_001.jpg

*The London Leicester Square sample data*

Press the "Get this data now" button to obtain the sample data More on that here: :ref:`sampledata`. Once you've downloaded the sample data, you need to "install" the zip files in your building repository: :ref:`cc3drepo`

.. figure:: ..\_images\MPR_2016-12-09_2215.png

*The sample data notification*

Adding buildings to a map
^^^^^^^^^^^^^^^^^^^^^^^^^

Once buildings have been installed in the building repository you can select your choice from the list and add it to the map by pressing the ``Place selected`` button. Along with the 3D models, CyberCity 3D will also provide an outline layer of your area of interest. Use the ``Show selected`` button to preview your model as an outline. You can also use ``Show all`` to place outlines of all the models you have installed.

As with all other map layers, an area of the data is added to your map. If you have an area of 5 by 5 km of buildings and you set the area of your map layer to 1 by 1 km, only the smaller section will be added to your map. This reduces waiting times if you only need a smaller part of your buildings as importing many buildings takes a bit of time.

.. figure:: ..\_images\MPR_2016-12-09_2217_B.png

*Use outlines to preview building placement.*

.. figure:: ..\_images\MPR_2016-12-09_2220.png

*London Leicester Square sample outline*

Each building is placed geographically accurate and it's also projected in the current map projection. This means that if the map space is set to a location in London and I add buildings from New York these buildings will appear quite far away in 3dsMax. 3dsMax will not like this as it has a hard time dealing with large distances (between London and New York) and high accuracy (the 3D buildings are very accurate) at the same time. Make sure that if you're placing New York buildings your map space is also set to New York or somewhere near.

.. _cc3drepo:

Building repository
^^^^^^^^^^^^^^^^^^^

The building repository houses your CC3D buildings. Once placed there, Maproom then has the ability to use the buildings in maps. After downloading buildings from CC3D, install them into your repository. Whether you’re using a purchased area or free sample data, the procedure is the same.

.. figure:: ..\_images\MPR_2016-12-09_2217_A.png

*Install new CC3D models into your building repository. Just press* ``Add new model...``

.. figure:: ..\_images\MPR_2016-12-09_2218.png

*Pick a zip file you've downloaded from CC3D*

.. figure:: ..\_images\MPR_2016-12-09_2219.png

*Once downloaded into the repository, the data is ready to use.*

Press the ``Open...`` button if you need to make minor adjustments to your repository. Keep in mind Maproom relies on a strict folder structure with naming conventions.

The CyberCity 3D City Library
-----------------------------

The second section of the map layer shows you the CC3D off-the-shelf library. It contains outlines of all of the available buildings CC3D has in its library. See immediately if the buildings you need are in the library or if you need to order new builds from CC3D.

Download outlines
^^^^^^^^^^^^^^^^^

Before you can view the outlines, you need to download an install them. Don't worry, it's all automatic and doesn't take more than a few seconds. Open the CC3D Library list and pick the ``Download CyberCity 3D coverage outlines`` option. The outlines are downloaded and placed in the repository. You can re-download the files whenever you want.

Use outlines
^^^^^^^^^^^^

Choose a city from the list and press ``Show selected``. An outline of that city will appear on your map. You can also press ``Show all`` to see each available area in your map.

.. figure:: ..\_images\MPR_2016-12-02_2211.png

*A sample of CyberCity 3D off-the-shelf buildings*

.. figure:: ..\_images\MPR_2016-12-09_2221.png

*CC3D library coverage in and around Los Angeles, CA*

.. _cc3dordering:

Ordering CC3D buildings
-----------------------

Maproom provides a handy way to order and pay for your buildings directly to CyberCity 3D. Any questions about data can be sent to info@cybercity3d.com. Check out their website at `www.cybercity.com <http://www.cybercity3d.com/>`_. Try out the free sample data first to get a feel for the CC3D buildings: :ref:`cc3dsampledata`

.. figure:: ..\_images\MPR_2016-12-09_2217_C.png

How to order
^^^^^^^^^^^^

Order data in two different ways

#. Order an off-the-shelf library city
#. Order a custom area
	#. part of an off-the-shelf library city
	#. a new build city or area
	#. a combination of both
	
Existing library cities can be downloaded immediately. New build cities or areas will be created quickly by CC3D.

Specifying your custom area

#. Create a satellite map of the area you need
#. Draw a rectangle or custom closed shape or spline on the map detailing the area you need
#. Select the shape
#. Press ``Order custom area``

Whether you choose an existing city or a new build custom outline, you’ll receive an email confirmation of your order from CyberCity 3D. Existing library city areas chosen will be sent to you promptly. CC3D will further process custom orders, and contact you if necessary. Please note that the outline of your area may be slightly modified to avoid split buildings. Payment is also arranged directly with CC3D.

Example
-------

Maproom is all about combining different types of data to create the map you need. Here's a map combining CC3D buildings, OSM buildings and a Bing satellite image.

.. figure:: ..\_images\cc3d_chicago_center_osm.jpg

*Downtown Chicago in extruded OSM buildings. OSM contains some height information in dense urban areas. It is used by the style sheet to extrude buildings to the correct height.*

.. figure:: ..\_images\cc3d_chicago_center_cc3d.jpg

*The same area with buildings from CC3D. All CyberCity 3D buildings are precisely constructed with up to 4 inch accuracy to reflect real world dimensions from the roof down.*

.. figure:: ..\_images\cc3d_chicago_close_osm.jpg

*Close-up of downtown Chicago with OSM*

.. figure:: ..\_images\cc3d_chicago_close_cc3d.jpg

*Close-up with CC3D buildings clearly showing the intricate building geometry.*

.. figure:: ..\_images\cc3d_chicago_center_combo.jpg

*CC3D and OSM combined. CC3D buildings are in the center with OSM buildings around the edges. The buildings blend nicely.*

.. figure:: ..\_images\cc3d_chicago_combo_bing.jpg

*The same downtown Chicago buildings on top of a Bing satellite map*

.. figure:: ..\_images\cc3d_chicago_combo_roofs_bing.jpg

*Finally, the roof surfaces mapped with the same satellite imagery as used on the ground*