# Fungsi ISOWEEKNUM

### Pengertian

Mengembalikan jumlah angka minggu `ISO` dalam tahun untuk tanggal yang ditentukan.

### Sintaks

`ISOWEEKNUM(date)`

Sintaks fungsi `ISOWEEKNUM` memiliki argumen berikut.

* **`Date`**    Diperlukan. Date adalah kode tanggal-waktu yang digunakan oleh Excel untuk perhitungan tanggal dan waktu.

#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor berurutan sehingga dapat digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena tanggal itu adalah 39.448 hari setelah 1 Januari 1900.
* Jika argumen date bukan angka valid, `ISOWEEKNUM` mengembalikan nilai kesalahan `#NUM!`.
* Jika argumen date bukan tipe tanggal yang valid, `ISOWEEKNUM` mengembalikan nilai kesalahan `#NUM!`.

### Contoh

Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

| **Tanggal** |  |  |
| :--- | :--- | :--- |
| 3/9/2012 |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=ISOWEEKNUM(A2)` | Jumlah minggu dalam tahun terjadinya 3/9/2012, berdasarkan minggu-minggu yang dimulai pada default, yaitu Senin \(10\). | 10 |

