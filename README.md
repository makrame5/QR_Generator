# 🔗 QRCode.js

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/davidshimjs/qrcodejs.svg?style=social&label=Star)](https://github.com/davidshimjs/qrcodejs)
[![GitHub forks](https://img.shields.io/github/forks/davidshimjs/qrcodejs.svg?style=social&label=Fork)](https://github.com/davidshimjs/qrcodejs/fork)

> A modern, dependency-free JavaScript library for generating QR codes with an enhanced user interface and export capabilities.

## ✨ Features

- 🎨 **Modern UI** with responsive design
- 📱 **Cross-browser** - Compatible with all modern browsers
- 🖼️ **Multiple exports** - Download as PNG, PDF and SVG
- ⚡ **No dependencies** - No external libraries required
- 🎯 **Easy to use** - Simple and intuitive API
- 📐 **Customizable size** - Control QR code dimensions
- 🎨 **Canvas and SVG rendering** - Support for both rendering formats

## 🚀 Live Demo

Open `index.html` or `index-svg.html` in your browser to test the enhanced interface.

## 📦 Installation

### Direct Download
```bash
https://github.com/makrame5/QR_Generator.git
cd qrcodejs
```

### CDN
```html
<script src="https://cdn.jsdelivr.net/npm/qrcode@1.5.3/build/qrcode.min.js"></script>
```

## 🎯 Basic Usage

### Simple HTML
```html
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "https://github.com/davidshimjs/qrcodejs");
</script>
```

### With Advanced Options
```html
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
    text: "https://github.com/davidshimjs/qrcodejs",
    width: 256,
    height: 256,
    colorDark: "#000000",
    colorLight: "#ffffff",
    correctLevel: QRCode.CorrectLevel.H
});
</script>
```

### Available Methods
```javascript
// Clear the QR code
qrcode.clear();

// Generate a new code
qrcode.makeCode("https://example.com");

// Change size dynamically
qrcode = new QRCode(document.getElementById("qrcode"), {
    width: 512,
    height: 512
});
```

## 🎨 Enhanced User Interface

This version includes a modern user interface with:

- **Input field** for text/URL to encode
- **Size control** with validation (100-2048px)
- **Export buttons** for PNG, PDF and SVG
- **Responsive design** adapted to all screens
- **Visual feedback** with error messages

### Export Features

#### PNG Export
```javascript
// Automatically available via the interface
// or programmatically:
var canvas = document.querySelector('#qrcode canvas');
var dataURL = canvas.toDataURL('image/png');
```

#### PDF Export
```javascript
// Uses jsPDF to generate a PDF
// QR code is centered on an A4 page
```

#### SVG Export (SVG version only)
```javascript
// Direct export of the generated SVG
var svg = document.querySelector('#qrcode svg');
var svgString = new XMLSerializer().serializeToString(svg);
```

## 🌐 Browser Compatibility

| Browser | Minimum Version |
|---------|-----------------|
| Chrome  | 4+              |
| Firefox | 3.5+            |
| Safari  | 4+              |
| Edge    | 12+             |
| IE      | 6+              |
| Mobile  | iOS 4+, Android 2.1+ |

## 📁 Project Structure

```
qrcodejs/
├── index.html          # Canvas version with enhanced UI
├── index-svg.html      # SVG version with enhanced UI
├── qrcode.js           # Main library
├── qrcode.min.js       # Minified version
├── jquery.min.js       # jQuery (for examples)
└── README.md           # Documentation
```

## ⚙️ Configuration Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `text` | string | - | Text or URL to encode |
| `width` | number | 256 | QR code width |
| `height` | number | 256 | QR code height |
| `colorDark` | string | "#000000" | Dark modules color |
| `colorLight` | string | "#ffffff" | Light modules color |
| `correctLevel` | number | QRCode.CorrectLevel.M | Error correction level |
| `useSVG` | boolean | false | Use SVG rendering |

### Error Correction Levels

- `QRCode.CorrectLevel.L` - ~7% correction
- `QRCode.CorrectLevel.M` - ~15% correction (default)
- `QRCode.CorrectLevel.Q` - ~25% correction
- `QRCode.CorrectLevel.H` - ~30% correction

## 🤝 Contributing

Contributions are welcome! Here's how to contribute:

1. **Fork** the project
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

## 📝 Changelog

### Enhanced Version
- ✨ Modern and responsive user interface
- 📥 PNG, PDF and SVG export features
- 🎛️ Size control with validation
- 🎨 Enhanced design with modern CSS
- 📱 Better mobile experience

### Original Version
- 🎯 Cross-browser QR code generation
- 🖼️ Canvas and SVG support
- ⚡ No external dependencies
- 🌐 Extended browser compatibility

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 👨‍💻 Author

**HIMEDI Makrame**

## 🙏 Acknowledgments

- [Kazuhiko Arase](http://www.d-project.com/) - Original QR Code algorithm
- [Jerome Etienne](http://jeromeetienne.github.com/jquery-qrcode/) - jQuery inspiration
- All contributors who have improved this library

---

⭐ **Don't forget to give a star if this project helped you!**
