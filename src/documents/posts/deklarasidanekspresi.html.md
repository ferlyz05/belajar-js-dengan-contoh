---
layout: article
title: Function Declaration & Function Expression
urutan: 20
author: A. Akbar Hidayat
---


Kita kembali bertemu dengan permasalahan definisi :D


Apa bedanya antara `function declaration` dan `function expression`?


Berikut ini adalah `function declaration`:


    function tambah( pertama, kedua ) {
        return pertama + kedua;
    }
    
Sementara berikut ini adalah `function expression`:

    var tambah = function( pertama, kedua ) {
        return pertama + kedua;
    }
    
    var kurang = function kurang( pertama, kedua) { // perhatikan pemberian nama
        return pertama - kedua;
    }