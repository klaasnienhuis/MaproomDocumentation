Shred
=====

A shred is a piece of code with metadata. The metadata makes it easier to keep a bunch of shreds and find what you’re looking for. To display a shred, click an item from the middle column. This will load up the shred in the right panel.

Storing
-------
A shred consists of two pieces which are stored independently. The code itself is stored in a .ms script file. The metadata is stored in an xml file. Metadata contains a title, a description, tags and a weblink. Each metadata field is optional, but the more you fill in the easier it becomes to use.

Creating a new Shred
--------------------
When I want to store a new shred, I press on the "New shred" button, fill in the metadata fields and paste in the code. Finally I press the "Commit" button and the shred is stored, ready for browsing.
At the moment the way the code is shown in Shred is pretty crappy: no color highlighting and insane tab spacing. I can edit the code in Shred but it's easier to make the piece of code just right in a maxscript window before you shred it. 

Use the code
------------
You can either copy the code with one of the “Copy” buttons in the toolbar or evaluate the code directly from within shred. Press the “Evaluate shred” button from the “Evaluate” dropdown on the toolbar. This will execute the code directly without having to place it in a new script first. You can also evaluate with dependencies. More on :ref:`rst_dependencies` here.

Copy code
^^^^^^^^^
There are three ways to copy code

* **Copy alone** copies the individual shred
* **Copy with dependencies** copies the shred and all dependencies used in it
* **Copy with dependencies as struct** copies the shred and all dependencies used in it formatted as a struct. 

Copying as a struct only makes sense if the dependent scripts will actually work in a scruct. This is nice when you have a bunch of functions you always bundle in a struct but still want to keep in separate shreds.

Three dependent functions are copied as such::

	fn fn_randomInt = random 0 25

	fn fn_sqrt a = sqrt a

	fn compoundMathFunction = 
	(
		myValue = fn_randomInt()
		mySqrt = fn_sqrt myValue
		format "start: % end: %\n" myValue mySqrt
	)

When copied as a struct they look like this::

	struct struct_name
	(
		fn fn_randomInt = random 0 25,

		fn fn_sqrt a = sqrt a,

		fn compoundMathFunction = 
		(
			myValue = fn_randomInt()
			mySqrt = fn_sqrt myValue
			format "start: % end: %\n" myValue mySqrt
		)
	)

Metadata
--------
To make it easier to find stuff back you should enter the available metadata fields: title, description, tags and reference. Title and description speak for themselves. Tags have to be comma separated. Each unique tag will end up in the tag list on the left. You can filter shreds by selecting one or more tags. the reference field can be used to store a link to a website or blog where you’ve found a solution for instance.

.. _shred-search:

Search
------
As an extra option it's possible to search the shreds for a specific string. When searching, the code of each shred is checked and matching shreds are listed. I don't know yet how this performs when my library of shreds grows, but for now it works great. Use this when looking for shreds with a specific maxscript function in it for instance.

.. image:: \_images\Search.gif

*Searching will show all shreds with the search term in the code*

