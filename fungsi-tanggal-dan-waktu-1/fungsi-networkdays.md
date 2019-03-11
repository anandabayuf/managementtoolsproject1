# Fungsi NETWORKDAYS

### Pengertian

Mengembalikan jumlah semua hari kerja di antara `start_date` dan `end_date`. Hari kerja tidak termasuk akhir pekan dan tanggal-tanggal yang ditentukan sebagai hari libur. Gunakan `NETWORKDAYS` untuk menghitung tunjangan karyawan yang dibayar berdasarkan jumlah hari kerja selama masa tertentu.

**Tips:** Untuk menghitung seluruh hari kerja di antara dua tanggal dengan menggunakan parameter yang menunjukkan yang mana dan berapa hari yang merupakan hari akhir pekan, gunakan fungsi `NETWORKDAYS.INTL`.

### Sintaks

`NETWORKDAYS(start_date, end_date, [holidays])`

Sintaks fungsi `NETWORKDAYS` memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal yang menunjukkan tanggal mulai.
* **`End_date`**    Diperlukan. Tanggal yang menunjukkan tanggal akhir.
* **`Hari Libur`**    Opsional. Rentang opsional yang terdiri dari satu atau lebih tanggal untuk dikecualikan dari kalender kerja, seperti hari libur nasional dan jatah cuti. Daftarnya bisa berupa rentang sel yang berisi tanggal atau konstanta array nomor seri yang menunjukkan tanggal.

**Penting:** Tanggal harus dimasukkan dengan menggunakan fungsi `DATE`, atau sebagai hasil dari rumus atau fungsi lain. Contoh, gunakan `DATE(2012,5,23)` untuk tanggal 23 Mei 2012. Masalah bisa muncul jika tanggal dimasukkan sebagai teks.

#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 01 Januari 2012 adalah nomor seri 40909 karena tanggal itu adalah 40.909 hari setelah 1 Januari 1900.
* Jika ada argumen yang bukan tanggal valid, maka `NETWORKDAYS` mengembalikan nilai kesalahan `#VALUE!`.

### Contoh

| **Tanggal** | **Deskripsi** |  |
| :--- | :--- | :--- |
| 01/10/2012 | Tanggal mulai proyek |  |
| 01/03/2013 | Tanggal berakhir proyek |  |
| 22/11/2012 | Hari Libur |  |
| 04/12/2012 | Hari Libur |  |
| 21/01/2013 | Hari Libur |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=NETWORKDAYS(A2,A3)` | Jumlah hari kerja antara tanggal mulai \(01/10/2012\) dan tanggal berakhir \(01/03/2013\). | 110 |
| `=NETWORKDAYS(A2,A3,A4)` | Jumlah hari kerja antara tanggal mulai \(01/10/2012\) dan tanggal berakhir \(01/03/2013\), dengan hari libur 22/11/2012 sebagai hari libur kerja. | 1:09 |
| `=NETWORKDAYS(A2,A3,A4:A6)` | Jumlah hari kerja antara tanggal mulai \(01/10/2012\) dan tanggal berakhir \(01/03/2013\), dengan tiga hari hari libur sebagai hari libur kerja. | 107 |

