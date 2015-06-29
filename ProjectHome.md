# Introduction #
This library is an extension for jQuery to rotate images directly within JavaScript. Good in situations where you want to organize your thumbnails without the lag of synchronous image operations via the web server.

# Implementation #
Two JavaScript image handling implementations are supported:
  1. using DXImageTransform filter for Microsoft Internet Explorer
  1. using Canvas object for other browsers

The library has been tested with:
  * Mozilla FireFox 2.0.0.2
  * Internet Explorer 7.0
  * Opera 9.1 (**note** Opera 8 is not supported)

# Functions #
```
.rotate(angle,[whence=relative])

.rotateLeft([angle=90])

.rotateRight([angle=90])
```

# Guide #
The library should be loaded after the `jquery.js`. Once the library is loaded, you can rotate images by calling `rotateLeft([angle=90])` or `rotateRight([angle=90])` on the jQuery object, like this:
```
$('#theimage').rotateLeft();
```
From version 1.1, this library also supports arbitrary angles, in degrees:
```
$('#theimage').rotateRight(45);
```

# Notes #
  * Safari is not yet supported, but according to the specs it should work. Any help on this would be appreciated.
  * As the old image gets replaced with each rotation, none of its onXXX events are copied either.
  * Internet Explorer also rotates the border around an image, the other browsers don't