---
layout: page
title: "The Designer's Guide to Web Development"
group: resources
---

ADE’s designs should look and feel as great on the web as they do in InDesign. That job belongs ultimately to the developers, but you can help them tremendously by following these guidelines in your designs.


Work in pixels.
---------------

Pixels are the units of the web. If you’re working in inches, points, or picas, the developers are going to have to translate your work into pixels, and they will probably get it wrong.


Know your platform.
-------------------

What kind of site are you designing? Is it a Tumblr, a store on Shopify, or a mobile web app app? 

Each platform has unique strengths and limits.

Find about five sites running on the platform you're targeting, and notice what they all do. More importantly, notice what they don't do. If you can't find an example site that does Thing X, it may be because Thing X is impossible to do on that platform.

If you have questions about the limits of a platform, ask! The developers will be happy to help.


Design on a grid.
-----------------

Grid-based design isn't the answer for every project, but if you're not designing on a grid, you may be doubling our development time. Please only do this on purpose.

Twitter's grid system, Bootstrap, is a great place to start. Learn about it here:

http://twitter.github.com/bootstrap


Specify everything.
-------------------

The more specific you can be when sending a project into development, the better. Try to hit everything on this list:

- Declare all font families, weights, styles, line heights, and sizes in pixels.
- Declare the column-width and gutter-width of your grid in pixels. Also tell us how many columns you used. Or, better, just use Bootstrap's grid.
- Declare all colors as hex values, e.g. #ff00cc. RGB is okay too, but do not use CMYK.
- Show hover and click states for all interactive elements.
- Package everything into a ZIP file. "Everything" means all graphics as separate PNGs or JPGs, all font files as OTF or TTF files, a text file with your notes, the PDF you used to present your design to the client, and a PNG or JPG of your design, rendered at scale. You can include an InDesign file if you want, but remember that most developers don't know how to use InDesign.


Design for several sizes.
-------------------------

It isn't a website until it looks right on iPhone, iPad, a 13" laptop, and a 27" iMac. Maybe your one design works well everywhere, like Apple's website. Maybe you'll end up making different versions for different screen sizes.

If your design changes on different screens, **design for a phone first.** It's easier to add features on a larger screen than to remove them on smaller ones.


Learn CSS.
----------

You ought to be able to answer this question for each element of your design:

*How hard is it to make this in CSS?*

CSS is the language developers use to style websites. The more you understand about how it works, the more informed your choices will be about drop shadows, opacity, transitions, borders, and, well, everything.

Here's a good place to get started:

http://www.w3schools.com/css/



Think about speed.
------------------

Every element of your design has to be transferred from a server to the user. Every image, video, and even every nonstandard font makes the page load more slowly. 

This doesn't mean you shouldn't use images and videos. Just rembember that visitors to the site will start trying to click around *before* the page has finished loading. Will the site feel broken if they do?

For extremely image-heavy sites, it's a good idea to make snapshots of three states: (i) barely loaded, (ii) half-loaded, and (iii) loaded. 

Sites by ADE should feel expensive as soon as they start loading.