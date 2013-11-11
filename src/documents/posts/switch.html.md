---
layout: article
title: Switch
urutan: 15
author: A. Akbar Hidayat
---

`switch` itu hampir mirip dengan `if`:

```javascript
var makananKesukaan = "pecel";

// kita akan memeriksa dan membandingkan nilai dari
// makananKesukaan
switch ( makananKesukaan ) {
    // bila makananKesukaan == pecel
    case "pecel":
        console.log("saya suka pecel");
        break; // jangan lupa
    // bila makananKesukaan == donat
    case "donat":
        console.log("saya suka donat");
        break;
    case "rujak":
        console.log("saya suka rujak");
        break;
    default:
        // bila tidak ada pilihan yang cocok, maka kita
        // masuk pada bagian ini
        console.log("saya tidak suka makan..bwahahaha");
}
```

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
```javascript
var angka = 10;

switch (true) {
    case angka > 5:
        console.log("Lebih besar dari 5");
        break;
    case angka < 5:
        console.log("Lebih kecil dari 5");
        break;
    default:
        console.log("zzzz");
}

```