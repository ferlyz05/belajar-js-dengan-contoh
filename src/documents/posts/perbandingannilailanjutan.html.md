---
layout: article
title: == vs === lanjutan
urutan: 10
author: A. Akbar Hidayat
---

Ada kondisi istimewa.

``` javascript
null == undefined; // betul

"NaN" == NaN; // salah
NaN == NaN; // salah
NaN != NaN; // betul

undefined == 0; // salah
null == 0; // salah
```

Jadi, `null` itu hanya `==` terhadap dirinya dan `undefined`.

Dan, `undefined` itu hanya `==` terhadap dirinya dan `null`.