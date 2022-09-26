<h2><b>Struktur Sistem Operasi</b></h2>

<p align="justify">&ensp;&ensp;&ensp;&ensp;Struktur sistem operasi merupakan komponen- komponen sistem operasi yang dihubungkan dan dibentuk di dalam kernel. Ada beberapa struktur sistem operasi yang pernah dicoba, diantaranya sebagai berikut:</p>

### __A. SISTEM MONOLITIK (Struktur Sederahana)__

<p align="justify">&ensp;&ensp;&ensp;&ensp;Sistem monolitik merupakan struktur sistem operasi sederhana yang dilengkapi dengan operasi “dual” pelayanan {sistem call} yang diberikan oleh sistem operasi. Model sistem call dilakukan dengan cara mengambil sejumlah parameter pada tempat yang telah ditentukan sebelumnya, seperti register atau stack dan kemudian mengeksekusi suatu intruksi trap tertentu pada monitor mod</p>

<p align="center"><img width="450" src="img/img1.jpeg"></p>

<p align="center"><i>Gambar Model struktur monolitik sistem operasi</i></p>

<p align="justify">&ensp;&ensp;&ensp;&ensp;Pada model ini, tiap-tiap sistem call memiliki satu service procedure. Utility procedure mengerjakan segala sesuatu yang dibutuhkan oleh beberapa service procedure, seperti mengambil data dari user program.</p>

<p align="justify">&ensp;&ensp;&ensp;&ensp;Mekanisme dan prinsip kerja model struktur monolitik sistem operasi ini adalah sebagai berikut:</p>

1. User program melakukan “trap” pada karnel
2. Intruksi berpindah dari user mode ke monitor mode dan mentransfer control ke sistem operasi.
3. Sistem operasi mengecek parameter — parameter dari pemanggilan tersebut, untuk menentukan sistem call mana yang memanggil.
4. Sistem operasi menunjuk ke suatu table yang berisi slot ke-k yang menunjuk sistem call K (Kontrol).
5. Kontrol akan dikembalikan kepada user program, jika sistem call telah selesai mengerjakan tugasnya.

<p align="justify">&ensp;&ensp;&ensp;&ensp;Tatanan ini memberikan suatu struktur dasar dari sistem operasi sebagai berikut :</p>

- Program utama meminta service procedure.
- Kumpulan service procedure yang dibaca oleh sistem call.
- Kumpulan utility procedure yang membantu service procedure.

### __Kegunggulan Sistem Monolik (Struktur Sederhana)__

1. Layanan pada satu ruang alamat memory.terhadap job-job yang ada bisa dilakukan dengan cepat karena berada

### __Kelemahan Sistem Monolik (Struktur Sederhana)__

1. Pengujian dan penghilangan kesalahan sulit dilakukan karena tidak dapat dipisahkan dan dilokasikan.
2. Sulit dalam menyediakan fasilitas pengamanan. Kurang efisien dalam penggunaan memori dimana setiap computer harus menjalankan kernel yang besar sementara tidak memerlukan seluruh layanan yang disediakan kernel.
3. Kesalahan pemrograman di satu bagian kernel menyebakan matinya seluruh system.