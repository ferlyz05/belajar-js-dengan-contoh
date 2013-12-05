---
layout: article
title: Objeck arguments
urutan: 18
author: A. Akbar Hidayat
---

Di dalam setiap metode, kita dapat mengetahui argumen apa yang dilemparkan kepadanya ketika metode tersebut dijalankan. Caranya adalah memanfaatkan objek yang bernama `arguments`

<a class="jsbin-embed" href="http://jsbin.com/AQiBEvOz/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>

Apa yang terjadi bila kita mengubah nilai dari `arguments`:

<a class="jsbin-embed" href="http://jsbin.com/ABetEPe/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>
    
Ok, nilai dari `pertama` tidak mengalami perubahan di luar metode `Angka`.

Bagaimana bila kita telah menetapkan bahwa suatu fungsi memiliki 2 parameter, tetapi argumen yang diberikan ketika ia dijalankan hanya berjumlah 1? Atau bagaimana bila ia berjumlah lebih dari 2?

<a class="jsbin-embed" href="http://jsbin.com/oNubULuZ/1/embed?js,console">JS Bin</a><script src="http://static.jsbin.com/js/embed.js"></script>
    
Bila pembaca bingung kenapa contoh terakhir menampilkan hasil `2: 15`, silahkan pembaca melihat kembali contoh pertama pada artikel ini.