# Fungsi DATEVALUE

### Pengertian

Fungsi **`DATEVALUE`** mengonversi tanggal yang disimpan sebagai teks ke nomor seri yang dikenali Excel sebagai tanggal. Misalnya, rumus **`=DATEVALUE("1/1/2008")`** mengembalikan 39448, nomor seri tanggal 1/1/2008. Akan tetapi, ingatlah bahwa pengaturan tanggal sistem komputer Anda mungkin menyebabkan hasil fungsi **`DATEVALUE`** berbeda dari contoh ini.

Fungsi **`DATEVALUE`** sangat membantu dalam hal sebuah lembar kerja berisi tanggal dalam format teks yang ingin Anda filter, sortir, atau format sebagai tanggal, atau gunakan dalam peritungan tanggal.

### Sintaks

```text
DATEVALUE(date_text)
```

Sintaks fungsi `DATEVALUE` memiliki argumen berikut:

* **`Date_text`**    Diperlukan. Teks yang menyatakan tanggal dalam format tanggal Excel, atau referensi ke sel berisi teks yang menyatakan tanggal dalam format tanggal Excel. Misalnya, "1/30/2008" atau "30-Jan-2008" adalah string teks dalam tanda kutip yang menyatakan tanggal.

  Dengan menggunakan sistem tanggal default dalam Microsoft Excel untuk Windows, argumen **`date_text`** harus menyatakan tanggal antara 1 Januari 1900 dan 31 Desember 9999. Fungsi **`DATEVALUE`** mengembalikan nilai kesalahan `#VALUE!`. jika nilai argumen **`date_text`** berada di luar rentang ini.

  Jika bagian tahun dari argumen **`date_text`** dihilangkan, fungsi **`DATEVALUE`** menggunakan tahun saat ini dari jam bawaan komputer Anda. Informasi waktu dalam argumen **`date_text`** diabaikan.

#### Keterangan

* Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.447 hari setelah 1 Januari 1900.
* Sebagian besar fungsi secara otomatis mengonversi nilai tanggal ke nomor seri.

### Contoh

| **Data** |  |  |
| :--- | :--- | :--- |
| 11 |  |  |
| 3 |  |  |
| 2011 |  |  |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=DATEVALUE("8/22/2011")` | Nomor seri tanggal yang dimasukkan sebagai teks. | 40777 |
| `=DATEVALUE("22-MAY-2011")` | Nomor seri tanggal yang dimasukkan sebagai teks. | 40685 |
| `=DATEVALUE("2011/02/23")` | Nomor seri tanggal yang dimasukkan sebagai teks. | 40597 |
| `=DATEVALUE("5-JUL")` | Nomor seri tanggal yang dimasukkan sebagai teks, menggunakan sistem tanggal 1900, dan dengan asumsi bahwa jam bawaan komputer memunculkan tahun 2011 sebagai tahun saat ini. | 39634 |
| `=DATEVALUE(A2 & "/" & A3 & "/" & A4)` | Nomor seri tanggal yang dibuat dengan menggabungkan nilai dalam sel A2, A3, dan A4. | 40850 |

{% page-ref page="fungsi-tanggal-dan-waktu.md" %}

