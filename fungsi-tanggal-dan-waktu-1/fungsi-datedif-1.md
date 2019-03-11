# Fungsi DATEDIF

### Pengertian

Menghitung jumlah hari, bulan, atau tahun di antara dua tanggal. **Peringatan:** Excel menyediakan fungsi `DATEDIF` untuk mendukung buku kerja yang lebih lama dari Lotus 1-2-3. Fungsi `DATEDIF` dapat menghasilkan jumlah yang salah dengan skenario tertentu. Silakan lihat bagian masalah umum dari artikel ini untuk detail selengkapnya.

### Sintaks

```text
DATEDIF(start_date,end_date,satuan)
```

**`Start_date`**    Tanggal yang menunjukkan tanggal yang lebih dahulu, atau tanggal dimulainya periode. Tanggal mungkin dimasukkan sebagai string teks di dalam tanda kutip \(misalnya, "2001/1/30"\), sebagai nomor seri \(misalnya, 36921, yang menyatakan 30 Januari 2001, jika Anda menggunakan sistem tanggal 1900\), atau seperti hasil dari rumus atau fungsi lain \(misalnya, `DATEVALUE("2001/1/30")`\).

**`End_date`**    Tanggal yang menunjukkan tanggal terakhir, atau tanggal berakhirnya periode.

**Catatan:** Jika **`Start_date`** lebih besar daripada **`End_date`**, hasilnya akan berupa `#NUM!`.

**Satuan**    Tipe informasi yang Anda inginkan untuk dikembalikan:

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Satuan</b>
      </th>
      <th style="text-align:left"><b>Mengembalikan</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&quot;Y&quot;</td>
      <td style="text-align:left">Jumlah tahun yang sudah berlalu dalam periode.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;M&quot;</td>
      <td style="text-align:left">Jumlah bulan yang sudah berlalu dalam periode.</td>
    </tr>
    <tr>
      <td style="text-align:left">:d</td>
      <td style="text-align:left">Jumlah hari dalam periode.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;MD&quot;</td>
      <td style="text-align:left">
        <p>Selisih antara hari dalam <code>start_date</code> dan <code>end_date</code>.
          Bulan dan tahun dari tanggal diabaikan.</p>
        <p><b>Penting:</b> Kami tidak menyarankan Anda menggunakan argumen &quot;MD&quot;,
          karena ada batasan yang diketahui dengannya. Lihat bagian masalah umum
          di bawah ini.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;YM&quot;</td>
      <td style="text-align:left">Selisih antara bulan dalam <code>start_date</code> dan <code>end_date</code>.
        Hari dan tahun dari tanggal diabaikan</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;YD&quot;</td>
      <td style="text-align:left">Selisih antara hari dalam <code>start_date</code> dan <code>end_date</code>.
        Tahun dari tanggal diabaikan.</td>
    </tr>
  </tbody>
</table>#### Keterangan

* Tanggal disimpan sebagai nomor seri yang berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 31 Desember 1899 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.
* Fungsi `DATEDIF` berguna dalam rumus di mana Anda perlu menghitung usia.

### Contoh

| **Start\_date** | **End\_date** | **Rumus** | **Deskripsi \(Hasil\)** |
| :--- | :--- | :--- | :--- |
| 1/1/2001 | 1/1/2003 | `=DATEDIF(Start_date,End_date,"Y")` | Dua tahun berlalu dalam periode \(2\) |
| 6/1/2001 | 8/15/2002 | `=DATEDIF(Start_date,End_date,"D")` | 440 hari di antara 1 Juni 2001 dan 15 Agustus 2002 \(440\) |
| 6/1/2001 | 8/15/2002 | `=DATEDIF(Start_date,End_date,"YD")` | 75 hari di antara 1 Juni dan 15 Agustus, dan mengabaikan tahun dari tanggal \(75\) |

### Masalah yang diketahui

Argumen "MD" mungkin menghasilkan angka negatif, nilai nol, atau hasil yang tidak akurat. Jika Anda mencoba menghitung sisa hari setelah bulan yang diselesaikan terakhir, berikut ini adalah solusinya:

![=DATEDIF\(D17,E17,&quot;md&quot;\) dan hasilnya: 5](https://support.content.office.net/id-id/media/a50cd076-9f82-47e6-83a5-6f408a682f84.png)

Rumus ini mengurangi hari pertama dalam bulan akhir \(5/1/2016\) dari tanggal akhir asli di sel E17 \(5/6/2016\). Berikut ini cara rumus tersebut melakukannya: Pertama, fungsi `DATE` membuat tanggal, 5/1/2016. Fungsi tersebut membuatnya menggunakan tahun di sel E17, dan bulan dalam sel E17. Kemudian **1** mewakili hari pertama dalam bulan tersebut. Hasil untuk fungsi `DATE` adalah 5/1/2016. Kemudian, kita menguranginya dari tanggal akhir asli di sel E17, yaitu 5/6/2016. 5/6/2016 minus 5/1/2016 adalah 5 hari.

{% page-ref page="fungsi-tanggal-dan-waktu.md" %}

