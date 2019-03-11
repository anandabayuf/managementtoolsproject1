# Fungsi IFERROR

### Pengertian

Mengembalikan nilai yang Anda tentukan jika rumus mengevaluasi ke kesalahan; jika tidak, mengembalikan hasil rumus. Gunakan fungsi `IFERROR` untuk memerangkap dan mengatasi kesalahan di dalam rumus.

### Sintaks

```text
IFERROR(value, value_if_error)
```

Sintaks fungsi `IFERROR` memiliki argumen berikut:

* **`Nilai`**    Diperlukan. Argumen yang diperiksa apakah ada kesalahan.
* **`Value_if_error`**    Diperlukan. Nilai yang dikembalikan jika rumus mengevaluasi ke kesalahan. Jenis-jenis kesalahan berikut ini dievaluasi : `#N/A`, `#VALUE!`, `#REF!`, `#DIV/0!`, `#NUM!`, `#NAME?`, atau `#NULL!`.

### Keterangan

* Jika `Value` atau `Value_if_error` adalah sel kosong, maka `IFERROR` memperlakukannya sebagai nilai string kosong \(""\).
* Jika Value adalah rumus array, maka `IFERROR` mengembalikan array hasil untuk setiap sel di dalam rentang yang ditentukan di dalam nilai. Lihat contoh kedua di bawah.

### Contoh Sederhana

| **Kuota** | **Unit Terjual** |  |
| :--- | :--- | :--- |
| 210 | 35 |  |
| 55 | {0} |  |
|  | 23 |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=IFERROR(A2/B2, "Kesalahan dalam perhitungan")` | Memeriksa kesalahan dalam rumus di argumen pertama \(membagi 210 dengan 35\), tidak menemukan kesalahan, lalu mengembalikan hasil rumus | 6 |
| `=IFERROR(A3/B3, "Kesalahan dalam perhitungan")` | Memeriksa kesalahan dalam rumus di argumen pertama \(membagi 55 dengan 0\), menemukan kesalahan membagi dengan 0, lalu mengembalikan `value_if_error` | Kesalahan dalam perhitungan |
| `=IFERROR(A4/B4, "Kesalahan dalam perhitungan")` | Memeriksa kesalahan dalam rumus di argumen pertama \(membagi "" dengan 23\), tidak menemukan kesalahan, lalu mengembalikan hasil rumus. | {0} |

{% page-ref page="fungsi-logika.md" %}

