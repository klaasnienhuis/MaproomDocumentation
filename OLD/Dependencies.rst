.. _rst_dependencies:

Dependencies
============

Shreds work best if they're atomic pieces of code: functions, math solutions, clever bits. Sometimes a group of these shreds depend on each other. It's possible to indicate these dependencies while still keeping the shreds separate. To do this, you can add dependency-tags to a shred. 

Dependency-tags
---------------

Assuming you have shred A with a clever bit of math and shred B which uses this. Add a tag "math" to shred A in the "Defines" field. In shred B you enter this same tag in the "Uses" field. From now on these shreds are linked with a dependency.
This example illustrates dependencies between 3 shreds. The first two shreds "define" something. The third shred "uses" these definitions. These dependency tags work just like ordinary tags and are comma separated. When you use a definition the script will automatically detect this and display this dependency, either by showing where a definition is used or where a definition comes from.

.. image:: \_images\Shred_2015-09-02_1553_cr.png

*A shred defines "fn_randomInt"*

.. image:: \_images\Shred_2015-09-02_1554_cr.png

*A second shred defines "fn_sqrt"*

.. image:: \_images\Shred_2015-09-02_1556_cr.png

*A third shred uses these definitions. Notice how the defining shreds are listed in the dropdown. Just click on them to open a defining shred.*

Evaluating
----------

You can evaluate code directly from within Shred. When code is setup with dependencies you can also evaluate these linked shreds as a whole. Shred will evaluate the defining shreds first and finally run the shred which uses these definitions. This enables you to set up your shreds even more granular or to include testing code in separate shreds for instance.

.. note:: Code is evaluated in the scope it's written in. If this is the global scope this might cause problems with running other scripts. Code in global scope also tends to "hang around".

.. image:: \_images\Shred_2015-09-02_1557.png

*Evaluate with dependencies runs all defining pieces of code first*

Navigating dependency tags
--------------------------

Just like ordinary tags you can navigate dependency tags. In the tags list, click on the "Show dependency tags" button from the Tags dropdown. This makes it a lot easier to find tags which use a particular definition for instance.

.. image:: \_images\Shred_2015-09-02_1558.png

*Isolate the dependency tags from the normal tags*

