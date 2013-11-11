---
layout: article
title: Perulangan while
urutan: 13
author: A. Akbar Hidayat
---

Konspenya tidak jauh berbeda dengan bentuk `for` sebelumnya. Contoh pertama adalah perulangan bentuk `do-while`:

```javascript
var i = 0;
do {
    // jalankan perintah berikut ini...
    console.log(i);
    i++;
    // selama i masih lebih kecil kurang dari 10
} while (i <= 10);
```

Sementara berikut ini adalah dalam bentuk `while`:
``` javascript
var i = 0;
while (i <= 10) {
    // selama i masih lebih besar dari i, maka kita
    // jalankan perintah berikut
    console.log(i);
    i++;
}
```