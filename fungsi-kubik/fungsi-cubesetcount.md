# Fungsi CUBESETCOUNT

### Deskripsi

Mengembalikan jumlah item dalam sebuah kumpulan.

### Sintaks

CUBESETCOUNT\(set\)

Sintaks fungsi CUBESETCOUNT memiliki argumen berikut:

*  **Set**    Diperlukan. Sebuah string teks ekspresi Microsoft Excel yang mengevaluasi sebuah kumpulan yang ditentukan oleh fungsi CUBESET. Set juga bisa berupa fungsi CUBESET, atau referensi ke sel yang memuat fungsi CUBESET.

### Keterangan

Bila fungsi CUBESETCOUNT mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.

### Contoh

=CUBESETCOUNT\(A3\)

= CUBESETCOUNT \(CUBESET \("Penjualan","\[Produk\].\[Semua Produk\]. Anak","Produk",1,"\[Pengukuran\].\[Jumlah Penjualan\]"\)\)

