# js-zxing-pdf417
[![license](https://img.shields.io/badge/license-APACHE-green.svg?style=flat)](https://raw.githubusercontent.com/PeculiarVentures/js-zxing-pdf417/master/LICENSE)


I wanted to be able to find and decode PDF417 in browser so we did a port of the excelent http://github.com/zxing/zxing PDF417 decoder.

It works with excellent quality images but additional work is needed to make it detect PDF417's more reliably but in many tests it now works better than Zxing.

Demo
----
http://peculiarventures.github.io/js-zxing-pdf417

Build
-----

  npm install
  
  grunt

API
-----
Example - crop an image context:

```let imgContext = await _loadImageContext(imgFilePath);```

```let canvas = new Canvas(imgContext.img.width, imgContext.img.height);```

```let topHalfContext = canvas.getContext('2d');```

```topHalfContext.drawImage(imgContext, 0, 0, imgContext.img.width, imgContext.img.height / 2);```

Example - rotate an image context:

```let source = new BitmapLuminanceSource(ctx, img);```

```let binarizer = new HybridBinarizer(source);```

```let bitmap = new BinaryBitmap(binarizer);```

```let rotate90 = bitmap.rotateCounterClockwise();```

```let rotate180 = rotate90.rotateCounterClockwise();```


Requirements
------------
This library depends on https://github.com/peterolson/BigInteger.js
