# QRCode.js
QRCode.js 是用于制作 二维码 的 javascript 库。QRCode.js 支持跨浏览器、HTML5 画布和 DOM 中的表格标签。
QRCode.js 没有依赖关系。

项目由 Dingjerry 从 KeeeX/qrcodejs 分支而来，将过时的keyCode属性更新为key属性，解决了按Enter键无效的问题。

早些时候，项目由 KeeeX Company 从 davidshimjs/qrcodejs 分支而来，并修复了代码长度溢出错误，并清理了软件源。



## 基本用法
```html
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "https://github.com/Dingjerry/qrcodejs");
</script>
```

或使用一些属性选项

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

你可以使用一些方法

```javascript
qrcode.clear(); // 清除二维码
qrcode.makeCode("https://github.com/Dingjerry"); // 制作另一个二维码
```

### 与 webpack 一起使用

```javascript
const QRCode = require("@keeex/qrcodejs-kx");
// 像往常一样使用 二维码
```

## 兼容浏览器
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## 许可证
MIT License
