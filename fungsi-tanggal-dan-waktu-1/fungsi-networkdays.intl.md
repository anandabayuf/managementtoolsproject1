# Fungsi NETWORKDAYS.INTL

### Pengertian

Mengembalikan jumlah semua hari kerja di antara dua tanggal dengan menggunakan parameter untuk menunjukkan yang mana dan berapa hari yang merupakan akhir pekan. Hari-hari akhir pekan dan hari yang ditentukan sebagai hari libur tidak dianggap hari kerja.

### Sintaks

`NETWORKDAYS.INTL(start_date, end_date, [weekend], [holidays])`

Sintaks fungsi `NETWORKDAYS.INTL` memiliki argumen berikut:

* **`Start_date`, `end_date`**    Diperlukan. Tanggal-tanggal yang selisihnya akan dihitung. `Start_date` dapat lebih awal dari, sama dengan, atau setelah `end_date`.
* **`Weekend`**    Opsional. Menunjukkan hari-hari dalam seminggu yang merupakan akhir pekan dan tidak dimasukkan ke dalam jumlah semua hari kerja di antara `start_date` dan `end_date`. Akhir pekan adalah jumlah akhir pekan atau string yang menentukan kapan akhir pekan terjadi.

  Nilai jumlah akhir pekan menunjukkan hari-hari akhir pekan berikut ini:

| **Jumlah akhir pekan** | **Hari-hari akhir pekan** |
| :--- | :--- |
| 1 atau dihilangkan | Sabtu, Minggu |
| 2 | Minggu, Senin |
| 3 | Senin, Selasa |
| 4 | Selasa, Rabu |
| 5 | Rabu, Kamis |
| 6 | Kamis, Jumat |
| 7 | Jumat, Sabtu |
| 11 | Hanya Minggu |
| 1.2 | Hanya Senin |
| 1,3 | Hanya Selasa |
| 14 | Hanya Rabu |
| 15 | Hanya Kamis |
| 16 | Hanya Jumat |
| 17 | Hanya Sabtu |

Nilai string akhir pekan panjangnya tujuh karakter dan setiap karakter dalam string menyatakan hari dalam seminggu, dimulai dengan Senin. **1** menyatakan hari libur dan **0** menyatakan hari kerja. Hanya karakter **1** dan **0** yang diperbolehkan dalam string. Menggunakan **1111111** akan selalu mengembalikan **0**.

Sebagai contoh, **0000011** akan mengembalikan akhir pekan yaitu Sabtu dan Minggu.

* **`Holiday`**    Opsional. Serangkaian tanggal opsional yang terdiri dari satu atau lebih tanggal yang akan dikecualikan dalam kalender hari kerja. Hari libur harus berupa rentang sel yang berisi tanggal, atau konstanta array dari nomor seri yang menyatakan tanggal-tanggal tersebut. Urutan tanggal atau nilai seri dalam hari libur dapat berubah-ubah.

#### Keterangan

* Jika `start_date` setelah `end_date`, nilai yang dikembalikan akan negatif, dan besarannya adalah jumlah seluruh hari kerja.
* Jika `start_date` berada di luar rentang untuk nilai basis tanggal saat ini, `NETWORKDAYS.INTL` mengembalikan nilai kesalahan `#NUM!`.
* Jika `end_date` berada di luar rentang untuk nilai basis tanggal saat ini, `NETWORKDAYS.INTL` mengembalikan nilai kesalahan `#NUM!`.
* Jika string akhir pekan panjangnya tidak valid atau berisi karakter yang tidak valid, maka `NETWORKDAYS.INTL` mengembalikan nilai kesalahan `#VALUE!`.

### Contoh

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Rumus</b>
      </th>
      <th style="text-align:left"><b>Deskripsi</b>
      </th>
      <th style="text-align:left">
        <p></p>
        <p><b>Hasil</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>=NETWORKDAYS.INTL(DATE(2006,1,1),DATE(2006,1,31))</code>
      </td>
      <td style="text-align:left">Menghasilkan 22 hari kerja mendatang. Mengurangi 9 hari akhir pekan libur
        kerja (5 Sabtu dan 4 Minggu) dari total 31 hari di antara dua tanggal.
        Secara default, Sabtu dan Minggu adalah hari libur kerja.</td>
      <td style="text-align:left">2,2</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=NETWORKDAYS.INTL(DATE(2006,2,28),DATE(2006,1,31))</code>
      </td>
      <td style="text-align:left">Hasil -21, yaitu 21 hari kerja di masa lampau.</td>
      <td style="text-align:left">-21</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=NETWORKDAYS.INTL(DATE(2006,1,1),DATE(2006,2,1),7,{&quot;2006/1/2&quot;,&quot;2006/1/16&quot;})</code>
      </td>
      <td style="text-align:left">Mengembalikan 22 hari kerja mendatang dengan mengurangi 10 hari libur
        kerja (4 Jumat, 4 Sabtu, 2 Hari Libur) dari 32 hari antara 1 Januari 2006
        hingga 1 Februari 2006. Menggunakan 7 argumen untuk akhir pekan, yaitu
        Jumat dan Sabtu. Ada juga 2 hari libur dalam periode waktu ini.</td>
      <td
      style="text-align:left">2,2</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>=NETWORKDAYS.INTL(DATE(2006,1,1),DATE(2006,2,1),&quot;0010001&quot;,{&quot;2006/1/2&quot;,&quot;2006/1/16&quot;})</code>
      </td>
      <td style="text-align:left">Menghasilkan 22 hari kerja mendatang. Periode waktu sama seperti contoh
        langsung di atas, kecuali Minggu dan Rabu sebagai hari akhir pekan.</td>
      <td
      style="text-align:left">0,20</td>
    </tr>
  </tbody>
</table>