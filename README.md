# Phroper - Image uploader and cropper. #

## Setup ##
You will only need to declare some dependencies: jQuery, cropper and phroper.
```html
<link rel="stylesheet" href="styles/cropper-jquery-2.3.0.mins.css" />
<link rel="stylesheet" href="styles/phroper.css" />

<script type="text/javascript" src="http://code.jquery.com/jquery-2.2.3.min.js" ></script>
<script type="text/javascript" src="scripts/cropper-jquery-2.3.0.mins.js" ></script>	
<script type="text/javascript" src="scripts/phroper.js" ></script>
```
After this you just need to declare an anchor div to place phroper.
```html
<div id="photo-uploader"></div>
```

## Usage & API ##
Phroper is very simple and straighforward. As of version 2.1.0 it offers you 6 functions.

1. **`testEnvironment()`** - returns `True` or `False` regarding the browser's ability to run Phroper or not.

2. **`start(showThumbnail, width, height, captions)`** - it loads and initializes phroper.   
`showThumbnail` indicates if you want to display a tiny thumbnail showing the cropped area.   
`width` passes the desired width in pixels for Phroper's stage.   
`height` _idem_ for height.   
`captions` is an optional array containing the labels used by Phroper.
	```javascript
	captions[0] = 'Drag your lovely picture here';
	captions[1] = 'Or, if you prefer...';
	captions[2] = 'Select it from your computer.';
	captions[3] = 'Loading picture...';
	```

3. **`getPicture(mode)`** - returns the cropping in `base64` format or, if mode is set to `'file'`, as a HTML5 [Blob](https://developer.mozilla.org/en/docs/Web/API/Blob).

4. **`getThumbnail(mode)`** - same as the previous function but applied to the thumbnail.

5. **`reset()`** - clears Phroper's stage.

6. **`hasLoadedPicture()`** - returns `True` if Phroper's stage is in use or `False` otherwise.

## Credits & Dependencies ##
Phroper used to have its own cropper implementation using [fabric.js](http://fabricjs.com/) as a HTML5 Canvas abstraction.   
Since its 2.0.0 version it has been using this great [cropper](https://github.com/fengyuanchen/cropper), developed by **Fengyuan Chen**.

You will need a HTML5 capable browser to run Phroper (Canvas & FileReader) as well as having an updated jQuery version running.