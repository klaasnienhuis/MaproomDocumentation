.. _measure-path:

Measure path
============

Measuring distances on a map seems easy and straightforward. Just put a ruler on the map (or in 3ds Max: a tape measure helper) and read the length. The contrary is actually true. Since a flat map is an unwrapped sphere, taking two points on that flat map and getting the distance between them doesn't tell you a whole lot. That's because the flat map is quite distorted in several ways.

The shortest distance between two points on earth lies on the Great Circle between those points. It's easiest to visualize a great circle as a circle on the globe where the center of the circle passes through the center of the earth. A great circle is a straight line on the globe, but it usually isn't on a flat map. this also depends on the map projection.

There are also plenty of map projections where seemingly equal distances between points are actually different. In a mercator projection (used by most online maps) measuring the same distance on a flat map at the equator and at a higher latitude gives you different great circle distances.

.. figure:: ..\_images\Mercator_measurement.jpg

The same length on the map gives wildly different distances on the globe

But it works in Google Maps
---------------------------

You can easily measure distances in google maps. Just rightlick on a map and pick ``Measure distance``. It will give you accurte, real world distances. Nothing of that projection mumbo jumbo. Why can google make this work and 3dsMax not? Actually, when measuring the distances in google map, the actual distance on the map isn't measured. In the background your line on the map is converted to a great circle and calculated on the fly. 

Measure great circle distances
------------------------------

To reliably measure distances you should use the ``Measure Path`` map layer. This map layer gives you the length of the shape used to measure. By default it comes with a shape but you can replace it with your own shape. When pressing the ``Update lengths`` button, Maproom will calculate the length of the shape. You can use a shape with any number of points and the shape can be curved or straight. 

Use your own
------------

By default this map layer come with a shape called ``measure path``. It is a child of the map helper. If you want to use your own measure path, you can unlink or delete the default shape and link your own shape.

Example: Champs-Elysees
-----------------------

The Champs-Elysees is nice and straght. When measured in google it's about 2.13 km long. Let's try to get that measurement in 3dsMax with Maproom as well.

.. figure:: ..\_images\MPR_2016-06-28_2079.png

The Champs-Elysees is 2.13 km long

Make a new satellite map layer and center it around the Champs-Elysees in Paris. After building the map add a new ``Measure path`` layer. Draw a line along the Champs-Elysees and add that line as a child to the map helper of the ``Measure path`` layer (get rid of the original child line). In Maproom press ``Update lengths``. You'll see the length on the globe is about 2.13 km but the length on the map is about 3.22 km. That's exactly the same length of the line when you look it up with the native 3dsMax measure utility.

.. figure:: ..\_images\MPR_2016-06-28_2080.png

The Champs-Elysees in Maproom

.. figure:: ..\_images\MPR_2016-06-28_2081.png

Using the ``Measure path`` tool we can measure the line. It's 2.12 km on the globe (or in real world) but it's 3.22 km on the map.

.. figure:: ..\_images\MPR_2016-06-28_2082.png

With the 3dsMax measure tool we see the line is also 3.22 km. 

Now make exactly the same map but switch the map projection to UTM. Also add a ``Measure path`` map layer and measure the Champs-Elysees. Again you should see the same length on the globe, about 2.13 km. But now the length on the map is about the same. This means that for smaller areas, the UTM map projection gives very accurate results. This should be the projection of choice when working with maps and CAD data for instance.

.. figure:: ..\_images\MPR_2016-06-28_2083.png

The Champs-Elysees in Maproom, in utm projection

.. figure:: ..\_images\MPR_2016-06-28_2084.png

Using the ``Measure path`` tool we can measure the line. It's 2.12 km on the globe (or in real world) and it's the same on the map.
