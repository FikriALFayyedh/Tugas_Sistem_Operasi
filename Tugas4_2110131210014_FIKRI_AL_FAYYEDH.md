# Struktur Sistem Operasi

## • Struktur Sederhana / Sistem Monolitik
Struktur Sederhana / Sistem Monolitik merupakan struktur sistem operasi sederhana yang dilengkapi dengan operasi “dual” pelayanan {sistem call} yang diberikan oleh sistem operasi. Model sistem call dilakukan dengan cara mengambil sejumlah parameter pada tempat yang telah ditentukan sebelumnya, seperti register atau stack dan kemudian mengeksekusi suatu intruksi trap tertentu Pada model ini, tiap-tiap sistem call memiliki satu service procedure. Utility procedure mengerjakan segala sesuatu yang dibutuhkan oleh beberapa service procedure, seperti mengambil data dari user program.

Mekanisme dan prinsip kerja model struktur monolitik sistem operasi ini adalah sebagai berikut:

1. User program melakukan “trap” pada karnel

2. Intruksi berpindah dari user mode ke monitor

mode dan mentransfer control ke sistem operasi.

3. Sistem operasi mengecek parameter — parameter dari pemanggilan tersebut, untuk menentukan sistem call mana yang memanggil.

4. Sistem operasi menunjuk ke suatu table yang berisi slot ke-k yang menunjuk sistem call K (Kontrol).

5. Kontrol akan dikembalikan kepada user program, jika sistem call telah selesai mengerjakan tugasnya.

#### Keunggulan Sistem Monolitik
1) Layanan pada satu ruang alamat memory.terhadap job-job yang ada bisa dilakukan dengan cepat karena berada

#### Kelemahan Sistem Monolitik
1) Pengujian dan penghilangan kesalahan sulit dilakukan karena tidak dapat dipisahkan dan dilokasikan.

2) Sulit dalam menyediakan fasilitas pengamanan. Kurang efisien dalam penggunaan memori dimana setiap computer harus menjalankan kernel yang besar sementara tidak memerlukan seluruh layanan yang disediakan kernel.

3) Kesalahan pemrograman di satu bagian kernel menyebakan matinya seluruh system.

## • Pendekatan Berlapis.
Sistem operasi dibentuk secara hirarki berdasar lapisan — lapisan, dimana lapisan-lapisan bawa memberi layanan lapisan lebih atas. Lapisan yang paling bawah adalah perangkat keras dan yang paling tinggi adalah user- interface. Sebuah lapisan adalah implementasi dari obyek abstrak yang merupakan enkapsulasi dari data dan operasi yang bisa memanipulasi data tersebut. Struktur berlapis dimaksudkan untuk mengurangi kompleksitas rancangan dan implementasi sistem operasi. Contoh sistem operasi yang menggunakan sistem ini adalah: UNIX termodifikasi, THE, Venus dan OS/2.

#### Kelebihan Sistem Berlapis
1) Memiliki rancangan modular, yaitu sistem dibagi menjadi beberapa modul & tiap modul dirancang secara independen.

2) Pendekatan berlapis menyederhanakan rancangan, spesifikasi dan implementasi sistem operasi.

#### Kelemahan Sistem Berlapis
1) Fungsi-fungsi sistem operasi diberikan ke tiap lapisan secara hati-hati.

C. KERNEL MIKRO (MIKROKERNEL)

## • Kernel Mikro.
Metode struktur ini adalah menghilangkan komponen-komponen yang tidak diperlukan dari kernel dan mengimplementasikannya sebagai sistem dan program-program level user. Hal ini akan menghasilkan kernel yang kecil.

Fungsi utama dari jenis ini adalah menyediakan fasilitas komunikasi antara program client dan bermacam pelayanan yang berjalan pada ruang user.

Sistem operasi yang menggunakan micro kernel umumnya secara dramatis memiliki kinerja di bawah kinerja sistem operasi yang menggunakan monolithic kernel. Hal ini disebabkan oleh adanya overhead yang terjadi akibat proses input/output dalam kernel yang ditujukan untuk mengganti konteks (context switch) untuk memindahkan data antara aplikasi dan server.

Contoh Sistem operasi yang menggunakan struktur ini adalah : TRU64 UNIX, MacOSX dan QNX.

#### Kelebihan Kernel Mikro
1) kemudahan dalam memperluas sistem operasi

2) Mudah untuk diubah ke bentuk arsitektur baru

3) Kode yang kecil dan lebih aman

#### Kekurangan Kernel Mikro
1) kinerja akan berkurang selagi bertambahnya fungsi- fungsi yang digunakan.