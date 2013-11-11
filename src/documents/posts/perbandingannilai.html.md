---
layout: article
title: == vs ===
urutan: 9
author: A. Akbar Hidayat
---

Apa sih bedanya?

```javascript
2 == "2"; // betul
2 === "2"; // salah

0 == false; // betul
0 === false; // salah

1 == true; // betul
1 === false; // salah
2 == true; // salah... ingat, salah

undefined == null; // betul
undefined === null; // salah
```

Jadi, perbedaan antara `==` dan `===` adalah:

Pada operasi `==`, javascript mengubah tipe dari nilai variabel ketika terjadi perbandingan.

Sementara operasi `===` tidak mengubah tipe dari nilai variabel ketika terjadi perbandingan.

Jadi, `3 == "3"` itu bernilai benar, karena ketika terjadi proses perbandingan, `"3"` diubah menjadi bentuk `Integer`, yaitu 3. Oleh karena itu, perbandingan yang terjadi pasca perubahan tipe nilai adalah `3 == 3`.

Bagaimana dengan `0 == false`? Yang diubah adalah nilai `Boolean`, dimana ia diubah menjadi bentuk `Integer`. `true` akan diubah menjadi 1, sementara `false` menjadi 0.