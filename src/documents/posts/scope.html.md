---
layout: article
title: Scope
urutan: 22
author: A. Akbar Hidayat
---

Perhatikan contoh berikut ini

    function kurang( pertama, kedua) {
        return ketiga;
    }
    
    kurang(15, 5); // akan melemparkan kesalahan: RefernceError: ketiga is not defined

dan bandingkan dengan contoh berikut

    var ketiga = 15;
    function kurang( pertama, kedua ) {
        // perhatikan bagaimana metode ini menggunakan
        // nilai dari variable ketiga yang didefinisikan
        // diluar dari metode ini
        return pertama - kedua - ketiga;
    }
    
    kurang(40, 5); // hasilnya 20
    
## Sebab

Ketika *javascript engine* menemukan sebuah objek, maka ia pertama kali mencari definisi objek tersebut pada konteks dimana ia sedang berjalan.

Pada contoh pertama, objek yang akan ditemukan pada konteks metode `kurang` adalah:

    - pertama
    - kedua
    
Nah, bagaimana dengan `ketiga`? `ketiga` tidak ditemukan pada konteks `kurang`. Sehingga, javascript engine mencari `ketiga` pada konteks di atas konteks metode `kurang`. Konteks tersebut adalah konteks `global`.

Namun, `ketiga` tetap tidak ditemukan pada konteks `global`. Itulah mengapa dibangkitkan error dimana `ketiga` belum terdefinisikan.

Sekarang mari kita lihat kembali contoh kedua. Pada contoh tersebut, variabel `ketiga` tidak ditemukan pada konteks `kurang`. Maka, javascript engine mencari `ketiga` pada konteks di atas konteks `kurang`, yaitu konteks `global`. Pada `konteks global` inilah variabel `kurang` berhasil ditemukan.

Itulah mengapa pada contoh kedua, metode `kurang` tidak membangkitkan error.