Basic Concepts
==============

Building a proper map in 3ds Max requires a bit of a mapping 101. This is an overview of the concepts used in Maproom. For more in depth knowledge about these topics, follow the links.

Map data
--------

Maps are based on data. You don't just draw a map by hand! You take data from a source and build a map from it. There are many sources: raster tiles such as the images on Bing maps or Google maps, vectors such as openstreetmap, shapefiles or KML files and height data such as SRTM or .asc files. A single map can hold multiple data sources. Typically each data source is placed in a separate layer. 

Layers
------

A basic mapmaking concept in Maproom and in many other mapmaking applications is the use of layers. You can stack different kinds of map data on top of each other. For example: use satellite imagery as a base layer, add vector data for buildings and roads on a second layer and add terrain height data as a third layer. Each of these layers share some basic map settings but use different map data sources. Read more here: :ref:`map-layers`

Space
-----

A map in Maproom has a "space" property. This property contains a location in degrees (longitude/latitude) and a map projection. The location and projection apply to each map layer and determine how the map data is transformed. Read more here: :ref:`map-space`

Location
--------

Each maplayer has a few location related settings. You can make a map of 1x1 KM or a map of 1000x1000 KM which is determined by the map area. The layer can also have an offset. This shifts the map layer from the space-location. This is convenient when you want to position multiple smaller map layers in relation to a bigger map. Read more here: :ref:`map-location`

Projection
----------

Creating a flat map of a piece of the earth involves some sort of projection. This means the map has to be unfolded or unwrapped. This is actually the same concept as UVW unwrapping a sphere in 3ds Max. When projecting a map there's always some kind of distortion. There are different types of distortion but usually map projections are described by the property or properties they preserve such as distances, area, shape or angle. When creating a map it's important to pick an appropriate projection because no matter what, your map will be distorted. For instance when comparing countries and the amount of childbirths per capita you should use a projection which preserves area. But if you want to show how a certain airport is located and relates to other airports and cities you might want a projection which preserves distances. Read more here: :ref:`projection-intro`

Zoomlevel
---------

We're all very used to zooming into an online map. If you want more detail you just zoom in and if you want to get a bigger picture you zoom out. Each time you zoom, the map is rendered to show different things. When looking at a map at world scale, you don't see individual cities, when looking at an entire city you won't see individual buildings. You don't really have to think about this.

When building a static map in 3ds Max you have to design the map with a certain zoomlevel in mind. If you make a global map, you can pick a low zoomlevel such as 3 or 4. If you build a map of a few streets you'll need more detail and a higher zoomlevel such as 17 or 18. Read more here: :ref:`raster-zoom`