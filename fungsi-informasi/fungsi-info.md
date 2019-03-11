# Fungsi INFO

### Deskripsi

Mengembalikan informasi tentang lingkungan operasi saat ini.

### Sintaks

INFO\(type\_text\)

Sintaks fungsi INFO memiliki argumen ini:

*  **Type\_text**    Diperlukan. Teks yang menentukan tipe informasi apa yang Anda inginkan dikembalikan.



<table>
  <thead>
    <tr>
      <th style="text-align:left"> <b>Type_text</b>
      </th>
      <th style="text-align:left"> <b>Mengembalikan</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&quot;directory&quot;</td>
      <td style="text-align:left">Jalur direktori atau folder saat ini.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;numfile&quot;</td>
      <td style="text-align:left">Jumlah lembar kerja aktif di dalam buku kerja yang terbuka.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;origin&quot;</td>
      <td style="text-align:left">
        <p>Mengembalikan referensi sel absolut sel paling atas dan sel paling kiri
          yang tampak di jendela, berdasarkan posisi gulir saat ini, sebagai teks
          yang diawali dengan &quot;$A:&quot;. Nilai ini ditujukan untuk kompatibel
          dengan Lotus 1-2-3 rilis 3.x. Nilai sebenarnya yang dikembalikan bergantung
          pada pengaturan gaya referensi saat ini. Menggunakan D9 sebagai contoh,
          nilai yang dikembalikan adalah sebagai berikut:</p>
        <ul>
          <li> <b>Gaya referensi A1</b> &quot;$A:$D$9&quot;.</li>
          <li> <b>Gaya referensi R1C1</b> &quot;$A:R9C4&quot;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;osversion&quot;</td>
      <td style="text-align:left">Versi sistem operasi saat ini, sebagai teks.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;recalc&quot;</td>
      <td style="text-align:left">Mode rekalkulasi saat ini; mengembalikan &quot;Automatic&quot; atau &quot;Manual&quot;.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;release&quot;</td>
      <td style="text-align:left">Versi Microsoft Excel, sebagai teks.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;system&quot;</td>
      <td style="text-align:left">Nama lingkungan operasi:
        <br />Macintosh = &quot;mac&quot;
        <br />Windows = &quot;pcdos&quot;</td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
 **Penting:** Dalam versi Microsoft Excel yang sebelumnya, nilai "memavail", "memused", dan "totmem" type\_text mengembalikan informasi memori. Jenis-jenis type\_text ini tidak lagi tersedia dan sekarang mengembalikan nilai kesalahan \#N/A.
{% endhint %}

### Contoh

Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.



|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| '=INFO\("numfile"\) | Jumlah lembar kerja aktif | INFO\("numfile"\) |
| '=INFO\("recalc"\) | Mode perhitungan ulang untuk buku kerja. | =INFO\("recalc"\) |



