# Fungsi WEEKDAY

### Pengertian

Mengembalikan hari yang tekait dengan sebuah tanggal. Hari diberikan sebagai bilangan bulat, yang berkisar dari 1 \(Minggu\) sampai 7 \(Sabtu\), secara default.

### Sintaks

`WEEKDAY(serial_number,[return_type])`

Sintaks fungsi `WEEKDAY` memiliki argumen berikut:

* **`Serial_number`**    Diperlukan. Nomor berurutan yang menunjukkan tanggal dari hari yang akan dicari. Tanggal harus dimasukkan dengan menggunakan fungsi `DATE`, atau sebagai hasil dari rumus atau fungsi lain. Contoh, gunakan `DATE(2008,5,23)` untuk tanggal 23 Mei 2008. Masalah bisa muncul jika tanggal dimasukkan sebagai teks.
* **`Return_type`**    Opsional. Angka yang menentukan tipe nilai yang dikembalikan.

| **Return\_type** | **Angka yang dikembalikan** |
| :--- | :--- |
| 1 atau dihilangkan | Angka 1 \(Minggu\) sampai 7 \(Sabtu\). Perilakunya sama seperti versi Microsoft Excel sebelumnya. |
| 2 | Angka 1 \(Senin\) sampai 7 \(Minggu\). |
| 3 | Angka 0 \(Senin\) sampai 6 \(Minggu\). |
| 11 | Angka 1 \(Senin\) sampai 7 \(Minggu\). |
| 1.2 | Angka 1 \(Selasa\) sampai 7 \(Senin\). |
| 1,3 | Angka 1 \(Rabu\) sampai 7 \(Selasa\). |
| 14 | Angka 1 \(Kamis\) sampai 7 \(Rabu\). |
| 15 | Angka 1 \(Jumat\) sampai 7 \(Kamis\). |
| 16 | Angka 1 \(Sabtu\) sampai 7 \(Kamis\). |
| 17 | Angka 1 \(Minggu\) sampai 7 \(Sabtu\). |

{% hint style="info" %}
#### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan di dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena tanggal itu adalah 39.448 hari setelah 1 Januari 1900.
* Jika nomor\_seri di luar rentang untuk nilai basis tanggal saat ini, kesalahan `#NUM!` akan dikembalikan.
* Jika `return_type` di luar rentang yang ditentukan dalam tabel di atas, kesalahan `#NUM!` akan dikembalikan.
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
      <td style="text-align:left">14/02/2008</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Rumus</b>
      </td>
      <td style="text-align:left"><b>Deskripsi (Hasil)</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><b>Hasil</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=WEEKDAY(A2)</code>
      </td>
      <td style="text-align:left">Hari dalam minggu, dengan angka 1 (Minggu) hingga 7 (Sabtu) (5)</td>
      <td
      style="text-align:left">5</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=WEEKDAY(A2, 2)</code>
      </td>
      <td style="text-align:left">Hari dalam minggu, dengan angka 1 (Senin) hingga 7 (Minggu) (4)</td>
      <td
      style="text-align:left">4</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=WEEKDAY(A2, 3)</code>
      </td>
      <td style="text-align:left">Hari dalam minggu, dengan angka 0 (Senin) hingga 6 (Minggu) (3)</td>
      <td
      style="text-align:left">3</td>
    </tr>
  </tbody>
</table>