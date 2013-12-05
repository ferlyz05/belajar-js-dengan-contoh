---
layout: article
title: Hoisting
urutan: 21
author: A. Akbar Hidayat
---

Untuk memahami apa itu `hoisting`, perhatikan contoh `function declaration` berikut:

<a class="jsbin-embed" href="http://jsbin.com/iCAKole/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>
    
Lihat bagaimana pada baris pertama contoh di atas, javascript tahu apa itu `tambah`. Tetapi perhatikan contoh `function expression` berikut:

<a class="jsbin-embed" href="http://jsbin.com/UNezUhU/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>
    
Ketika contoh kedua dijalankan, kita memperoleh pesan error. Yaitu `kurang` bukanlah sebuah fungsi. Javascript tidak mengetahui apa itu `kurang`.

## Apa sebabnya?

Alasannya adalah, ketika javascript interpeter mengevaluasi kode pada contoh pertama, ia menemukan sebuah `function declaration` dengan nama `tambah`. Oleh *interpeter*-nya, `function declaration` diletakkan pada bagian awal dari program (dibelakang layar).

Untuk mengilustrasikan contoh di atas, inilah yang terjadi ketika contoh pertama dijalankan:

    function tambah( pertama, kedua ) {
        return pertama + kedua;
    }
    
    tambah(5, 10);
    
Kejadian di atas disebut dengan **Hoisting**. Jadi, sebuah `function declaration` akan di-*hoist* oleh *javascript engine*.

## Function Expression tidak dihoist

Sementara itu, `function expression` tidak di-*hoist* oleh javascript. Itulah mengapa, ketika contoh kedua dijalankan, *javascript engine* tidak mengetahui apa itu `kurang`.

Inilah salah satu perbedaan antara `function declaration` dan `function expression`.