# Fungsi WORKDAY

### Pengertian

Mengembalikan angka yang menyatakan tanggal yang merupakan indikasi jumlah hari kerja sebelum atau sesudah sebuah tanggal \(tanggal mulai\). Hari kerja tidak termasuk akhir pekan dan tanggal yang ditetapkan sebagai hari libur. Gunakan `WORKDAY` untuk mengecualikan akhir pekan atau hari libur ketika menghitung tanggal jatuh tempo faktur, perkiraan tanggal pengiriman, atau jumlah hari pekerjaan yang telah dilakukan.

{% hint style="info" %}
**Tips:** Untuk menghitung nomor seri tanggal sebelum atau sesudah jumlah hari kerja tertentu dengan menggunakan parameter untuk menunjukkan berapa hari adalah hari akhir pekan, gunakan fungsi `WORKDAY.INTL`.
{% endhint %}

### Sintaks

`WORKDAY(start_date, days, [holidays])`

Sintaks fungsi `WORKDAY` memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal yang menunjukkan tanggal mulai.
* **`Days`**    Diperlukan. Jumlah hari nonakhir pekan dan nonhari libur sebelum atau setelah `start_date`. Nilai positif untuk hari mengembalikan tanggal mendatang, nilai negatif mengembalikan tanggal lampau.
* **`Hari Libur`**    Opsional. Daftar opsional yang terdiri dari satu atau lebih tanggal untuk dikecualikan dari kalender kerja, seperti hari libur nasional dan jatah cuti. Daftarnya bisa berupa rentang sel yang berisi tanggal atau konstanta array nomor seri yang menunjukkan tanggal.

{% hint style="info" %}
**Penting:** Tanggal harus dimasukkan dengan menggunakan fungsi `DATE`, atau sebagai hasil dari rumus atau fungsi lain. Contoh, gunakan `DATE(2008,5,23)` untuk tanggal 23 Mei 2008. Masalah bisa muncul jika tanggal dimasukkan sebagai teks.
{% endhint %}

{% hint style="info" %}
#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan di dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.
* Jika salah satu argumen bukan tanggal yang valid, `WORKDAY` mengembalikan nilai kesalahan `#VALUE!`.
* Jika `start_date` plus hari menghasilkan tanggal yang tidak valid, `WORKDAY` mengembalikan nilai kesalahan `#NUM!`.
* Jika hari bukan bilangan bulat, maka dipotong.
{% endhint %}

### Contoh

| **Data** |  |  |
| :--- | :--- | :--- |
| 01/10/2008 | Tanggal mulai |  |
| 151 | Hari menuju penyelesaian |  |
| 26/11/2008 | Hari Libur |  |
| 04/12/2008 | Hari Libur |  |
| 21/01/2009 | Hari Libur |  |
| **Rumus** | **Deskripsi \(Hasil\)** | **Hasil** |
| `=WORKDAY(A2,A3)` | Tanggal 151 hari kerja dari tanggal mulai \(30/04/2009\) | 30/04/2009 |
| `=WORKDAY(A2,A3,A4:A6)` | Tanggal 151 hari kerja dari tanggal mulai, kecuali hari libur \(30/04/2009\) | 05/05/2009 |

