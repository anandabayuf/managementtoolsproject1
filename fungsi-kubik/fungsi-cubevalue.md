# Fungsi CUBEVALUE

### Deskripsi

Mengembalikan nilai agregat dari kubus.

### Sintaks

CUBEVALUE\(connection, \[member\_expression1\], \[member\_expression2\], …\)

Sintaks fungsi CUBEVALUE memiliki argumen berikut:

*  **Connection**    Diperlukan. String teks nama koneksi ke kubus.
*  **Member\_expression**    Opsional. Sebuah string teks ekspresi multidimensi \(MDX, multidimensional expression\) yang mengevaluasi anggota atau rangkap dalam kubus. Alternatifnya, member\_expression dapat berupa sebuah set yang ditentukan dengan fungsi CUBESET. Gunakan member\_expression sebagai pemotong untuk menentukan bagian kubus di mana nilai agregat dikembalikan. Jika tidak ada ukuran yang ditentukan dalam member\_expression, maka ukuran default untuk kubus tersebut akan digunakan.

### Keterangan

* Bila fungsi CUBEVALUE mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.
* Jika referensi sel digunakan untuk member\_expression, dan referensi sel berisi fungsi CUBE, maka member\_expression menggunakan ekspresi MDX untuk item dalam sel referensi, dan bukan nilai yang ditampilkan dalam sel referensi.
* Jika nama koneksi bukan merupakan koneksi buku kerja valid yang disimpan dalam buku kerja, CUBEVALUE akan mengembalikan nilai kesalahan \#NAME?. Jika server Pemrosesan Analitik Online \(OLAP, Online Analytical Processing\) tidak bekerja, tidak tersedia, atau mengembalikan pesan kesalahan, maka CUBEVALUE akan mengembalikan nilai kesalahan \#NAME?.
* Jika setidaknya satu elemen dalam rangkap tidak valid, CUBEVALUE akan mengembalikan nilai kesalahan \#VALUE!.
* CUBEVALUE mengembalikan nilai kesalahan \#N/A bila:

1. Sintaks member\_expression salah.
2. Anggota yang ditentukan oleh member\_expression tidak terdapat di dalam kubus.
3. Rangkap tidak valid karena tidak terdapat irisan untuk nilai-nilai yang ditentukan. \(Ini dapat terjadi pada beberapa elemen dari hierarki yang sama.\)
4. Set berisi setidaknya satu anggota dengan dimensi yang berbeda dibandingkan anggota lainnya.
5.  CUBEVALUE dapat mengembalikan nilai kesalahan \#N/A jika Anda mereferensikan objek berbasis sesi, seperti anggota terhitung atau set bernama, dalam PivotTable saat berbagi koneksi, dan PivotTable tersebut dihapus atau Anda mengonversi PivotTable ke rumus. \(Pada tab **Opsi**, di grup **Alat**, klik **Alat OLAP**, lalu klik **Konversi ke Rumus**.\)

 **Masalah: Nilai null dikonversi ke string panjang-nol**

Dalam ,Excel jika sel tidak memiliki data, karena Anda tidak pernah mengubahnya atau Anda telah menghapus kontennya, maka sel akan berisi nilai kosong. Dalam banyak sistem database, nilai kosong disebut sebagai nilai Null. Nilai kosong atau Null secara literal berarti "Tidak ada nilai." Namun, sebuah rumus bisa tidak pernah mengembalikan string kosong atau nilai Null. Rumus selalu mengembalikan satu dari tiga nilai berikut: nilai angka; nilai teks, yang mungkin berupa string panjang-nol, atau nilai kesalahan, seperti \#NUM! atau \#VALUE.

Jika rumus berisi fungsi CUBEVALUE yang tersambung ke database Online Analytical Processing \(OLAP\) dan kueri ke database ini mengembalikan nilai Null, Excel akan mengonversi nilai Null ini ke string panjang-nol, meskipun rumus sebaliknya akan mengembalikan nilai angka. Hal ini dapat menimbulkan situasi di mana rentang sel berisi gabungan nilai numerik dan string kosong, dan situasi ini dapat memengaruhi hasil rumus lainnya yang merujuk pada rentang sel tersebut. Misalnya, jika A1 dan A3 berisi angka, dan A2 berisi rumus dengan fungsi CUBEVALUE yang mengembalikan string kosong, maka rumus berikut akan mengembalikan \#VALUE! kesalahan:

=A1+A2+A3

Untuk mencegah hal ini, Anda dapat menguji string panjang-nol dengan menggunakan fungsi ISTEXT dan menggunakan fungsi IF untuk mengganti string panjang-nol dengan 0 \(nol\) seperti yang diperlihatkan contoh berikut:

=IF\(ISTEXT\(A1\),0,A1\)+IF\(ISTEXT\(A2\),0,A2\)+IF\(ISTEXT\(A3\),0,A3\)

Alternatifnya, jika Anda dapat menumpuk fungsi CUBEVALUE dalam syarat IF yang mengembalikan nilai 0 jika fungsi CUBEVALUE mengevaluasi string panjang-nol seperti yang diperlihatkan contoh berikut:

=IF \(CUBEVALUE\("Penjualan","\[Ukuran\].\[Keuntungan\]","\[Waktu\].\[2004\]","\[Semua Produk\].\[Minuman\]"\)="", 0, CUBEVALUE\("Penjualan","\[Ukuran\].\[Keuntungan\]","\[Waktu\].\[2004\]","\[Semua Produk\].\[Minuman\]"\)\)

Perhatikan bahwa fungsi SUM tidak mensyaratkan uji untuk string panjang-nol ini karena secara otomatis mengabaikan string panjang-nol ketika menghitung nilai yang dikembalikan.

### Contoh

=CUBEVALUE\("Penjualan","\[Ukuran\].\[Keuntungan\]","\[Waktu\].\[2004\]","\[Semua Produk\].\[Minuman\]"\)

=CUBEVALUE\($A$1,"\[Ukuran\].\[Keuntungan\]",D$12,$A23\)

=CUBEVALUE\("Penjualan",$B$7,D$12,$A23\)

