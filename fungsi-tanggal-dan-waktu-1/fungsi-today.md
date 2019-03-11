# Fungsi TODAY

### Pengertian

Mengembalikan nomor seri dari tanggal saat ini. Nomor seri adalah kode tanggal-waktu yang digunakan oleh Excel untuk perhitungan tanggal dan waktu. Jika format sel adalah **Umum** sebelum fungsi dimasukkan, Excel mengganti format sel ke **Tanggal**. Jika Anda ingin melihat nomor serinya, Anda harus mengganti format sel ke **Umum** atau **Angka**.

Fungsi **`TODAY`** berguna saat Anda perlu untuk menampilkan tanggal saat ini di lembar kerja, tidak peduli kapan Anda membuka buku kerja. Ini juga berguna untuk menghitung interval. Sebagai contoh, jika Anda tahu bahwa seseorang lahir pada tahun 1963, Anda mungkin ingin menggunakan rumus berikut untuk menemukan umur orang itu pada ulang tahunnya tahun ini:

**`=YEAR(TODAY())-1963`**

Rumus ini menggunakan fungsi **`TODAY`** sebagai argumen untuk fungsi **`YEAR`** untuk mendapatkan tahun saat ini, lalu menguranginya dengan 1963, mengembalikan umur orang itu.

{% hint style="info" %}
**Catatan:** Jika fungsi **`TODAY`** tidak memperbarui tanggal seperti yang Anda harapkan, Anda mungkin perlu mengubah pengaturan yang mengontrol kapan perhitungan ulang buku kerja atau lembar kerja dilakukan. Di tab **File**, klik **Opsi**, lalu di kategori **Rumus** di bawah **Opsi perhitungan**, pastikan **Otomatis** dipilih.
{% endhint %}

### Sintaks

`TODAY()`

Sintaks fungsi `TODAY` tidak memiliki argumen.

{% hint style="info" %}
**Catatan:** Microsoft Excel menyimpan tanggal sebagai nomor seri yang berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena tanggal itu adalah 39.447 hari setelah 1 Januari 1900.
{% endhint %}

### Contoh

| **Rumus** | **Deskripsi** | **Hasil** |
| :--- | :--- | :--- |
| `=TODAY()` | Mengembalikan tanggal saat ini. | 12/1/2011 |
| `=TODAY()+5` | Mengembalikan tanggal saat ini plus 5 hari. Misalnya, jika tanggal saat ini adalah 1/1/2012, formula ini mengembalikan 1/6/2012. | 12/6/2011 |
| `=DATEVALUE("1-1-2030")-TODAY()` | Mengembalikan jumlah hari antara tanggal saat ini dan 1/1/2030. Perhatikan bahwa sel A4 harus diformat sebagai Umum atau Angka untuk hasil agar ditampilkan dengan benar. | 1/31/1918 |
| `=DAY(TODAY())` | Mengembalikan hari saat ini dalam sebulan \(1 - 31\). | 1 |
| `=MONTH(TODAY())` | Mengembalikan hari saat ini dalam setahun \(1 - 12\). Misalnya, jika bulan saat ini adalah Mei, rumus ini mengembalikan 5. | 1.2 |

