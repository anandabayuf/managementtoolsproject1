# Fungsi HOUR

### Pengertian

Mengembalikan jam dari satu nilai waktu. Jam diberikan sebagai bilangan bulat, mulai dari 0 \(12:00 A.M.\) hingga 23 \(11:00 P.M.\).

### Sintaks

`HOUR(serial_number)`

Sintaks fungsi `HOUR` memiliki argumen berikut:

* **`Nomor_seri`**    Diperlukan. Waktu yang berisi jam yang ingin Anda temukan. Waktu bisa dimasukkan sebagai string teks dengan tanda kutip \(contoh, "6:45 PM"\), sebagai angka desimal \(contoh, 0,78125, yang menyatakan 6:45 PM\), atau sebagai hasil dari rumus atau fungsi lain \(contoh, `TIMEVALUE("6:45 PM")`\).

#### Keterangan

Nilai waktu adalah bagian dari nilai tanggal dan dinyatakan oleh angka desimal \(contoh, 12:00 PM ditampilkan sebagai 0,5 karena setengah dari hari\).

### Contoh

| **Waktu** |  |  |
| :--- | :--- | :--- |
| 0,75 |  |  |
| 18/07/2011 07:45 |  |  |
| 21/04/2012 |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=HOUR(A2)` | Mengembalikan 75% dari 24 jam | 18 |
| `=HOUR(A3)` | Mengembalikan bagian jam dari nilai tanggal/waktu. | 7 |
| `=HOUR(A4)` | Tanggal tanpa bagian waktu tertentu dianggap 12:00 AM, atau 0 jam. | {0} |

