# Fungsi NOW

### Pengertian

Mengembalikan nomor seri tanggal dan waktu saat ini. Jika sebelum fungsi dimasukkan format selnya **Umum**, Excel mengubah sel format sehingga cocok dengan format tanggal dan waktu pengaturan regional Anda. Anda dapat mengubah format tanggal dan waktu dalam grup **Angka** di tab **Beranda** di Pita.

Fungsi **`NOW`** berguna ketika Anda perlu menampilkan tanggal dan waktu saat ini di atas lembar kerja atau menghitung nilai berdasarkan tanggal dan waktu saat ini, dan memperbarui nilai tersebut setiap Anda membuka lembar kerja.

{% hint style="info" %}
**Catatan:** Jika fungsi **`NOW`** tidak memperbarui nilai sel seperti yang Anda inginkan, Anda mungkin perlu mengubah pengaturan yang mengendalikan kapan buku kerja atau lembar kerja menghitung ulang. Pengaturan ini dapat diubah di Panel Kontrol untuk aplikasi desktop Excel.
{% endhint %}

### Sintaks

`NOW`

Sintaks fungsi NOW tidak memiliki argumen.

#### Keterangan

* Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.447 hari setelah 1 Januari 1900.
* Angka di sebelah kanan koma desimal dalam nomor seri menunjukkan waktu; angka di sebelah kiri menunjukkan tanggal. Misalnya, nomor seri 0,5 menunjukkan waktu pukul 12:00 siang.
* Hasil fungsi **`NOW`** hanya berubah ketika lembar kerja dihitung atau ketika sebuah makro yang berisi fungsi dijalankan. Fungsi itu tidak diperbarui secara terus-menerus.

### Contoh

| **Rumus** | **Deskripsi** | **Hasil** |
| :--- | :--- | :--- |
| `=NOW()` | Mengembalikan tanggal dan waktu saat ini. | 06/11/2011 19:03 |
| `=NOW()-0,5` | Mengembalikan tanggal dan waktu 12 jam lalu \(-0,5 hari yang lalu\). | 06/11/2011 07:03 |
| `=NOW()+7` | Mengembalikan tanggal dan waktu 7 hari mendatang. | 13/11/2011 19:03 |
| `=NOW()-2,25` | Mengembalikan tanggal dan waktu 2 hari dan 6 jam lalu \(-2,25 hari yang lalu\). | 04/11/2011 13:03 |

