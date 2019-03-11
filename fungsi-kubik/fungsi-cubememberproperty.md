# Fungsi CUBEMEMBERPROPERTY

### Deskripsi

Mengembalikan nilai properti anggota dari kubus. Gunakan untuk memvalidasi nama anggota yang terdapat di dalam kubus dan mengembalikan properti yang ditentukan untuk anggota ini.

### Sintaks

CUBEMEMBERPROPERTY\(connection, member\_expression, property\)

Sintaks fungsi CUBEMEMBERPROPERTY memiliki argumen berikut:

*  **Connection**    Diperlukan. String teks nama koneksi ke kubus.
*  **Member\_expression**    Diperlukan. Sebuah string teks ekspresi multidimensi \(MDX, multidimensional expression\) dari anggota dalam kubik.
*  **Property**    Diperlukan. Sebuah string teks berupa nama properti yang dikembalikan atau referensi ke sel yang berisi nama properti.

### Keterangan

* Bila fungsi CUBEMEMBERPROPERTY mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.
* Jika nama koneksi bukan merupakan koneksi buku kerja valid yang disimpan dalam buku kerja, CUBEMEMBERPROPERTY akan mengembalikan nilai kesalahan \#NAME?. Jika server Pemrosesan Analitik Online \(OLAP, Online Analytical Processing\) tidak berjalan, tidak tersedia, atau mengembalikan pesan kesalahan, maka CUBEMEMBERPROPERTY akan mengembalikan nilai kesalahan \#NAME? .
* Jika sintaks member\_expression salah atau jika anggota yang ditentukan oleh member\_expression tidak terdapat dalam kubik, CUBEMEMBERPROPERTY mengembalikan nilai kesalahan \#N/A.
*  CUBEMEMBERPROPERTY dapat mengembalikan nilai kesalahan \#N/A jika Anda mereferensikan objek berbasis sesi, seperti anggota terhitung atau set bernama, dalam PivotTable saat berbagi koneksi, dan PivotTable tersebut dihapus atau Anda mengonversi PivotTable ke rumus. \(Pada tab **Opsi**, di grup **Alat**, klik **Alat OLAP**, lalu klik **Konversi ke Rumus**.\)
*  CUBEMEMBERPROPERTY tidak akan berfungsi pada [Model Data](https://support.office.com/id-id/article/membuat-model-data-di-excel-87e7a54c-87dc-488e-9410-5c75dbcb0f7b) Excel yang diedit di [Power Pivot](https://support.office.com/id-id/article/power-pivot-analisis-data-yang-efektif-dan-pemodelan-data-di-excel-a9c2c6e2-cc49-4976-a7d7-40896795d045), karena bukan kubus multidimensi.

### Contoh

=CUBEMEMBERPROPERTY\("Penjualan","\[Waktu\].\[Fiskal\].\[2014\]",$A$3\)

=CUBEMEMBERPROPERTY\("Penjualan","\[Toko\].\[TokoFavoritSaya\]","\[Toko\].\[Nama Toko\].\[Luas Toko\]"\)

