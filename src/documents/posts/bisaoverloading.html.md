---
layout: article
title: Function Overloading???
urutan: 19
author: A. Akbar Hidayat
---

Bagaimana bila terdapat 2 atau lebih fungsi dengan nama yang sama?

    function angka( pertama, kedua ) {
        console.log(pertama, kedua);
    }
    
    function angka( pertama, kedua ) {
        console.log(pertama + kedua);
    }
    
    function angka( pertama, kedua ) {
        console.log(pertama - kedua);
    }
    
    angka(10, 3); // 7
    
Jadi, metode yang terakhir didefinisikanlah yang memperoleh nama `angka`.