# Fungsi YEARFRAC

### Pengertian

**`YEARFRAC`** menghitung pecahan tahun yang ditunjukkan dengan jumlah keseluruhan hari di antara dua tanggal \( **`start_date`** dan **`end_date`**\). Misalnya, Anda bisa menggunakan **`YEARFRAC`** untuk mengidentifikasi proporsi keuntungan sepanjang tahun, atau kewajiban untuk menetapkan istilah tertentu.

### Sintaks

`YEARFRAC(start_date, end_date, [basis])`

Sintaks fungsi YEARFRAC memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal yang menunjukkan tanggal mulai.
* **`End_date`**    Diperlukan. Tanggal yang menunjukkan tanggal akhir.
* **`Basis`**    Opsional. Tipe basis perhitungan hari untuk digunakan.

| **Basis** | **Basis perhitungan hari** |
| :--- | :--- |
| 0 atau dihilangkan | US \(NASD\) 30/360 |
| 1 | Sebenarnya/sebenarnya |
| 2 | Sebenarnya/360 |
| 3 | Sebenarnya/365 |
| 4 | European 30/360 |

**Penting:** 

* Tanggal harus dimasukkan menggunakan fungsi **`DATE`** , atau sebagai hasil dari rumus atau fungsi lain. Sebagai contoh, menggunakan `DATE(2018,5,23)` untuk hari 23 Mei, 2018. Masalah ini bisa terjadi jika tanggal yang dimasukkan sebagai teks.
* Fungsi **`YEARFRAC`** dapat mengembalikan hasil yang tidak benar ketika menggunakan basis kami \(NASD\) 30/360, dan `start_date` adalah hari terakhir bulan Februari.

{% hint style="info" %}
### Keterangan

* Excel menyimpan tanggal sebagai nomor seri berurutan sehingga mereka bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2018 adalah nomor seri 43101 karena 43,101 hari setelah 1 Januari 1900.
* Semua argumen dipotong menjadi bilangan bulat.
* Jika tanggal mulai atau tanggal akhir bukan tanggal yang valid, `YEARFRAC` mengembalikan nilai kesalahan `#VALUE!`.
* Jika basis &lt; 0 atau jika basis &gt; 4, `YEARFRAC` memuncukan nilai kesalahan `#NUM!`.
{% endhint %}

### Contoh

| **Data** | **Deskripsi** |  |
| :--- | :--- | :--- |
| 01/01/2012 | Tanggal mulai |  |
| 30/07/2012 | Tanggal akhir |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=YEARFRAC(A2,A3)` | Pecahan tahun antara 1/1/2012 dan 30/7/12, yang menghilangkan argumen Basis. | 0,58055556 |
| `=YEARFRAC(A2,A3,1)` | Pecahan antara tanggal yang sama, menggunakan argumen Aktual/Basis aktual. Karena 2012 adalah tahun kabisat, ini memiliki basis 366 hari. | 0,57650273 |
| `=YEARFRAC(A2,A3,3)` | Pecahan antara tanggal yang sama, menggunakan argumen Aktual/Basis 365. Menggunakan basis 365 hari. | 0,57808219 |

