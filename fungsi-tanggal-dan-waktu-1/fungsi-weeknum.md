# Fungsi WEEKNUM

### Pengertian

Mengembalikan nomor minggu tanggal tertentu. Misalnya, minggu yang berisi tanggal 1 Januari adalah minggu pertama dalam setahun, dan diberi nomor minggu 1.

Ada dua sistem yang digunakan untuk fungsi ini:

* **`Sistem 1`**    Minggu yang berisi tanggal 1 Januari adalah minggu pertama dalam setahun, dan diberi nomor minggu 1.
* **`Sistem 2`**    Minggu yang berisi Kamis pertama dalam setahun adalah minggu pertama tahun tersebut, dan diberi nomor minggu 1. Sistem ini adalah metodologi yang ditetapkan dalam ISO 8601, yang umum dikenal sebagai sisten penomoran minggu Eropa.

### Sintaks

`WEEKNUM(serial_number,[return_type])`

Sintaks fungsi `WEEKNUM` memiliki argumen berikut:

* **`Serial_number`**     Diperlukan. Tanggal dalam minggu. Tanggal harus dimasukkan dengan menggunakan fungsi DATE, atau sebagai hasil dari rumus atau fungsi lain. Contoh, gunakan DATE\(2008,5,23\) untuk tanggal 23 Mei 2008. Masalah bisa muncul jika tanggal dimasukkan sebagai teks.
* **`Return_type`**     Opsional. Angka yang menentukan pada hari apa minggu dimulai. Nilai default adalah 1.

| **Return\_type** | **Awal minggu** | **Sistem** |
| :--- | :--- | :--- |
| 1 atau dihilangkan | Minggu | 1 |
| 2 | Senin | 1 |
| 11 | Senin | 1 |
| 1.2 | Selasa | 1 |
| 1,3 | Rabu | 1 |
| 14 | Kamis | 1 |
| 15 | Jumat | 1 |
| 16 | Sabtu | 1 |
| 17 | Minggu | 1 |
| 2,1 | Senin | 2 |

{% hint style="info" %}
#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri yang berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1. 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.
* Jika Serial\_number di luar rentang untuk nilai basis tanggal saat ini, kesalahan `#NUM!` akan dikembalikan.
* Jika `Return_type` di luar rentang yang ditentukan dalam tabel di atas, kesalahan `#NUM!` akan dikembalikan.
{% endhint %}

### Contoh

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Data</b>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">3/9/2012</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Rumus</b>
      </td>
      <td style="text-align:left"><b>Deskripsi</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><b>Hasil</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=WEEKNUM(A2)</code>
      </td>
      <td style="text-align:left">Jumlah minggu dalam tahun terjadinya 09/03/2012, berdasarkan minggu-minggu
        yang dimulai hari Minggu (default).</td>
      <td style="text-align:left">10</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=WEEKNUM(A2,2)</code>
      </td>
      <td style="text-align:left">Jumlah minggu dalam tahun terjadinya 09/03/2012, berdasarkan minggu-minggu
        yang dimulai hari Senin (argumen kedua, 2).</td>
      <td style="text-align:left">11</td>
    </tr>
  </tbody>
</table>