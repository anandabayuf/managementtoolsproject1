# Fungsi DAYS

### Pengertian

Mengembalikan jumlah hari antara dua tanggal.

### Sintaks

```text
DAYS(end_date, start_date)
```

Sintaks fungsi `DAYS` memiliki argumen berikut.

* **`End_date`**    Diperlukan. `Start_date` dan `End_date` adalah dua tanggal yang ingin Anda ketahui jumlah hari di antara keduanya.
* **`Start_date`**   Diperlukan. `Start_date` dan `End_date` adalah dua tanggal yang ingin Anda ketahui jumlah hari di antara keduanya.

**Catatan:** Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan di dalam perhitungan Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39.448 karena 39.447 hari setelah 1 Januari 1900.

#### Keterangan

* Jika kedua argumen tanggal adalah angka, `DAYS` menggunakan `EndDate–StartDate` untuk menghitung jumlah hari di antara kedua tanggal tersebut.
* Jika salah satu argumen tanggal adalah teks, maka argumen tersebut diperlakukan sebagai `DATEVALUE(date_text)` dan mengembalikan tanggal bilangan bulat, bukan komponen waktu.
* Jika argumen tanggal adalah nilai numerik yang berada di luar rentang tanggal yang valid, `DAYS` akan mengembalikan nilai kesalahan `#NUM!`.
* Jika argumen tanggal adalah string yang tidak dapat diuraikan sebagai tanggal valid, `DAYS` akan mengembalikan nilai kesalahan `#VALUE!`.

### Contoh

| **Data** |  |  |
| :--- | :--- | :--- |
| 31/12/11 |  |  |
| 01/01/11 |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=DAYS("15/03/11","01/02/11")` | Menemukan jumlah hari antara tanggal akhir \(15/03/11\) dan tanggal akhir \(01/02/11\). Saat tanggal dimasukkan langsung ke dalam fungsi, Anda perlu menyertakannya dalam tanda kutip. Hasilnya adalah 42. | 42 |
| `=DAYS(A2,A3)` | Menemukan jumlah hari antara tanggal akhir di A2 dan tanggal awal di A3 \(364\). | 364 |

{% page-ref page="fungsi-tanggal-dan-waktu.md" %}

