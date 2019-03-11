# Fungsi CUBESET

### Deskripsi

Menentukan set terhitung dari anggota atau rangkap dengan mengirim ekspresi set ke kubus pada server, yang membuat set itu, lalu mengembalikan set itu ke Microsoft Excel.

### Sintaks

CUBESET\(connection, set\_expression, \[caption\], \[sort\_order\], \[sort\_by\]\)

Sintaks fungsi CUBESET memiliki argumen berikut:

*  **Connection**    Diperlukan. String teks nama koneksi ke kubus.
*  **Set\_expression**    Diperlukan. String teks dari sebuah ekspresi set yang mengembalikan set anggota atau rangkap. Set\_expression juga dapat menjadi referensi sel bagi sebuah rentang Excel yang memuat satu atau beberapa anggota, rangkap, atau beberapa set yang dimasukkan dalam set tersebut.
*  **Caption**    Opsional. Sebuah string teks ditampilkan dalam sel sebagai ganti keterangan, jika ditentukan dari kubus.
*  **Sort\_order**    Opsional. Tipe pengurutan, jika ada, untuk dijalankan dapat berupa salah satu dari yang berikut:

|  **Bilangan bulat** |  **Konstanta yang dijumlahkan** |  **Deskripsi** |  **Argumen** **Sort\_by** |
| :--- | :--- | :--- | :--- |
| {0} | SortNone | Membiarkan set dalam urutan yang sudah ada. | Diabaikan |
| 1 | SortAscending | Mengurutkan set dalam urutan naik menurut sort\_by. | Diperlukan |
| 2 | SortDescending | Mengurutkan set dalam urutan turun menurut sort\_by. | Diperlukan |
| 3 | SortAlphaAscending | Mengurutkan set dalam urutan naik alfa. | Diabaikan |
| 4 | Sort\_Alpha\_Descending | Mengurutkan set dalam urutan turun alfa. | Diabaikan |
| 5 | Sort\_Natural\_Ascending | Mengurutkan set dalam urutan naik natural. | Diabaikan |
| 6 | Sort\_Natural\_Descending | Mengurutkan set dalam urutan turun natural. | Diabaikan |

* Nilai default adalah 0. Pengurutan alfa untuk sebuah set rangkap mengurutkan elemen terakhir dalam setiap rangkap. Untuk informasi selengkapnya tentang perintah urutan yang berbeda ini, lihat sistem bantuan Microsoft Office SQL Analysis Services.
*  **Sort\_by**    Opsional. Sebuah string teks nilai untuk mengurutkan. Misalnya, untuk mendapatkan kota dengan penjualan tertinggi, set\_expression berupa serangkaian kota, dan sort\_by berupa ukuran penjualan. Misalnya, untuk mendapatkan kota dengan populasi tertinggi, set\_expression berupa serangkaian kota, dan sort\_by berupa ukuran populasi. Jika sort\_order mensyaratkan sort\_by, dan sort\_by dikosongkan, maka CUBESET mengembalikan pesan kesalahan \#VALUE! .

### Keterangan

* Bila fungsi CUBESET mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.
* Jika nama koneksi bukan merupakan koneksi buku kerja valid yang disimpan dalam buku kerja, CUBESET akan mengembalikan nilai kesalahan \#NAME? Jika server Pemrosesan Analitik Online \(OLAP, Online Analytical Processing\) tidak bekerja, tidak tersedia, atau mengembalikan pesan kesalahan, maka CUBESET akan mengembalikan nilai kesalahan \#NAME?.
* Jika sintaks set\_expression salah atau set berisi setidaknya satu anggota dengan dimensi yang berbeda dibandingkan anggota lainnya, CUBESET akan mengembalikan nilai kesalahan \#N/A.
* Jika set\_expression lebih panjang dari 255 karakter, yang merupakan batasan untuk argumen bagi sebuah fungsi, maka CUBESET akan mengembalikan nilai kesalahan \#VALUE!. Untuk menggunakan string teks yang lebih panjang dari 255 karakter, masukkan string teks dalam sel \(dengan batasan 32.767 karakter\), lalu gunakan referensi sel sebagai argumen.
*  CUBESET dapat mengembalikan nilai kesalahan \#N/A jika Anda mereferensikan objek berbasis sesi, seperti anggota terhitung atau set bernama, dalam PivotTable saat berbagi koneksi, dan PivotTable tersebut dihapus atau Anda mengonversi PivotTable ke rumus. \(Pada tab **Opsi**, di grup **Alat**, klik **Alat OLAP**, lalu klik **Konversi ke Rumus**.\)

### Contoh

=CUBESET\("Keuangan","Urutan\(\[Produk\].\[Produk\].\[Kategori Produk\].Anggota,\[Ukuran\].\[Jumlah Penjualan\],ASC\)","Produk"\)

=CUBESET\("Penjualan","\[Produk\].\[Semua Produk\].Anak","Produk",1,"\[Ukuran\].\[Jumlah Penjualan\]"\)

