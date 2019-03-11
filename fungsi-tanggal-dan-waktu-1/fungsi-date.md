# Fungsi DATE

### **Pengertian**

Fungsi **`DATE`** mengembalikan nomor seri berurutan yang mewakili tanggal tertentu. Gunakan fungsi `DATE` Excel ketika mengambil tiga nilai terpisah dan menggabungkannya untuk membentuk tanggal.

### Sintaks

```text
DATE(tahun,bulan,hari)
```

Sintaks fungsi `DATE` memiliki argumen berikut:

* **`Tahun`**    Diperlukan. Nilai argumen **`tahun`** dapat diisi satu sampai empat digit. Excel menginterpretasikan argumen **`tahun`** sesuai sistem tanggal yang digunakan komputer. Secara default, Microsoft Excel untuk Windows menggunakan sistem tanggal 1900, yang berarti tanggal pertama adalah 1 Januari 1900.

  **Tips:** Gunakan empat digit untuk argumen **`tahun`** guna mencegah hasil yang tidak diinginkan. Sebagai contoh, "07" dapat berarti "1907" atau "2007." Tahun dengan empat digit akan mencegah kebingungan.

  * Jika **`tahun`** berada antara 0 \(nol\) dan 1899 \(inklusif\), Excel menambahkan nilai tersebut ke 1900 untuk menghitung tahun. Misalnya, `DATE(108,1,2)` mengembalikan 2 Januari 2008 \(1900+108\).
  * Jika **`tahun`** berada antara 1900 dan 9999 \(inklusif\), Excel menggunakan nilai tersebut sebagai tahun. Misalnya, `DATE(2008,1,2)` mengembalikan 2 Januari 2008.
  * Jika **`tahun`** kurang dari 0 atau diisi 10000 atau lebih, Excel akan mengembalikan nilai kesalahan `#NUM!`.

* **`Month`**    Diperlukan. Bilangan bulat positif atau negatif yang menyatakan bulan dari tahun tersebut dari 1 sampai 12 \(Januari sampai Desember\).
  * Jika **`bulan`** lebih besar dari 12, **`bulan`** menambahkan angka bulan tersebut ke bulan pertama pada tahun yang ditentukan. Misalnya, `DATE(2008,14,2)` mengembalikan nomor seri yang mewakili 2 Februari 2009.
  * Jika **`bulan`** kurang dari 1, **`bulan`** mengurangi besaran nomor bulan tersebut, ditambah 1, dari bulan pertama pada tahun yang ditentukan. Misalnya, `DATE(2008,-3,2)` mengembalikan nomor seri yang mewakili 2 September 2007.
* **`Day`**    Diperlukan. Bilangan bulat positif atau negatif yang menyatakan tanggal bulan dari 1 sampai 31.
  * Jika **`tanggal`** lebih besar dari jumlah hari dalam bulan yang ditentukan, **`tanggal`** menambahkan jumlah hari tersebut ke hari pertama dalam bulan. Misalnya, DATE\(2008,1,35\) mengembalikan nomor seri yang mewakili 4 Februari 2008.
  * Jika **`tanggal`** kurang dari 1, **`tanggal`** mengurangi besaran jumlah hari tersebut, ditambah satu, dari hari pertama pada bulan yang ditentukan. Misalnya, `DATE(2008,1,-15)` mengembalikan nomor seri yang mewakili 16 Desember 2007.

**Catatan:** Excel menyimpan tanggal sebagai nomor seri berurutan sehingga tanggal tersebut dapat digunakan dalam perhitungan. 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena tanggal tersebut berjarak 39.447 hari setelah 1 Januari 1900. Anda akan perlu mengubah format nomor \(Format Sel\) guna menampilkan tanggal yang sesuai.

![Fungsi DATE contoh 1](https://support.content.office.net/id-id/media/8f4e5f5d-8ea5-44f6-aae8-f473176fe431.png)

**Sintaks**: 

```text
DATE(tahun,bulan,hari)
```

Misalnya: **`=DATE(C2,A2,B2)`** menggabungkan tahun dari sel C2, bulan dari sel A2, dan hari dari sel B2, lalu meletakkannya ke satu sel sebagai tanggal. Contoh di bawah ini memperlihatkan hasil akhir di sel D2.

![Fungsi DATE Contoh 2](https://support.content.office.net/id-id/media/d14634e7-c3df-40ad-94ca-d44878460a00.png)

{% hint style="info" %}
**Diperlukan untuk menyisipkan tanggal tanpa rumus?** Tidak ada masalah. Anda bisa menyisipkan tanggal dan waktu dalam sel, atau Anda bisa menyisipkan tanggal yang diperbarui. Anda juga bisa mengisi data secara otomatis dalam sel lembar kerja.
{% endhint %}

### Menghitung tanggal berdasarkan tanggal lain

Anda dapat menggunakan fungsi `DATE` untuk membuat tanggal berdasarkan tanggal sel lain. Misalnya, Anda dapat menggunakan fungsi `YEAR`, `MONTH`, dan `DAY` untuk membuat tanggal hari jadi berdasarkan sel lain. Katakanlah hari pertama seorang karyawan di kantor adalah 1/10/2016; fungsi `DATE` dapat digunakan untuk menetapkan tanggal hari jadi kelima karyawan tersebut:

![Menghitung tanggal berdasarkan tanggal lain](https://support.content.office.net/id-id/media/031fb8d8-08ca-447c-a4df-547350c63607.png)

1. Fungsi `DATE` membuat tanggal.

   `=DATE(YEAR(C2)+5,MONTH(C2),DAY(C2))`

2. Fungsi `YEAR` terlihat di sel C2 dan mengekstrak "2012".
3. Lalu, "+5" menambahkan 5 tahun, dan menetapkan "2017" sebagai tahun hari jadi di sel D2.
4. Fungsi `MONTH` mengekstrak "3" dari C2. Fungsi ini menetapkan "3" sebagai bulan di sel D2.
5. Fungsi `DAY` mengekstrak "14" dari C2. Fungsi ini menetapkan "14" sebagai hari di sel D2.

### Mengonversi string teks dan angka menjadi tanggal

Jika membuka file yang berasal dari program lain, Excel akan mencoba mengenali tanggal dalam data. Namun terkadang tanggal tidak dikenali. Hal ini mungkin terjadi karena angka tersebut tidak terlihat seperti tanggal pada umumnya, atau karena data diformat sebagai teks. Jika demikian, Anda dapat menggunakan fungsi `DATE` untuk mengonversi informasi ke tanggal. Misalnya, dalam ilustrasi berikut, sel C2 berisi tanggal yang menggunakan format: TTTTBBHH. Tanggal tersebut juga diformat sebagai teks. Untuk mengonversinya menjadi tanggal, fungsi `DATE` digunakan dalam hubungannya dengan fungsi `LEFT`, `MID`, dan `RIGHT`.

![Mengonversi string teks dan angka menjadi tanggal](https://support.content.office.net/id-id/media/c6e1fe5a-6ac3-47c7-94bf-8b6a5062464e.png)

1. Fungsi `DATE` membuat tanggal.

   `=DATE(LEFT(C2,4),MID(C2,5,2),RIGHT(C2,2))`

2. Fungsi `LEFT` terlihat di sel C2 dan membawa 4 karakter pertama dari kiri. Fungsi ini akan menetapkan “2014” sebagai tahun dari tanggal yang dikonversi dalam sel D2.
3. Fungsi `MID` terlihat di sel C2. Fungsi tersebut dimulai di karakter kelima, kemudian membawa 2 karakter ke kanan. Fungsi ini menetapkan “03” sebagai bulan dari tanggal yang dikonversi dalam sel D2. Karena pemformatan D2 diatur menjadi **`Tanggal`**, “0” tidak disertakan dalam hasil akhir.
4. Fungsi `RIGHT` terlihat di sel C2 dan membawa 2 karakter pertama dimulai dari bagian paling kanan lalu berpindah ke kiri. Fungsi ini menetapkan “14” sebagai hari dari tanggal di D2.

### Menambah atau mengurangi tanggal dengan jumlah hari tertentu

Untuk menambahkan atau mengurangi tanggal dengan sejumlah hari tertentu, cukup tambah atau kurangi jumlah hari ke referensi sel atau nilai yang berisi tanggal.

Dalam contoh di bawah ini, sel A5 berisi tanggal yang kita inginkan untuk menambah dan mengurangi dengan 7 hari \(nilai dalam C5\).

![Menambah atau mengurangi tanggal dengan jumlah hari tertentu](https://support.content.office.net/id-id/media/b8eec6cd-4b2c-48e9-bf1e-439311f04373.png)

{% page-ref page="fungsi-tanggal-dan-waktu.md" %}

