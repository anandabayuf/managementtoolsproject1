# Fungsi EOMONTH

### Pengertian

Mengembalikan nomor seri untuk hari terakhir bulan yang merupakan nomor indikasi dari bulan sebelum atau setelah `start_date`. Gunakan `EOMONTH` untuk menghitung tanggal jatuh tempo yang jatuh pada hari terakhir bulan tersebut.

### Sintaks

`EOMONTH(start_date, months)`

Sintaks fungsi `EOMONTH` memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal yang mewakili tanggal mulai. Tanggal harus dimasukkan menggunakan fungsi `DATE`, atau sebagai hasil dari rumus atau fungsi lain. Sebagai contoh, gunakan `DATE(2008,5,23)` untuk tanggal 23 Mei 2008. Masalah dapat terjadi jika tanggal dimasukkan sebagai teks.
* **`Month`**    Diperlukan. Jumlah bulan sebelum atau setelah `start_date`. Nilai positif untuk bulan menghasilkan tanggal masa mendatang; nilai negatif menghasilkan tanggal lampau.

  **Catatan:** Jika bulan bukan bilangan bulat, maka dipotong.

### Keterangan

* Microsoft Excel menyimpan tanggal sebagai nomor seri berurutan sehingga bisa digunakan di dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.
* Jika `tanggal_mulai` bukan tanggal yang valid, `EOMONTH` akan mengembalikan nilai kesalahan `#NUM!`.
* Jika `tanggal_mulai` ditambah bulan mengembalikan tanggal yang tidak valid, `EOMONTH` akan mengembalikan nilai kesalahan `#NUM!`.

### Contoh

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Tanggal</b>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1-Jan-11</td>
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
      <td style="text-align:left"><code>=EOMONTH(A2,1)</code>
      </td>
      <td style="text-align:left">Tanggal hari terakhir dalam bulan, satu bulan setelah tanggal dalam A2.</td>
      <td
      style="text-align:left">28/02/2011</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=EOMONTH(A2,-3)</code>
      </td>
      <td style="text-align:left">Tanggal hari terakhir dalam bulan, tiga bulan sebelum tanggal dalam A2.</td>
      <td
      style="text-align:left">31/10/2010</td>
    </tr>
  </tbody>
</table>