# Sinatra base application

Features:

* Sets up Sass to try load & include Compass and Bourbon
* Mounts middleware that handles Sass & CoffeeScript compilation and HTTP cache
  headers
* Sass output set to compressed in production
* JS files concatenated & minified in production

You might want to:

* Pick either Compass or Bourbon and remove the other from bundle
* Remove Haml from bundle if not using it
