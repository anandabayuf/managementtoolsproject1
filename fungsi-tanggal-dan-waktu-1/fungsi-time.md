# Fungsi TIME

### Pengertian

Mengembalikan angka desimal untuk waktu tertentu. Jika format sel adalah **Umum** sebelum fungsi dimasukkan, hasil diformat sebagai tanggal.

Angka desimal yang dihasilkan oleh `TIME` adalah nilai yang dimulai dari 0 \(nol\) sampai 0,99988426, menyatakan waktu dari jam 0:00:00 \(12:00:00 AM\) sampai 23:59:59 \(11:59:59 P.M.\).

### Sintaks

`TIME(hour, minute, second)`

Sintaks fungsi `TIME` memiliki argumen berikut:

* **`Hour`**    Diperlukan. Angka dari 0 \(nol\) sampai 32767 yang menyatakan jam. Nilai apa pun yang lebih besar dari 23 akan dibagi dengan 24 dan sisanya akan dianggap sebagai nilai jam. Sebagai contoh, `TIME(27,0,0) = TIME(3,0,0) = 0,125 atau 3:00 AM`.
* **`Minute`**    Diperlukan. Angka dari 0 sampai 32767 yang menyatakan menit. Nilai apa pun yang lebih besar dari 59 akan dikonversi menjadi jam dan menit. Sebagai contoh, `TIME(0,750,0) = TIME(12,30,0) = 0,520833 atau 12:30 PM`.
* **`Second`**    Diperlukan. Angka dari 0 sampai 32767 yang menyatakan detik. Nilai apa pun yang lebih besar dari 59 akan dikonversi menjadi jam, menit, dan detik. Sebagai contoh, `TIME(0,0,2000) = TIME(0,33,22) = 0,023148 atau 12:33:20 AM`

{% hint style="info" %}
#### Keterangan

Nilai waktu adalah bagian dari nilai tanggal dan dinyatakan oleh angka desimal \(contoh, 12:00 PM ditampilkan sebagai 0,5 karena setengah dari hari\).
{% endhint %}

### Contoh

| **Jam** | **Menit** | **Detik** |
| :--- | :--- | :--- |
| 12 | {0} | 0 |
| 16 | 48 | 10 |
| **Rumus** | **Deskripsi** | **Hasil** |
| `=TIME(A2,B2,C2)` | Bagian desimal dari suatu hari, untuk waktu yang ditentukan di baris 2 \(12 jam, 0, menit, 0 detik\) | 0,5 |
| `=TIME(A3,B3,C3)` | Bagian desimal dari suatu hari, untuk waktu yang ditentukan di baris 3 \(16 jam, 48 menit, 10 detik\) | 0,7001157 |

