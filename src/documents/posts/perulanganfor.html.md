---
layout: article
title: Perulangan for
urutan: 12
author: A. Akbar Hidayat
---

Kita ingin mengulang beberapa operasi sebanyak 10 kali

```javascript
for (i = 0; i < 10; i++) {
    console.log(i);
}
// hasilnya = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

for (i = 0; i <= 10; i++) {
    console.log(i);
}
// hasilnya = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

for (i = 10; i > 0; i--) {
    console.log(i);
}
// hasilnya = 10, 9, 8, 7, 6, 5, 4, 3, 2, 1

```

Mau lebih ato kurang dari 10 kali?
``` javascript
// 20 kali
for (i = 0; i < 20; i++) {
    console.log(i);
}

// 1 kali
for (i = 0; i < 1; i++) {
    console.log(i);
}

// selamanya
for (;;) {
    console.log("selamanya"); // tidak dianjurkan dilakukan di rumah.
}
```