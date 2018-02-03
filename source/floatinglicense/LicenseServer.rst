License server
==============

The license server is a small application. It can run on a separate machine on the network or on one of the clients. However, it needs to be always on to lease out licenses. The license server is started and stopped by command line. You need to run the command line as administrator. I've found that it also needs to run on a local disk, not a network share. There can be only one floating license server per network.

When you get a floating license, you receive a single product key similar to a node locked key. But in this case the single product key represents a number of floating licenses.

First you need to activate the license server with the product key. This means you authenticate yourself with me. Once the license server has been activated it can be started. From that moment on clients can lease licenses. There's no authentication between the client and the server. The client asks for a lease. If it's there, the server hands it over. No questions asked!

I've created a few convenient bat-files to operate the server. They require a few files to be present in the same folder as the bat-files:

* float_server.log
* LexFloat.config
* Product.dat
* productkey.txt

The config file allows you to configure a number of things. For instance the port number for the license server (8091 by default). ``productkey.txt`` should contain the product key of the floating license.

License server API
------------------

Once the license server is up and running, you can check its status and the number of leased licenses through a web api. The address is ``serverip:serverport/services/api/stats``. For example ``http://192.168.2.1:8091/services/api/stats`` if the license server runs on a machine with the ip address ``192.168.2.1`` and the port ``8091``.