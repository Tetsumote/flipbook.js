# flipbook.js

Scroll-based inline flipbook animation for the internet. Checkout the [demo](https://russellgoldenberg.github.io/flipbook.js).


## Installation

``` npm install flipbook```

or 

``` <script src="flipbook.min.js"></script> ```



## Usage

``` html
	<div id='walk-cycle'></div>

	<script>
		// instantiate the flipbook
		flipbook({
			id: 'walk-cycle',
			path: 'frames/walk',
			extension: 'jpg',
			frames: 86,
			speed: 0.5
		});
	</script>
```

## Options
* **id** (required)
	The id of the element where the flipbook will be inserted

* **path** (required)
	The relative path the directory where the images are

* **extension** (required)
	The type of image file *(png or jpg)*

* **frames** (required)
	Number of images in directory

* **speed** (optional)
	[0 to 1] How fast the scroll advances the frames (0: slow, 1: fast)

* **cover** (option)
	[True or false] If the flipbook should go full window height, and center-crop (like CSS's `background-size: cover`)


### Helpful bits
Convert a video to image sequnce with ffmpeg:

```ffmpeg -i input.mp4 -r 12 frames/%d.png ```


## License & Credit

MIT © [Russell Goldenberg](http://russellgoldenberg.com)

Inspired by [canvid](https://github.com/gka/canvid/blob/master/canvid.js) and [stack](https://github.com/mbostock/stack)
