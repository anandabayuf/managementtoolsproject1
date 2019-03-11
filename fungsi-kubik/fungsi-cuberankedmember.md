# Fungsi CUBERANKEDMEMBER

### Deskripsi

Mengembalikan anggota dalam set yang diperingkat. Gunakan untuk mengembalikan satu atau beberapa elemen dalam sebuah set, seperti tenaga penjualan paling berprestasi atau 10 siswa terbaik.

### Sintaks

CUBERANKEDMEMBER\(connection, set\_expression, rank, \[caption\]\)

Sintaks fungsi CUBERANKEDMEMBER memiliki argumen berikut:

*  **Connection**    Diperlukan. String teks nama koneksi ke kubus.
*  **Set\_expression**    Diperlukan. String teks dari sebuah ekspresi set, seperti "{\[Item1\].children}". Set\_expression juga bisa berupa fungsi CUBESET, atau referensi ke sel yang memuat fungsi CUBESET.
*  **Rank**    Diperlukan. Bilangan bulat yang menentukan nilai teratas untuk dikembalikan. Jika peringkat berupa nilai 1, maka akan mengembalikan nilai teratas, jika peringkat berupa nilai 2, maka akan mengembalikan nilai teratas kedua, dan seterusnya. Untuk mengembalikan 5 nilai teratas, gunakan CUBERANKEDMEMBER lima kali, yang masing-masing menentukan peringkat yang berbeda, dari 1 sampai 5.
*  **Keterangan**    Opsional. Sebuah string teks akan ditampilkan dalam sel sebagai ganti keterangan, jika ada, dari kubus.

### Keterangan

* Bila fungsi CUBERANKEDMEMBER mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.
* Jika nama koneksi bukan merupakan koneksi buku kerja valid yang disimpan dalam buku kerja, CUBERANKEDMEMBER akan mengembalikan nilai kesalahan \#NAME?. Jika server Pemrosesan Analitik Online \(OLAP, Online Analytical Processing\) tidak bekerja, tidak tersedia, atau mengembalikan pesan kesalahan, maka CUBERANKEDMEMBER akan mengembalikan nilai kesalahan \#NAME?.
* CUBERANKEDMEMBER mengembalikan nilai kesalahan \#N/A bila sintaks set\_expression salah atau bila set memuat setidaknya satu anggota dengan dimensi yang berbeda dibandingkan anggota lainnya.

### Contoh

=CUBERANKEDMEMBER\("Penjualan",$D$4,1,"Bulan Tertinggi"\)

=CUBERANKEDMEMBER\("Penjualan",CUBESET\("Penjualan","Musim Panas","\[2004\].\[Juni\]","\[2004\].\[Juli\]","\[2004\].\[Agustus\]"\),3,"Bulan Tertinggi"\)

{% hint style="info" %}
 **Tips:** Untuk mengembalikan nilai n terbawah, gunakan argumen sort\_order dan sort\_by pada fungsi CUBESET untuk membalik urutan set sehingga nilai teratas dalam set yang diurutkan merupakan nilai terbawah. Misalnya, CUBERANKEDMEMBER \("Sales", $D$4,1\) mengembalikan anggota terakhir, CUBERANKEDMEMBER \("Sales", $D$4, 2\) mengembalikan anggota terakhir berikutnya, dan seterusnya.
{% endhint %}

