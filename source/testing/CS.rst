Testing .NET
============

Most of the heavy lifting is done by .net libraries. These can be tested independently from 3dsMax. These tests operate with a commandline tool and generate a text-file with the test results. After the tests have run, which might take a minute or two, please send this text-file to mail@klaasnienhuis.nl.

Download the testfiles here `dotnet test files <https://www.dropbox.com/sh/z25tbqrmmrg7obq/AAAFIaefGu0_9o1sLqGb4LKAa?dl=0>`_. Get the latest zip-file labeled with dotnet in the filename.

Test instructions
-----------------

Download the zipfile and unzip it somewhere on your computer. There are lots of files in there, but you just need to doubleclick the ``MSTestRunner.bat`` file. This will execute the tests and it will run for a couple of minutes. You don't need to open 3dsMax for these tests. Once it's done you'll see the following:

.. image:: ..\\_images\\MPR_2016-05-24_2030.png


In the same folder, get the file ``MaproomTestLog.txt`` and send it to mail@klaasnienhuis.nl

Manual check
------------

The tests (should) also create some images in your user folders. They should be about here: ``C:\Users\[username]\Documents\3dsMax\MaproomTest``. Please zip that entire folder and send it over too.




