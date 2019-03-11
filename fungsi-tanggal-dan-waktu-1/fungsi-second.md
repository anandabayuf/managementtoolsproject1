# Fungsi SECOND

### Pengertian

Mengembalikan detik dari satu nilai waktu. Detik diberikan sebagai bilangan bulat dalam rentang 0 \(nol\) sampai 59.

### Sintaks

`SECOND(serial_number)`

Sintaks fungsi `SECOND` memiliki argumen berikut:

* **`Serial_number`**    Diperlukan. Waktu yang memuat detik yang ingin Anda temukan. Waktu bisa dimasukkan sebagai string teks dengan tanda kutip \(contoh, "6:45 PM"\), sebagai angka desimal \(contoh, 0,78125, yang menyatakan 6:45 PM\), atau sebagai hasil dari rumus atau fungsi lain \(contoh, `TIMEVALUE("6:45 PM")`\).

{% hint style="info" %}
#### Keterangan

Nilai waktu adalah bagian dari nilai tanggal dan dinyatakan oleh angka desimal \(contoh, 12:00 PM ditampilkan sebagai 0,5 karena setengah dari hari\).
{% endhint %}

### Contoh

| **Data** |  |  |
| :--- | :--- | :--- |
| **Waktu** |  |  |
| 16.48.18 |  |  |
| 4.48 |  |  |
| **Rumus** | **Deskripsi** | **H** **asil** |
| `=SECOND(A3)` | Detik dalam waktu pertama \(18\) | 18 |
| `=SECOND(A4)` | Detik dalam waktu kedua \(0\) | {0} |

