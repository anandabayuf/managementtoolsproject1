# Fungsi MINUTE

### Pengertian

Mengembalikan menit dari nilai waktu. Menit ditentukan sebagai bilangan bulat, rentangnya antara 0 sampai 59.

### Sintaks

`MINUTE(serial_number)`

Sintaks fungsi `MINUTE` memiliki argumen berikut:

* **`Serial_number`**    Diperlukan. Waktu yang memuat menit yang ingin Anda temukan. Waktu bisa dimasukkan sebagai string teks dengan tanda kutip \(contoh, "6:45 PM"\), sebagai angka desimal \(contoh, 0,78125, yang menyatakan 6:45 PM\), atau sebagai hasil dari rumus atau fungsi lain \(contoh, `TIMEVALUE("6:45 PM")`\).

#### Keterangan

Nilai waktu adalah porsi dari nilai tanggal dan diwakili oleh bilangan desimal \(misalnya, 12:00 PM ditulis 0,5, karena itu separuh hari\).

### Contoh

| **Waktu** |  |  |
| :--- | :--- | :--- |
| 12:45:00 PM |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=MINUTE(A2)` | Bagian menit dalam waktu di A2. | 4,5 |

