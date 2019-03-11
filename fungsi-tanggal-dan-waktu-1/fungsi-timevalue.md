# Fungsi TIMEVALUE

### Pengertian

Mengembalikan angka desimal dari waktu yang dinyatakan oleh string teks. Angka desimal adalah nilai dimulai dari 0 \(nol\) sampai 0,99988426, menyatakan waktu dari jam 0:00:00 \(12:00:00 AM\) sampai jam 23:59:59 \(11:59:59 P.M.\).

### Sintaks

`TIMEVALUE(time_text)`

Sintaks fungsi `TIMEVALUE` memiliki argumen berikut:

* **`Time_text`**    Diperlukan. String teks yang menyatakan waktu dalam salah satu format waktu Microsoft Excel; sebagai contoh, string teks "6:45 PM" dan "18:45" di dalam tanda kutip ganda yang menyatakan waktu.

{% hint style="info" %}
#### Keterangan

* Informasi tanggal dalam `time_text` diabaikan.
* Nilai waktu adalah bagian dari nilai tanggal dan dinyatakan oleh angka desimal \(contoh, 12:00 PM ditampilkan sebagai 0,5 karena setengah dari hari\).
{% endhint %}

### Contoh

| **Rumus** | **Deskripsi** | **Hasil** |
| :--- | :--- | :--- |
| `=TIMEVALUE("2.24 AM")` | Bagian desimal dari suatu hari, dengan hanya waktu yang ditentukan. | 0,10 |
| `=TIMEVALUE("22-Ags-2011 6.35 AM")` | Bagian desimal dari suatu hari, dengan tanggal dan waktu yang ditentukan. | 0,2743 |

