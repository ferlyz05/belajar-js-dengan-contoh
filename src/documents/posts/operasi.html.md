---
layout: article
title: Operasi
urutan: 7
author: A. Akbar Hidayat
---

Kita dapat melakukan beberapa operasi aritmatika terhadap variabel.

``` javascript
var satu = 1,
    dua = 2,
    tiga = 3;

/**
 * Contoh Unary Operator
 */

// kita naikkan nilai dari satu sebanyak 1 kali
satu++;
satu++;

console.log(satu); // 3

// kita turunkan nilai dari satu sebanyak 1 kali
satu--;

console.log(satu); // 2

dua--;
dua--;
dua--;

console.log(dua); // -1
```

Tapi bentuk di bawah ini beda lo:

``` javascript
dua++;
++dua;
```

Bedanya adalah:

``` javascript
var satu = 1,
    dua = 2;

/**
 * Kita tampilkan nilai dari satu, baru kita tambahkan
 */
console.log(satu++); // 1
console.log(satu); // 2

/**
 * Kita tambahkan dulu, baru kita tampilkan nilai dari dua
 */
console.log(++dua); // 3
console.log(dua); // 3
```

Mari kita lanjutkan:

``` javascript
var kota = "Surabaya",
    kabupaten = "Malang";

// kita dapat menambahkan string
console.log(kota + ", " + kabupaten); // Surabaya, Malang
```

Tapi kita tidak dapat melakukan operasi ** * / - ** pada string

``` javascript
var kota = "Surabaya";

console.log(kota * 2); // NaN => Not A Number
console.log(kota - 2); // NaN => Not A Number
console.log(kota / 2); // NaN => Not A Number
```