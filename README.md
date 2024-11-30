# QRCode.js
QRCode.js is javascript library for making QRCode. QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.
QRCode.js has no dependencies.

Project forked by Dingjerry from KeeeX/qrcodejs, updated the obsolete keyCode attribute to a key attribute, fixed an issue where pressing Enter would not work.
Earlier,the project forked by KeeeX Company from davidshimjs/qrcodejs, they fixed Code Length Overflow error, and cleaned up the repository.

## Basic Usages
```html
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "https://github.com/Dingjerry/qrcodejs");
</script>
```

or with some options

```html
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "https://github.com/Dingjerry/qrcodejs",
	width: 128,
	height: 128,
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H
});
</script>
```

and you can use some methods

```javascript
qrcode.clear(); // clear the code.
qrcode.makeCode("https://github.com/Dingjerry"); // make another code.
```

### Using with webpack

```javascript
const QRCode = require("@Dingjerry/qrcodejs-dj");
// Use QRCode as usual
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License
