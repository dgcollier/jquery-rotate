# Introduction #

The jquery-rotate library uses two mechanisms to enable rotation of images inside a web page without using Flash or Java:
  * Internet Explorer can use a propriety CSS option called `filter`
  * Other browsers rely on the Canvas object within JavaScript

# Functions #
## rotate() ##
`rotate(angle,[whence=rel])`

The main function of this library. It allows you to set an angle and whether the change is relative or absolute.

### Arguments ###
  * angle - the rotation angle, in degrees.
  * whence - optional; when given, the angle is set to an absolute value given by `angle`

### Examples ###
  * To revert back to the original state, call `rotate(0,'abs')`
  * To rotate 90 degrees anti-clockwise, call `rotate(-90)`
  * To rotate 90 degrees clockwise, no matter the previous state, call `rotate(90,'abs')`

## rotateLeft() ##
`rotateLeft([angle=90])`

An alias for `rotate(-90)`. Rotates the image anti-clockwise.

## rotateRight() ##
`rotateRight([angle=90])`

An alias for `rotate(90)`. Rotates the image clockwise.
