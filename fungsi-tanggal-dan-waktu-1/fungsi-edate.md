# Fungsi EDATE

### Pengertian

Mengembalikan nomor seri yang mewakili tanggal yang merupakan nomor indikasi dari bulan sebelum atau setelah tanggal yang ditentukan \(`start_date`\). Gunakan `EDATE` untuk menghitung tanggal jatuh tempo yang jatuh pada hari yang sama bulan tersebut sebagai tanggal penerbitan.

### Sintaks

```text
EDATE(start_date, months)
```

Sintaks fungsi `EDATE` memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal yang mewakili tanggal mulai. Tanggal harus dimasukkan menggunakan fungsi `DATE`, atau sebagai hasil dari rumus atau fungsi lain. Sebagai contoh, gunakan `DATE(2008,5,23)` untuk tanggal 23 Mei 2008. Masalah dapat terjadi jika tanggal dimasukkan sebagai teks.
* **`Month`**    Diperlukan. Jumlah bulan sebelum atau setelah `start_date`. Nilai positif untuk bulan menghasilkan tanggal masa mendatang; nilai negatif menghasilkan tanggal lampau.

#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri berurutan sehingga dapat digunakan di dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.
* Jika `start_date` bukan tanggal yang valid, `EDATE` akan mengembalikan nilai kesalahan `#VALUE!`.
* Jika bulan bukan bilangan bulat, maka dipotong.

### Contoh

| **Tanggal** |  |  |
| :--- | :--- | :--- |
| 15-Jan-11 |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=EDATE(A2,1)` | Tanggal, satu bulan setelah tanggal di atas | 15-Feb-11 |
| `=EDATE(A2,-1)` | Tanggal, satu bulan sebelum tanggal di atas | 15-Des-10 |
| `=EDATE(A2,2)` | Tanggal, dua bulan setelah tanggal di atas | 15-Mar-11 |

