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

Return is an unsigned byte arraybuffer with the output values in consecutive r, g, b bytes per pixel.

This is deliberately raw and unpacked for speed reasons.

## warning

this is under development so expect BOMBS to fall all around you. alternatively your script might hang. boom!
