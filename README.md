# LATIHAN7DPBO2023

> Saya Amida Zulfa Laila dengan NIM 2101147 mengerjakan Latihan Praktikum 7 dalam mata kuliah Desain Pemrograman Berorientasi Objek untuk keberkahan-Nya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

### Spesifikasi Soal
- Pemain mengendalikan bola. Setiap kali bola bergerak, skor pemain bertambah +1.
- Skor hanya bertambah jika pemain berbelok, bukan bergerak berurutan. Detail:
    - Saat pertama kali membuka program, pemain bergerak ke arah manapun, skor +1.
    - Setelah pemain bergerak, dia harus bergerak ke arah lain agar skornya +1. Jika menekan tombol yang sama, skor tetap (+0).
        - Contoh, pemain membuka program, lalu bergerak ke kanan dan berhenti, maka skor bertambah +1. Jika pemain bergerak ke arah atas, bawah, atau kiri, maka skor         - bertambah +1. Namun, jika pemain bergerak ke kanan lagi, maka skor +0.
    - Bagaimana jika urutannya, kanan - atas - kiri - kanan? Kanan yang kedua tetap +1, karena pergerakan pemain sebelumnya adalah kiri, sehingga tidak dianggap berurutan.


### Alur Program 
- User menekan tombol `W` `A` `S` `D` atau `⬆` `⬇` `⬅` `➡`
  - Lalu skor akan bertambah setiap kali menekan tombol di atas
  - Misalnya, user menekan tombol `D`, lalu lepas maka score bertambah menjadi `1`.
    - Lalu menekan kembali tombol `W`, lalu lepas maka score bertambah menjadi `2`.
    
### Design Program 
Program ini memiliki beberapa class, yaitu :
- Controller, berfungsi untuk mengontrol objek dalam game.
- Display, berfungsi untuk menampilkan objek pada frame.
- Game, berfungsi untuk mengontrol jalannya game karena terdapat beberapa method seperti method `start()` untuk memulai game, `stop()` untuk menghentikan game, `render()` untuk memuat tampilan game, dan `loop()` untuk menjalankan loop utama pada game.
- GameObject, merupakan class yang mengimplementasikan interface `GameInterface`.
- GameInterface, merupakan sebuah `interface` yang memiliki dua method, yaitu `render()` dan `loop()`.
- Handler, merupakan class yang mengimplementasikan interface `GameInterface`.
- Player, merupakan subclass dari class `GameObject`.
- Synchronization, berfungsi untuk me `render` objek dan me `looping` objek.

### Dokumentasi 
- Jika bola bergerak ke berbeda arah maka score `+1`, jika bola bergerak berkali-kali atau berurutan kepada 1 arah maka score `tidak bertambah`.
<p align="center">
  <img src="https://github.com/amizulfa/LATIHAN7DPBO2023/blob/main/screenshoot/lp7.gif" alt="gif format testing"/>
</p>

- Misalkan bola bergerak ke arah `atas`, `kiri`, `kanan`, lalu ke `atas` lagi, maka score nya menjadi `4` bukan `3`, karena tidak berurutan.
<p align="center">
  <img src="https://github.com/amizulfa/LATIHAN7DPBO2023/blob/main/screenshoot/contoh.gif" alt="gif format testing"/>
</p>
