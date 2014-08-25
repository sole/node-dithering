# node-dithering

available algorithms:

* Bayer
* Closest
* Floyd-Steinberg

All of them using this method signature:

````javascript
function(inPixels, width, height, palette)
````
where

* `inPixels` is an array of rgb values - three values per pixel
* `width` and `height` define the size of the image
* `palette` is the desired output palette - and array of hexadecimal colour values. eg. `[ 0xff0000, 0x000000 ]` would be red and black

Return is an unsigned byte ArrayBuffer with the indexed output values in consecutive pixels, i.e. indices from the colour palette (hence these values are from 0..255 and the palette can hold a maximum of 256 colours, so that's why the unsigned byte type).

This is deliberately raw and unpacked for speed reasons.

## warning

this is under development so expect BOMBS to fall all around you. alternatively your script might hang. boom!
