1. Penjelasan Struktur Antar Hubungan dan Contohnya
   
  Struktur antar hubungan dalam sistem komputer, sering disebut sebagai bus system, merupakan jalur komunikasi utama yang menghubungkan berbagai komponen dalam komputer.        Jalur ini mengatur pertukaran data, sinyal kontrol, dan alamat memori antar komponen seperti CPU, memori utama, dan perangkat input/output (I/O). Bus memungkinkan komponen    yang berbeda untuk berinteraksi satu sama lain dengan cara yang terkoordinasi dan efisien. contohnya sebagai berikut:

- PCI (Peripheral Component Interconnect):
PCI adalah standar bus yang diperkenalkan pada awal 1990-an, yang digunakan untuk menghubungkan perangkat keras seperti kartu grafis, kartu suara, dan jaringan ke motherboard komputer. PCI memiliki kecepatan transfer data tinggi dan tidak bergantung pada prosesor tertentu, sehingga fleksibel dan cepat dalam menangani beberapa perangkat sekaligus. PCI mendukung transfer data paralel dan memiliki kecepatan yang cukup untuk zamannya.

- USB (Universal Serial Bus):
USB adalah standar industri yang dirancang untuk menyederhanakan koneksi perangkat eksternal ke komputer. Melalui USB, perangkat seperti printer, keyboard, mouse, kamera digital, dan flash disk bisa dihubungkan dengan cepat tanpa perlu menghidupkan ulang komputer. USB mendukung kecepatan transfer yang tinggi (hingga 12 Mbps untuk USB 1.1, bahkan lebih untuk generasi berikutnya), serta kemampuan plug-and-play.

- ISA (Industry Standard Architecture):
ISA adalah standar bus yang digunakan pada komputer IBM PC awal. Bus ini beroperasi pada frekuensi rendah (sekitar 8,33 MHz) dan memiliki jalur data selebar 8 atau 16 bit. Kelebihan ISA adalah kompatibilitasnya dengan banyak perangkat lama, tetapi kekurangannya adalah kecepatan transfer yang lebih lambat dibandingkan bus modern seperti PCI.
Dengan kata lain, bus adalah tulang punggung jalur komunikasi di dalam komputer, yang menghubungkan seluruh bagian menjadi satu sistem kerja yang terintegrasi.

2. Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya?

Ketika terlalu banyak modul atau perangkat dipasang di satu bus, kinerja sistem bisa turun karena beberapa alasan teknis:

- Delay Propagasi Bertambah:
Semakin banyak perangkat yang terhubung, semakin panjang waktu yang diperlukan untuk sinyal menyebar dari satu ujung bus ke ujung lainnya. Ini berarti komunikasi antar perangkat menjadi lebih lambat.

- Antrian Akses Bus Memanjang:
Bus hanya bisa digunakan satu perangkat pada satu waktu (kecuali pada sistem tertentu seperti switched bus). Jika banyak perangkat ingin menggunakan bus bersamaan, mereka harus antri. Ini memperlambat waktu respon untuk masing-masing perangkat.

- Kapasitas Transfer Terbatas:
Bus memiliki batasan jumlah data yang bisa dikirim dalam satu waktu. Jika terlalu banyak data yang harus dikirimkan dari banyak perangkat sekaligus, bus bisa "macet", sehingga kinerja sistem keseluruhan menjadi turun drastis.

3. Solusi yang umum digunakan adalah dengan menerapkan struktur bus hierarkis, yaitu membagi sistem menjadi beberapa bus berdasarkan kecepatan dan kebutuhan bandwidth. 

Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah ? Di bawah kondisi Seperti apa keadaan diatas tidak berlaku?
Dalam sistem berbasis interrupt (SBI), prioritas menentukan urutan layanan. Biasanya CPU atau perangkat penting diberi prioritas lebih tinggi. Namun, ada kondisi unik dimana perangkat berprioritas rendah justru memiliki waktu tunggu yang lebih singkat. Ini karena:

- Perangkat berprioritas tinggi sering harus menunggu selesainya pemrosesan data besar atau operasi kompleks.

- Perangkat prioritas rendah biasanya hanya membutuhkan layanan cepat, kecil, dan segera selesai, sehingga antriannya relatif lebih cepat bergerak.

Namun, kondisi ini tidak berlaku dalam kasus tertentu, misalnya:

- Overrun Buffer:
Jika perangkat mengirimkan data terlalu cepat dan buffer (penampung data sementara) tidak cukup besar untuk menampung semua data itu, maka data bisa hilang atau perlu dikirim ulang. Ini menyebabkan keterlambatan dan meningkatkan waktu tunggu rata-rata.

- Sistem Terlalu Sibuk:
Bila hampir semua perangkat dalam sistem aktif bersamaan (high load), perangkat berprioritas rendah mungkin harus menunggu jauh lebih lama dibanding biasanya karena resource sudah dipakai penuh oleh prioritas lebih tinggi.

Kesimpulannya, meskipun teori umum mengatakan bahwa perangkat prioritas rendah punya waktu tunggu pendek, pada kenyataannya situasi sistem sangat menentukan.

SUMBER REFRENSI:

https://tecnomasi.blogspot.com/2015/12/jawaban-organisasi-arsitektur-komputer.html

https://123dok.com/document/zg65782q-bab-sistem-bus-organisasi-komputer.html

https://www.questionai.com/questions-sz1AD1Tn3j/content-3-umumnya-perangkat-berprioritas-paling-rendah
