Settings
========

.. _repository:

Repository
----------

Maproom uses map data from outside sources. This data is cached to make editing your maps more responsive. The repository distinguishes between a cache and a session. 

A cache contains the raw data downloaded from a provider **if** it's reusable. Currently this covers the raster tiles, such as tiles from mapbox and mapquest and height data mapbox and mapzen. A separate cache is built for each tile provider and zoomlevel. If I make a map based on the same tiles (location, provider and zoomlevel) twice, tiles aren't downloaded but taken from the cache. This improves speed a lot.

A session is a location where sources are stored for each map created which can't be recycled. when creating a map based on raster tiles, these tiles are downloaded or taken from the cache and stiched into a single map image. The tiles can be reused in other maps, but this stiched image probably can't. That image is stored in a session folder in the repository. This also applies to openstreetmap data. It's currently not feasible to use a cached version. Each new openstreetmap layer means a new chunk of data is downloaded.

Since the amount of data you're downloading and caching can get quite large, put the repo where you've got the space.

.. note:: Content provided through the Maproom script is copyrighted by the respective owner. Check out the copyright, license and attribution conditions for each of these sources. The creator of this script does not claim ownership and can't provide a license for this content.

.. image:: _images\\MPR_2015-11-05_1719.png

*Put the repository somewhere where you've got the space*

.. _mapapikey:

Map API key
-----------

Some mapping API's require you to identify yourself with the use of an API key. This key is linked to your account with the respective map provider. Usually this means you have to make an account with Bing or Mapbox, find the API key in your account settings and paste it in here. Once you've got a good API key you can start using the maps from thse providers. Normally there's a free account available. Only when you start consuming a LOT of maps you'll be notified to get a paid plan. Map provider fees are not included in the Maproom licenses or subscription.

Currently the mapping keys are wiped when you update Maproom. Make sure you keep these keys handy in a password manager or something similar.


.. image:: _images\\MPR_2015-11-05_1720.png

*Enter your map API keys*

Mapbox
^^^^^^

To create a Mapbox access token, you first need to sign up for a mapbox account. You can do that `here <https://www.mapbox.com/signup/>`_. Then you can create an access token. You enter this access token in Maproom to link your mapbox data usage to your account. `More about the access token <https://www.mapbox.com/help/define-access-token/>`_

.. raw:: html

		<iframe width="700" height="525" src="https://www.youtube.com/embed/W4q_fnOWcCg" frameborder="0" allowfullscreen></iframe>
		
*Create a Mapbox token*

Bing
^^^^

The same procedure applies to Bing. `Sign in <https://www.bingmapsportal.com/>`_ to the Bing Maps Dev Center with an existing Microsoft account or create a new one. `More on the Bing Maps key here <http://www.microsoft.com/maps/create-a-bing-maps-key.aspx>`_. A basic key will be enough at first! Keep in mind Bing maps are not available in the free version.

.. raw:: html

		<iframe width="700" height="525" src="https://www.youtube.com/embed/WkiOgQhlwMw" frameborder="0" allowfullscreen></iframe>

*Create a Bing maps key*

.. _settings-stylesheets:

Stylesheets
-----------

Stylesheets are .ini files used to convert shapes into geometry based on a set of rules. Maproom comes with a production ready stylesheet and a few samples for demonstration purposes. You can make copies and modify them or start from scratch to make styles which fit your needs. There are two locations Maproom looks in to find stylesheets: the system location and the user location. The system location is fixed and sits in the Maproom installation folder. The user location is located in the map data cache folder by default but can be changed. More about working with stylesheets here: :ref:`stylesheet`

.. note:: When modifying stylesheets or creating new ones you should do that in the user location. The system stylesheet location will be reset every time you install an update.

.. image:: _images\\MPR_2016-03-02_1911.png

*Manage your stylesheets*

.. _license:

License
-------

By default Maproom comes with a free license. You're able to create good looking image based maps with the free version. If you'd like to build bigger maps and use terrain heights, openstreetmap, shapefiles and more you can purchase a pro license. You can purchase a pro license in `the shop. <https://www.klaasnienhuis.nl/product/maproom/>`_

.. raw:: html

		<iframe width="700" height="525" src="https://www.youtube.com/embed/rwlGYHwbu4E" frameborder="0" allowfullscreen></iframe>
		
*Get a free license*

Starting with Maproom 70 you can access your license through an online portal. You can for instance see if your license has been activated and deactivate it yourself. The portal can be found here: https://klaasnienhuis.cryptlex.app. Use your email address and a fresh password to gain access.

Node locked
^^^^^^^^^^^

You can purchase node locked licenses in the shop. Each license can be used on one PC at a time. The system works with your email address and a plain text product key. You get the product key by email after the purchase has been processed. In the License tab of the Settings panel paste your product key. Press the ``Activate product key...`` button. This will activate your pro license and tie it to the PC you're working on. You'll need to restart Maproom for the new key to take effect.

If you buy multiple keys in one go, you get multiple product keys. You can activate each key on a different machine.

.. image:: _images\\2021-04-13_213927.png

*Open the license panel in the settings. By default it shows the node locked license options*

After activating your product key, it's locked to this machine. Please restart Maproom for the licnese changes to take effect.

You can also deactivate a product key. This means that you make the product key available to use on another machine. Press the ``decativate product key`` button. Once you do that, you're auotmatically switched to the free plan. Deactivating a license is convenient when you switch to a new PC for instance. The number of deactivations is limited per product key.

Floating license
^^^^^^^^^^^^^^^^

It's possible to purchase a floating license for bulk orders. For example if you want to use Maproom in a teaching environment or a large studio with many seats. A floating license doesn't add extra functionality.

A floating license works with a hosted license server. A single floating license can contain multiple seats. A user of maproom enters the product key as described above and activates it. This leases a single seat from the license. Closing maproom releases that seat. 

If for instance you have purchased 10 licenses, the server can hand out leases to 10 clients. If the 11th client requests a lease from the server, it's denied. The number of clients on the network is infinite but only 10 of these clients can lease a license at the same time. All other clients operate with a free license.

A floating license can't be purchased from the shop yet. Get in touch with me at mail-at-klaasnienhuis.nl to set it up.

Feature comparison
^^^^^^^^^^^^^^^^^^

The pro license will contain all features covered here in the documentation. The free license allows you to build maps with the Mapbox and OSMMapnik image sources. You can make maps of 1K size. Due to the nature of these maps you can zoom to any portion of the world though the maximum texturesize will be 2048*2048 pixels. The free license isn't able to generate terrain heights or process vector data such as openstreetmap or shapefiles. an exception are the Demo presets which are also available in Maproom Free: :ref:`preset-demo`.

.. _updating:

Updating
--------

The script checks for an update on a server every time it starts up. If there’s an update available, the script will notify you with a message in the home screen. If you press the message the Update panel will open. Here it says which release number you currently have and which release is available on the server. A small overview of the most important features of the update is also shown.

If there's an update available there's also a button available. Press it to download the update and start the installer. Follow the instructions under the :ref:`installation` chapter. However, you don’t need to customize the gui again. Just close the installer and script and reopen the script. It’s been updated now.

.. image:: _images\\MPR_2016-01-25_1850.png

*An update is available, press the yellow button to open the update panel.*

.. image:: _images\\MPR_2016-01-25_1851.png

*An overview of the available update. Press the button to install it.*

.. _sampledata:

Sample data
-----------

Maproom comes with sample data courtesy of their respective owners. Currently you can request three sample areas of CyberCity 3D buildings. Enter your email address and press the ``Request...`` button. A link to the data will be emailed to you together with a tutorial on how to work with it.

.. image:: _images\\MPR_2016-12-09_2213.png

*Request sample data*

.. _imagesource:

Image source
------------

Image sources are the places where Maproom gets its satellite images and other map textures from. Maproom has built in image sources, such as Bing, Mapbox and Stamen. But there are a lot more image providers out there. The User Image sources section enables you to set up your own custom sources.

An image source provides its images through a specific url template. This url template is used to download the map textures at any zoomlevel and from any location. Usually image providers follow a common pattern, we'll leverage that. These patterns contains a few symbols. Here's an example:

``http://api.tiles.mapbox.com/v4/{mapid}/{zoomlevel}/{tilex}/{tiley}.png?access_token={token}``

The first part ``http://api.tiles.mapbox.com/v4/`` points to the Mapbox server. Then we have the symbols

- ``{mapid}`` this is usually the type of map. For instance the Bing satellite maps has as mapid "Aerial" and the Stamen watercolor map has "watercolor". Sometimes you need to provide this, other times it can be left out.
- ``{zoomlevel}`` this determines the zoomlevel of the images you're downloading. Every url needs this symbol.
- ``{tilex}`` and ``{tiley}`` these are the tile coordinates being downloaded. Every url needs this symbol.
- ``{token}`` some map providers require an access token. Others don't. Usually you can get an access token when you set up an account with the map provider.

Image providers all use similar url's

- ``http://sat.owm.io/sql/{zoomlevel}/{tilex}/{tiley}?appid={token}&op=rgb&from=s2&select=b4,b3,b2``
- ``http://a.sm.mapstack.stamen.com/($d9da8e[@p],(mapbox-water,$60c9fe[source-in]))/{zoomlevel}/{tilex}/{tiley}.png``
- ``https://maps1.aerisapi.com/{token}/{mapid}/{zoomlevel}/{tilex}/{tiley}/current.png``

Sometimes the order of the symbols is different. Sometimes you don't need a token or a mapid. You don't need to guess these url's. Every map provider can tell you how these url's should look. And when you create a new image source, Maproom offers a few examples.

.. warning:: Even though it's technically possible to add a certain image source, this doesn't mean you're allowed to. ArcGis for instance has beautiful image sources, easily accessible. But it's only allowed to use them in software by ESRI. Google maps would also be pretty cool to use, however you'll have to pay a hefty license fee to do so. Always keep the terms and conditions in mind. 

Working with image sources
^^^^^^^^^^^^^^^^^^^^^^^^^^

Go to Settings > Image sources. There you see a dropdown with the custom image sources. Use the ``New``, ``Delete`` and ``Clone`` buttons to create or delete an image source. Use the ``Test`` button to test it once you've created one. The test will tell you if the image source has been set up properly. Only when you pass this test you can actually use the image source in your maps. Give your image source a proper name and make sure it's unique. Fill in the url template, optionally the map id and token and the zoom limits. Make sure you add the attribution required by the map provider.

.. image:: _images\\SPH_2018-02-03_2855.png

*A user image source setup from AerisWeather. Note the blurred out token. This provider needs you to make an account*

.. note:: Content provided through the Maproom script is copyrighted by the respective owner. Check out the copyright, license and attribution conditions for each of these sources. The creator of this script does not claim ownership and can't provide a license for this content.

Examples
^^^^^^^^

.. image:: _images\\reprojected_2cedb620-e778-4e6f-82e3-b2b669f77e55.png

*Temperature forecast from AerisWeather*

.. image:: _images\\reprojected_8964b459-545a-406d-ac6e-e4609c7e64f5.png

*Blue Marble from AerisWeather*

.. image:: _images\\reprojected_70212652-2228-4a4d-a8d3-743fb872e57e.png

*Clouds from AerisWeather*

.. image:: _images\\SPH_2018-02-03_2860.png

*Clouds and Blue marble combined*

.. image:: _images\\reprojected_d49c0b98-c4ca-415a-892e-770140108e9c.png

*A style from Mapstack by Stamen*

.. image:: _images\\reprojected_e2e9e11a-8e98-4c1d-bd25-198220841041.png

*Another style from Mapstack by Stamen*

Mapstack Tutorial
^^^^^^^^^^^^^^^^^

Here's how to get the correct url from Mapstack. First go to `mapstack.stamen.com <http://mapstack.stamen.com/>`_ and then press the "Try it" button. Fiddle with the map layers and settings. It's best just to try it for a bit and create a style you like. Once you're satisfied, in the map on the right side of the screen, rightclick and press ``View image`` from the dropdown. Copy the url of that image.

.. image:: _images\\SPH_2018-02-04_2861.png

*A style from Mapstack by Stamen*

Then in Maproom, create a new image source and use the Mapstack template. The Mapstack template already comes with a url. We just need to replace the part which determines the look of the map. This is the url of the Mapstack template

``http://a.sm.mapstack.stamen.com/($9a9a30[@p],(mapbox-water,$60c9fe[source-in]))/{zoomlevel}/{tilex}/{tiley}.png``. We need to replace the middle part ``($9a9a30[@p],(mapbox-water,$60c9fe[source-in]))`` with the middle part of the url you just copied. Also make sure to copy the attribution you see in the bottom right of the map. An example of this is

	
    Tiles by MapBox, Data © OpenStreetMap contributors
    Tiles by Stamen Design, under CC-BY 3.0. Data © OpenStreetMap contributors, under CC-BY-SA.

Where to get these
^^^^^^^^^^^^^^^^^^

There are many places you can get access to custom styles. Some of these are freely accessible, for others you need a free token, others are commercial.

- `Mabbox studio <https://www.mapbox.com/mapbox-studio>`_
- `AerisWeather <https://www.aerisweather.com/support/docs/aeris-maps/reference/map-layers/>`_
- `Openweathermap <http://openweathermap.org/api/weathermaps>`_
- `Vane <http://owm.io/sql-viewer?lat=38.87&lon=-121.47&zoom=10&select=red,green,blue&op=rgb&from=cloudless>`_
- `Mapstack <http://mapstack.stamen.com/>`_
- `Thunderforest <http://www.thunderforest.com>`_
- `Here <https://developer.here.com/documentation/map-tile/topics/overview.html>`_
- `Planet <https://www.planet.com/>`_
- `DigitalGlobe <https://www.digitalglobe.com/products/digitalglobe-basemap>`_


.. _units:

Units
-----

If your system units are set to small units, like meters or inches, making maps will cause issues in 3dsMax. A map of a city of 10*10 km measures about 400.000 inches. 3dsMax has difficulty showing large units like these accurately. I advise to use kilometers or miles when making maps. Maproom notifies you of this in the home screen and offers you shortcuts to change your system units. You can also do this manually. Keep in mind you need to change the **system** units, not the **display** units.

.. image:: _images\\MPR_2016-02-01_1858.png

*A notification in the home screen helps you quickly change your system units*

Changing the system units manually is also possible. Go to the *Menu > Customize > Units setup...* Then press the *System Unit Setup* button. In the popup pick the system unit scale you want to use. I recommend Kilometers or Miles.

.. image:: _images\\MPR_2016-02-01_1859.png

*Got to the Customize menu*

.. image:: _images\\MPR_2016-02-01_1860.png

*Open the System Units Setup*

.. image:: _images\\MPR_2016-02-01_1861.png

*Pick a system unit scale appropriate to making topographic maps*