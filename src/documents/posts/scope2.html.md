---
layout: article
title: Scope Lanjutan
urutan: 23
author: A. Akbar Hidayat
---

Untuk menjelajahi lebih lanjut mengenai `scope` dan `konteks`, mari kita lihat contoh berikut:

    var kelima = 17;
    
    function angka( pertama, kedua ) {
    
        var ketiga = 7;
        
        function tambah () {
        
            var keempat = 10;
            
            return pertama + kedua + ketiga + keempat + kelima;
            
        }
        
        var hasilPenambahan = tambah();
        
        return hasilPenambahan;
    
    }
    
    angka(2, 4); // mengembalikan 40
    
Pada contoh di atas, hirarki konteks adalah seperti berikut

    - global
        - kelima
        - `angka`:
            - pertama
            - kedua
            - ketiga
            - `tambah`:
                - keempat
                
Jadi, ketika `pertama`, `kedua` dan `ketiga` tidak ditemukan pada konteks `tambah`, javascript engine mencari ketiga variabel tersebut pada konteks di atasnya. Konteks tersebut adalah konteks metode `angka`.

Pada konteks `angka` inilah ditemukan `pertama`, `kedua` dan `ketiga`. Bagaimana dengan variabel `kelima`?

Pertama, javascript engine akan mencari pada konteks `tambah`, namun ia tidak menemukannya. Kemudian ia mencari pada konteks di atasnya, konteks metode `angka`. Tidak juga ditemukan. Maka, langkah terakhir adalah mencari konteks di atas konteks `angka`, yaitu konteks `global`. Disinilah ia menemukan `kelima`.

# Scope berdasarkan fungsi

Itulah konsep *scope* pada javascript. *Scope* ditentukan oleh blok fungsi. Jadi, bila ada 2 variabel yang memiliki nama yang sama, maka nilai dari variabel tersebut akan ditentukan oleh *scope* paling bawah.

    var lima = 5;
    
    function angka() {
        var lima = 7;
        return lima;
    }
    
    angka(); // 7