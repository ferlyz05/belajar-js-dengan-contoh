---
layout: article
title: Perulangan for
urutan: 12
author: A. Akbar Hidayat
---

Kita ingin mengulang beberapa operasi sebanyak 10 kali

<a class="jsbin-embed" href="http://jsbin.com/UWAZuXE/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>

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

Tidak ingin dimulai dari `0`?
``` javascript
for (i = 5; i < 10; i++) {
    console.log(i);
}
// hasilnya 5, 6, 7, 8, 9
```

Bagaimana bila pada tiap perulangan, jumlah yang berubah tidaklah 1 saja seperti contoh di atas?

<a class="jsbin-embed" href="http://jsbin.com/oWolEcAX/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>