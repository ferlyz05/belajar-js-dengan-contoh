---
layout: article
title: Objeck arguments
urutan: 18
author: A. Akbar Hidayat
---

Di dalam setiap metode, kita dapat mengetahui argumen apa yang dilemparkan kepadanya ketika metode tersebut dijalankan. Caranya adalah memanfaatkan objek yang bernama `arguments`

    function Hallo() {
        return arguments;
    }
    
    Hallo(1, 2, 4, 6, 10); // mengembalikan 1, 2, 4, 6, 10
    
    function Angka() {
        for (i = 0; i < arguments.length; i++) {
            console.log(arguments[i]);
        }
        
        console.log("ada " + arguments.length + " jumlah argumen");
    }
    
    Angka(10, 5, 7, 19, 21, 1, 45);
    // 10
    // 5
    // 7
    // 19
    // 21
    // 1
    // 45
    // ada 7 jumlah argumen

Apa yang terjadi bila kita mengubah nilai dari `arguments`:

    function Angka() {
        arguments[0] = 0;
        console.log(arguments);
    }
    
    var pertama = 15,
        kedua = 30;
        
    Angka(pertama, kedua); // mengembalikan 0, 30
    console.log(pertama); // bernilai 15 (tidak berubah)
    
Ok, nilai dari `pertama` tidak mengalami perubahan di luar metode `Angka`.

Bagaimana bila kita telah menetapkan bahwa suatu fungsi memiliki 2 parameter, tetapi argumen yang diberikan ketika ia dijalankan hanya berjumlah 1? Atau bagaimana bila ia berjumlah lebih dari 2?

    function Angka( pertama, kedua ) {
        console.log(pertama);
        console.log(kedua);
        
        for (i = 0; i < arguments.length; i++) {
            console.log(i + " : ", arguments[i]);
        }
    }
    
    Angka(1);
    // 1
    // undefined <-- undefined karena parameter `kedua` tidak didefinisikan
    // 0: 1
    
    Angka(5, 10);
    // 5
    // 10
    // 0: 5
    // 1: 10
    
    Angka(5, 10, 15);
    // 5
    // 10
    // 0: 5
    // 1: 10
    // 2: 15 <-- seharusnya tidak kaget dengan hasil ini :D
    
Bila pembaca bingung kenapa contoh terakhir menampilkan hasil `2: 15`, silahkan pembaca melihat kembali contoh pertama pada artikel ini.