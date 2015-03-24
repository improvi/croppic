see full documentation at http://www.croppic.net/

works in IE 10+, chrome, firefox, safari and opera.

Added below options:

**Added checkFileSize option**

Ex.
````
var croppicContainerModalOptions = {
		uploadUrl:'img_save_to_file.php',
		cropUrl:'img_crop_to_file.php',
		modal:true,
		imgEyecandyOpacity:0.4,
		loaderHtml:'<div class="loader bubblingG"><span id="bubblingG_1"></span><span id="bubblingG_2"></span><span id="bubblingG_3"></span></div> ',
		,checkFileSize: function (origFileSize) {
			if(origFileSize > 500000) // greater than 5MB
			{
				alert("The uploaded file is too big. The maximum accepted file size is 5MB.");
				return false;
			}
			return true;
		}
}
````

You can now pass a function to the checkFileSize parameter with one variable which is the size of the uploaded file.

**Added Progress bar options**

Option progressBar => a jQuery element of the actual progress bar where the width is set based on the uploaded status
Option progressBarContainer => a jQuery element, this is hidden when the progressBar reaches 100%

Ex.
````
var croppicContainerModalOptions = {
		uploadUrl:'img_save_to_file.php',
		cropUrl:'img_crop_to_file.php',
		modal:true,
		imgEyecandyOpacity:0.4,
		loaderHtml:'<div class="loader bubblingG"><span id="bubblingG_1"></span><span id="bubblingG_2"></span><span id="bubblingG_3"></span></div> ',
		progressBar: $('#progressBar1 .progress-bar'),
		progressBarContainer: $('#progressBar1')
}
````

Currently in works:

- Mobile Support
- Backwards compatibility for older Browsers.

MIT LICENCE
Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sub-license, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
