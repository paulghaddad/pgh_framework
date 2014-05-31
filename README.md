pgh_framework
=============

## Purpose

This is my personal framework for building websites.  It allows me to start each project with a custom Gruntfile, SASS file structure and custom CSS grid.

## How it was built

The framework is a fork of HTML5 Boilerplate, but I have modified all the files significantly:

* Bower is used to import any necessary packages, such as jQuery or Respond.js
* Respond.js is used for media queries in Internet Explorer 8. A Modernizr function is written at the end of the HTML file that conditionally loads it.
* The SASS files are separated into many directories, such as base, components, and layout, among others. Each partial SASS file is then imported in the _imports.scss file, which is in turn imported into the styles.scss file.
* Grunt is used to compile the styles.scss file into an unprefixed css file. The Grunt autoprefixer plugin then adds any necessary prefixes for the build version. Grunt also concatenates and minimizes javascript from the working file, main.js, to the production files in the build subdirectory. Finally, I have Grunt plugins to minimize images, watch and automatically run certain tasks, and to run a local server.
* Modernizr to check for certain browser features, and then using the yep-nope library, conditionally load respond.js and polyfills.
* Adobe Typekit Fonts are loaded asynchronously.
* A custom grid that is responsive, starting mobile first.