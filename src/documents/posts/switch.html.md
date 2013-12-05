---
layout: article
title: Switch
urutan: 15
author: A. Akbar Hidayat
---

`switch` itu hampir mirip dengan `if`:

<a class="jsbin-embed" href="http://jsbin.com/UXefEqEr/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>

Pertanyaan, ketika melakukan perbandingan nilai, `switch` ini menggunakan konsep `==` atau `===` ya? Mari kita uji coba

```javascript
var angka = 10;

switch (angka) {
    case "10":
        console.log("Bentuk string dan bernilai '10'");
        break;
    case 10:
        console.log("Bentuk integer dan bernilai 10");
        break;
    default:
        console.log("zzzz");
}
// hasilnya = "Bentuk integer dan bernilai 10"
```

Jadi, `switch` meggunakan konsep `===`.

Bagaimana kalau mau lebih seru lagi:

<a class="jsbin-embed" href="http://jsbin.com/IhELemi/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>