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

.. image:: _images\MPR_2015-11-05_1719.png

*Put the repository somewhere where you've got the space*

.. _mapapikey:

Map API key
-----------

Some mapping API's require you to identify yourself with the use of an API key. This key is linked to your account with the respective map provider. Usually this means you have to make an account with Bing or Mapbox, find the API key in your account settings and paste it in here. Once you've got a good API key you can start using the maps from thse providers. Normally there's a free account available. Only when you start consuming a LOT of maps you'll be notified to get a paid plan. Map provider fees are not included in the Maproom licenses or subscription.

Currently the mapping keys are wiped when you update Maproom. Make sure you keep these keys handy in a password manager or something similar.


.. image:: _images\MPR_2015-11-05_1720.png

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

.. image:: _images\MPR_2016-03-02_1911.png

*Manage your stylesheets*

.. _license:

License
-------

By default Maproom comes with a free license. You're able to create good looking image based maps with the free version. If you'd like to build bigger maps and use terrain heights, openstreetmap, shapefiles and more you can purchase a pro license. The pro license is node locked. The license is tied to the PC you request the license from. During the beta you can request a beta license. 

.. raw:: html

		<iframe width="700" height="525" src="https://www.youtube.com/embed/rwlGYHwbu4E" frameborder="0" allowfullscreen></iframe>
		
*Get a free beta license*

Previously the license came to you as a file you'd have to install. The current system works with your email address and a plain text token. You get the token by email and you have to fill in the token and your email address in the corresponding fields in Maproom.

In the License tab of the Settings panel, enter your email address and press ``Request beta license``. The request is sent to the server and you'll get a confirmation email. I'm still manually verifying each request, so you won't get your license immediately. Don't request multiple license fromthe same machine, it makes no sense and it won't get you your license any faster.

.. image:: _images\MPR_2016-10-01_2133_cr1.png

*Send your license request from here*

.. image:: _images\MPR_2016-10-01_2138.png

*Your license request has been recieved*

.. image:: _images\MPR_2016-10-01_2139.png

*There's probably already a license in place for this machine. Please be patient while I process it.*

When you recieve the email with the credentials, you need to fill in your email and token. Press the "Edit" button next to the text field, paste the email and token and press the "OK" button.

.. image:: _images\MPR_2016-10-01_2135.png

*Press the little pencil icon to unlock the text field*

.. image:: _images\MPR_2016-10-01_2136.png

*Press the green checkmark to store your credentials*

Once you've filled in your credentials you need to restart Maproom for the new license to take effect.

Feature comparison
^^^^^^^^^^^^^^^^^^

The pro license will contain all features covered here in the documentation. During the beta some features might not be completely functional or temporarily disabled. These will be introduced gradually. The free license allows you to build maps with the Mapbox and OSMMapnik image sources. You can make maps of 1K size. Due to the nature of these maps you can zoom to any portion of the world though the maximum texturesize will be 1024x1024 pixels. The free license isn't able to generate terrain heights or process vector data such as openstreetmap or shapefiles.

.. _updating:

Updating
--------

The script checks for an update on a server every time it starts up. If there’s an update available, the script will notify you with a message in the home screen. If you press the message the Update panel will open. Here it says which release number you currently have and which release is available on the server. A small overview of the most important features of the update is also shown.

If there's an update available there's also a button available. Press it to download the update and start the installer. Follow the instructions under the :ref:`installation` chapter. However, you don’t need to customize the gui again. Just close the installer and script and reopen the script. It’s been updated now.

.. image:: _images\MPR_2016-01-25_1850.png

*An update is available, press the yellow button to open the update panel.*

.. image:: _images\MPR_2016-01-25_1851.png

*An overview of the available update. Press the button to install it.*

.. _sampledata:

Sample data
-----------

Maproom comes with sample data courtesy of their respective owners. Currently you can request three sample areas of CyberCity 3D buildings. Enter your email address and press the ``Request...`` button. A link to the data will be emailed to you together with a tutorial on how to work with it.

.. image:: _images\MPR_2016-12-09_2213.png

*Request sample data*

.. _units:

Units
-----

If your system units are set to small units, like meters or inches, making maps will cause issues in 3dsMax. A map of a city of 10*10 km measures about 400.000 inches. 3dsMax has difficulty showing large units like these accurately. I advise to use kilometers or miles when making maps. Maproom notifies you of this in the home screen and offers you shortcuts to change your system units. You can also do this manually. Keep in mind you need to change the **system** units, not the **display** units.

.. image:: _images\MPR_2016-02-01_1858.png

*A notification in the home screen helps you quickly change your system units*

Changing the system units manually is also possible. Go to the *Menu > Customize > Units setup...* Then press the *System Unit Setup* button. In the popup pick the system unit scale you want to use. I recommend Kilometers or Miles.

.. image:: _images\MPR_2016-02-01_1859.png

*Got to the Customize menu*

.. image:: _images\MPR_2016-02-01_1860.png

*Open the System Units Setup*

.. image:: _images\MPR_2016-02-01_1861.png

*Pick a system unit scale appropriate to making topographic maps*