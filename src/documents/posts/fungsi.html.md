---
layout: article
title: Fungsi
urutan: 16
author: A. Akbar Hidayat
---

Kita dapat menggunakan fungsi untuk membungkus sebuah perintah. Bungkusan tadi memungkinkan kita mereferensi fungsi tersebut, sehingga dapat kita jalankan perintah yang dikandungnya di tempat lain.

```javascript
// ini adalah sebuah fungsi, dengan nama cetakNama
function cetakNama( nama ) {
    console.log("Nama saya: " + nama);
}

// kita dapat menjalankan perintah yang dikandung oleh
// cetakNama dengan cara berikut
cetakNama("keripix");
// hasilnya = "Nama saya: keripix"
```