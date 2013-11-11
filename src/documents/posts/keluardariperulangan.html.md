---
layout: article
title: Keluar dari perulangan
urutan: 14
author: A. Akbar Hidayat
---

Kita dapat keluar dari perulangan yang sedang terjadi dengan menggunakan kata kunci `break`:

```javascript
for (i = 0; i <= 10; i++) {
    if (i == 8) {
        break;
    }

    console.log(i);
}
// hasilnya 0, 1, 2, 3, 4, 5, 6, 7
```

Tapi kita juga dapat memerintahkan perulangan untuk melanjutkan perulangan kepada tahapan berikutnya tanpa menjalankan fungsi yang ada di dalam perulangan:

```javascript
for (i = 0; i <= 10; i++) {
    if (i == 5) {
        // jika i bernilai 5, maka kita tidak akan menjalankan
        // perintah console.log(i) yang ada pada baris
        // dibawah
        continue;
    }

    console.log(i);
}
// hasilnya 0, 1, 2, 3, 4, 6, 7, 8, 9, 10
```