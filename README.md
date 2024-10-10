# SistemAuthAman
Sistem login PHP yang aman, dibangun dari awal dengan perlindungan terhadap berbagai serangan umum.

Harap dicatat bahwa kode ini tidak disediakan untuk di-copy dan paste secara langsung (meskipun tidak ada masalah hukum dalam melakukannya). Kode ini mungkin tidak berfungsi langsung untuk Anda. Tujuan dari memposting kode ini adalah agar Anda dapat mengikuti video dan merujuknya jika diperlukan. Mohon jangan mengisi kolom komentar video saya dengan pesan kesalahan jika Anda mengalami masalah dalam implementasinya. Namun, jika Anda menemukan masalah dengan KODE YANG SEBENARNYA (bukan masalah yang hanya berlaku pada lingkungan Anda), silakan ajukan isu di GitHub.

### Fitur / Perlindungan
- Login (terlindungi dari serangan brute force/dictionary)
- Pendaftaran
- Reset kata sandi (dilakukan dengan cara yang aman dan ramah)
- Validasi Email (memastikan pengguna memiliki akses ke email yang digunakan untuk membuat akun)
- Perlindungan CSRF untuk semua fitur/formulir
- Penghapusan Akun 
- Semua fitur dilindungi dari SQL Injection menggunakan pernyataan terprepared PHP
- Perlindungan XSS (lihat video untuk cara mengimplementasikan saat menambahkan halaman Anda sendiri dengan data yang tidak terpercaya)
- Semua kata sandi di-hash sehingga bahkan jika penyerang mendapatkan akses ke basis data, mereka tidak dapat memperoleh kata sandi pengguna (kata sandi di-hash dan di-salt)

... Mungkin ada lebih banyak fitur yang belum saya pikirkan saat menulis ini.

***Beberapa fitur mungkin belum diimplementasikan.***

### Cara Menggunakan
1. Unduh dan instal MAMP/XAMPP (atau unduh PHP, MySQL, dan server Apache secara individu jika Anda tahu apa yang Anda lakukan).
2. Pastikan Anda menggunakan versi PHP yang terbaru. Saya menguji dengan versi 8, tetapi versi 7 seharusnya berfungsi, meskipun saya belum mengujinya sendiri.
3. Salin dan tempel semua file ke dalam direktori publik.
4. Modifikasi `config.php` untuk mencocokkan lingkungan dan kasus penggunaan Anda (mungkin perlu memodifikasi file lain juga).
5. Mulai layanan MySQL dan server Apache (lihat di bawah untuk struktur basis data).
6. Kunjungi situs web Anda dan uji.

### Struktur Basis Data
Struktur basis data didefinisikan dalam [tables.sql](tables.sql) yang dapat Anda gunakan untuk menghasilkan tabel yang diperlukan dalam basis data Anda.
