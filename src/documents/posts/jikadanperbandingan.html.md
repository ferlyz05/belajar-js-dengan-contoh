---
layout: article
title: Jika & Perbandingan
urutan: 8
author: A. Akbar Hidayat
---

Bila saya adalah seorang manusia, maka saya jalan-jalan:

```javascript
var saya = "manusia";

// kita melakukan perbandingan menggunakan tanda == atau ===
if (saya == "manusia") {
    console.log("maka saya jalan-jalan... asyeeek");
}
```

Kita akan bahas tentang `===` pada bagian berikutnya. Tenang saja.

Lanjuuut...

Bila saya bukan seekor binatang, maka saya membaca:

```javascript
var saya = "manusia"

// != berarti tidak sama dengan
if (saya != "binatang") {
    console.log("maka saya membaca");    
}
```

Jangan sampai keliru ya:

```javascript
// ini adalah sebuah pemberian nilai, bukan perbandingan
if (saya = "manusia") { // kesalahan
    console.log("ooooh");
}
```

Tapi...tapi..tapi...

``` javascript
var saya = "manusia";

if (saya == "manusia") {
    // bila saya adalah manusia
    // tentu saja saya manusia
    console.log("maka saya tidur");
} else if (saya == "binatang") {
    // bila saya adalah binatang
    console.log("maka saya garuk-garuk");
} else if (saya == "tumbuhan") {
    // bila saya adalah tumbuhan
    console.log("maka saya melambai lambai");
} else {
    // bila tidak ketiga-tiganya
    console.log("lah....");
}
```

Perbandingan nilai kawan-kawan:

```javascript
var bilangan = 4;

// % adalah operasi modulo: bagi habis
if (bilangan % 2 === 0) {
    // dan ini yang dijalankan
    console.log("bilangan genap");
} else {
    console.log("bilangan ganjil");
}

// >= berarti lebih besar sama dengan
if (bilangan >= 0) {
    // dan ini yang dijalankan
    console.log("bilangan positif");
} else {
    console.log("bilangan negatif");
}

console.log(4 > 3); // betul
console.log(4 > 4); // salah
// tapi
console.log(4 >= 4); // betul
```
