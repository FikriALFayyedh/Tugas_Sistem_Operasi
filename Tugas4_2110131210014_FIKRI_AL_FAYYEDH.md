# Struktur Sistem Operasi

## • Struktur Sederhana.
Banyak sistem yang tidak terstruktur dengan baik, sehingga sistem operasi seperti ini dimulai
dengan sistem yang lebih kecil, sederhana, dan terbatas. Kemudian berkembang dengan cakupan
yang original. Contoh sistem seperti ini adalah MS-DOS, yang disusun untuk mendukung fungsi
yang banyak pada ruang yang sedikit karena keterbatasan perangkat keras untuk menjalankannya.

Contoh sistem lainnya adalah UNIX, yang terdiri dari dua bagian yang terpisah, yaitu kernel dan
program sistem. Kernel selanjutnya dibagi dua bagian, yaitu antarmuka dan device drivers. Kernel
mendukung sistem berkas, penjadwalan CPU, manajemen memori, dan fungsi sistem operasi
lainnya melalui system calls.

## • Pendekatan Berlapis.
Sistem operasi dibagi menjadi sejumlah lapisan yang masing-masing dibangun di atas lapisan yang
lebih rendah. Lapisan yang lebih rendah menyediakan layanan untuk lapisan yang lebih tinggi.
Lapisan yang paling bawah adalah perangkat keras, dan yang paling tinggi adalah user-interface.

Sebuah lapisan adalah implementasi dari obyek abstrak yang merupakan enkapsulasi dari data dan
operasi yang bisa memanipulasi data tersebut. Keuntungan utama dengan sistem ini adalah
modularitas. Pendekatan ini mempermudah debug dan verifikasi sistem. Lapisan pertama bisa di
debug tanpa mengganggu sistem yang lain karena hanya menggunakan perangkat keras dasar untuk
implementasi fungsinya. Bila terjadi error saat debugging sejumlah lapisan, error pasti pada lapisan
yang baru saja di debug, karena lapisan dibawahnya sudah di debug.

Sedangkan menurut Tanenbaum dan Woodhull, sistem terlapis terdiri dari enam lapisan, yaitu:

• Lapisan 0. Mengatur alokasi prosesor, pertukaran antar proses ketika interupsi terjadi atau waktu
habis. Lapisan ini mendukung dasar multi-programming pada CPU.

• Lapisan 1. Mengalokasikan ruang untuk proses di memori utama dan pada 512 kilo word drum

yang digunakan untuk menahan bagian proses ketika tidak ada ruang di memori utama.

• Lapisan 2. Menangani komunikasi antara 
masing-masing proses dan operator console. Pada lapis
ini masing-masing proses secara efektif memiliki opertor console sendiri.

• Lapisan 3. Mengatur peranti M/K dan menampung informasi yang mengalir dari dan ke proses
tersebut.

• Lapisan 4. Tempat program pengguna. Pengguna tidak perlu memikirkan tentang proses,
memori, console, atau manajemen M/K.
• Lapisan 5. Merupakan operator sistem.

Dapat disimpulkan bahwa lapisan sistem operasi secara umum terdiri atas empat bagian, yaitu:
1. Perangkat keras. Lebih berhubungan kepada perancang sistem. Lapisan ini mencakup lapisan 0
dan 1 menurut Tanenbaum, dan level 1 sampai dengan level 4 menurut Stallings.
2. Sistem operasi. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 2 menurut
Tanenbaum, dan level 5 sampai dengan level 7 menurut Stallings.
3. Kelengkapan. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 3 menurut
Tanenbaum, dan level 8 sampai dengan level 11 menurut Stallings.
4. Program aplikasi. Lebih berhubungan kepada pengguna aplikasi komputer. Lapisan ini
mencakup lapisan 4 dan lapisan 5 menurut Tanebaum, dan level 12 dan level 13 menurut
Stallings.
## • Kernel Mikro.
Metode ini menyusun sistem operasi dengan mengeluarkan semua komponen yang tidak esensial
dari kernel, dan mengimplementasikannya sebagai program sistem dan level pengguna. Hasilnya
kernel yang lebih kecil. Pada umumnya mikrokernel mendukung proses dan menajemen memori
yang minimal, sebagai tambahan utnuk fasilitas komunikasi.

Fungsi utama mikrokernel adalah mendukung fasilitas komunikasi antara program klien dan
bermacam-macam layanan yang juga berjalan di user space. Komunikasi yang dilakukan secara
tidak langsung, didukung oleh sistem message passing, dengan bertukar pesan melalui mikrokernel.

Salah satu keuntungan mikrokernel adalah ketika layanan baru akan ditambahkan ke user space,
kernel tidak perlu dimodifikasi. Kalau pun harus, perubahan akan lebih sedikit. Hasil sistem
operasinya lebih mudah untuk ditempatkan pada suatu desain perangkat keras ke desain lainnya.
kernel-mikro juga mendukung keamanan reliabilitas lebih, karena kebanyakan layanan berjalan
sebagai pengguna proses. Jika layanan gagal, sistem operasi lainnya tetap terjaga. Beberapa sistem
operasi yang menggunakan metode ini adalah TRU64 UNIX, MacOSX, dan QNX.