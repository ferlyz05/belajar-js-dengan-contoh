---
layout: article
title: Closure
urutan: 24
author: A. Akbar Hidayat
---

Dengan *Closure*, kita dapat mengembalikan sebuah fungsi yang memiliki akses terhadap *scope* fungsi ketika ia didefinisikan.

    function tambahAwal( nilai ) {
        return function( pertama, kedua ) {
            return nilai + pertama + kedua;
        }
    }
    
    var tambahDua = tambahAwal(2);
    
    tambahDua(3, 5); // 10
    
Mari kita bedah pelan-pelan. Ketika metode `tambahAwal` dijalankan, ia mengembalikan metode berikut:
    
    function( pertama, kedua ) {
        return nilai + pertama + kedua;
    }
    
Fungsi di atas bernama `anonymous function`, karena ia tidak memiliki nama.

Pertanyaan: berapa nilai dari variabel `nilai`? Nilainya sama dengan nilai dari argumen pada metode `tambahAwal` ketika ia dijalankan. Jadi, pada contoh di atas, nilai dari variabel `nilai` adalah 2:

    var tambahDua = tambahAwal(2);
    
Yang perlu dipahami adalah, `anonymous function` yang dikembalikan oleh fungsi `tambahAwal` tetap memegang konteks ketika ia didefinisikan.

    function tambahAwal( nilai ) {
        // anonymous function didefinisikan
        return function( pertama, kedua ) {
            // Jadi, ketika fungsi ini telah dikembalikan oleh metode tambahAwal, fungsi ini tetap memiliki akses
            // terhadap konteks ketika ia terdefinisikan.
            // Jadi, ia dapat mengakses variabel `nilai` miliknya `tambahAwal`.
            return nilai + pertama + kedua;
        }
    }
    
Jadi `tambahDua` kurang lebih berisi fungsi berikut:

    var tambahDua = function( pertama, kedua ) {
        // return nilai + pertama + kedua
        return 2 + pertama + kedua;
    }
    
Sehingga, `tambahDua(3,5);` adalah: `2 + 3 + 5`.

## Kesimpulan

Wujud dari konsep *Closure* adalah fungsi yang tetap memiliki referensi terhadap konteks ketika fungsi tersebut didefinisikan. Konsep *Closure* masih memiliki hubungan yang erat dengan konsep *Scope* yang telah kita bahas sebelumnya.