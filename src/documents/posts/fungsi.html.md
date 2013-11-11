---
layout: article
title: Fungsi
urutan: 16
author: A. Akbar Hidayat
---

Kita dapat menggunakan fungsi untuk membungkus sebuah perintah. Bungkusan tadi memungkinkan kita mereferensi fungsi tersebut, sehingga dapat kita jalankan perintah yang dikandungnya di tempat lain.

```javascript
// ini adalah sebuah fungsi, dengan nama cetakNama
// dan memiliki parameter yaitu `nama`
function cetakNama( nama ) {
    console.log("Nama saya: " + nama);
}

// kita dapat menjalankan perintah yang dikandung oleh
// cetakNama dengan cara berikut
cetakNama("keripix");
// hasilnya = "Nama saya: keripix"

// ini adalah sebuah fungsi, dengan nama siapaSaya
// dan memiliki parameter nama dan asal
function siapaSaya( nama, asal ) {
    console.log("Saya adalah " + name + ", dan saya berasal dari " + asal);
}

siapaSaya("keripix", "Indonesia");
// "Saya adalah , dan saya berasal dari Indonesia"
```