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
