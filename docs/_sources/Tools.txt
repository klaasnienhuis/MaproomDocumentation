.. _tools:

Map Tools
=========

The map tools panel contains a collection of handy scripts you might need when working with the maps. Currently there's one tool but this collection will be expanded over time.

.. _exportmap-tools:

Export map
----------

When maps are created Maproom stores all created textures in a repository. This is a central folder structure where all the downloaded mapping data is stored. You can specify its location in the settings: :ref:`repository`. Most textures actually have the same filenames. This is unpractical when you want to do stuff with the map you've just created. Besides that, once the map is done you also can get rid of the map helpers. They are of no added value after you've built your map.

The ```Export Map``` tool collects all the assets used in your scene, gives them unique filenames and saves them in a timestamped folder next to your maxfile. After that it deletes all map helpers. This completely disconnects your map from Maproom. Use this if you want to send a map to somebody else or if you want to render your map on a renderfarm.