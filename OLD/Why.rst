Why
===

I'm a pretty clever programmer, sometimes. 90% of my time I'm dealing with boilerplate code, finding bugs or making cups of tea. Most of all I'm trying to remember whether I have written some code before and where to find it. It could be something very specific I've encountered maybe once earlier, or it could be a common pattern refined over the years and which I'm using all the time.
My memory serves me bad and often I end up trying to reinvent the wheel or reusing an outdated version of a common solution. That's why I started writing Shred. Shred helps me organize and store bits of maxscript code outside of their project context. I use it to store pieces of functions, intricate algorithms or beautiful code I've found on forums for which I don't have a specific use yet. I call these bits of code "shreds".

Always up to date
-----------------

A big advantage of storing shreds outside of their context of actual projects, is there's one place to find and maintain common pieces of code. I write code for gui's all the time and share lots of this code among projects. I also improve this code with every project I do (I hope). When I start a new project I go to the most recent project I've finished and copy most of it to my new one. This can get very messy and it's impossible to keep track of where the "most recent" version of a piece of code resides.
Once I've put such code in Shred, I can come back to it and add improvements to it and also update the metadata. This helps me maintain my "best practices" and actually find them when I need.

Libraries
---------

An alternative to this approach is to use script libraries. A library might contain all math related functions I've made for instance. When I need some math in my script I just copy this library and use the function I need. For each type of code or pattern I use I'd have a library.
Libraries also are a great way to maintain common code in a single place. So in a way it's similar to Shred. A downside is that if I need a single math function from my library, I have to package the entire library with my script. Maxscript libraries aren't huge, but still, it feels redundant. Another downside is that libraries can grow pretty big. I'm more used to having multiple smaller files in a project than one big. But that's just personal preference.

Hybrid
------

Actually, all my script projects use libraries and some of these are exactly the same for each project. But what I do is to trim down my libraries for each project to only contain the functions which are actually used. Shred helps me with this tremendously.