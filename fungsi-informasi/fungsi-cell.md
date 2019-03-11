# Fungsi CELL

### Deskripsi

Fungsi CELL mengembalikan informasi tentang pemformatan, lokasi, atau konten sel. Misalnya, jika Anda ingin melakukan verifikasi bahwa sebuah sel berisi nilai numerik dan bukan teks sebelum Anda melakukan perhitungan, Anda dapat menggunakan rumus berikut:

 **=** **IF\(** **CELL\("type", A1\) = "v", A1 \* 2, 0\)**

Rumus ini menghitung A1\*2 hanya jika sel A1 berisi nilai numerik, dan mengembalikan 0 jika A1 berisi teks atau kosong.

### Sintaks

CELL\(info\_type, \[reference\]\)

Sintaks fungsi CELL memiliki argumen berikut:

*  **Info\_type**    Diperlukan. Nilai teks yang menentukan tipe informasi sel apa yang ingin Anda hasilkan. Daftar berikut menampilkan kemungkinan nilai argumen Info\_type dan hasil-hasil terkait.

<table>
  <thead>
    <tr>
      <th style="text-align:left">info_type</th>
      <th style="text-align:left">Mengembalikan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&quot;address&quot;</td>
      <td style="text-align:left">Referensi sel pertama dalam referensi, sebagai teks.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;col&quot;</td>
      <td style="text-align:left">Nomor kolom sel dalam referensi.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;color&quot;</td>
      <td style="text-align:left">
        <p>Nilai 1 jika sel diformat dengan warna untuk nilai negatif; jika tidak,
          mengembalikan 0 (nol).</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;contents&quot;</td>
      <td style="text-align:left">Nilai sel kiri atas dalam referensi; bukan rumus.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;filename&quot;</td>
      <td style="text-align:left">
        <p>Filename (termasuk jalur lengkap) file yang berisi referensi, sebagai
          teks. Mengembalikan teks kosong (&quot;&quot;) jika lembar kerja yang berisi
          referensi belum disimpan.</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;format&quot;</td>
      <td style="text-align:left">
        <p>Nilai teks terkait format angka sel. Nilai teks untuk berbagai format
          diperlihatkan dalam tabel berikut. Mengembalikan &quot;-&quot; di akhir
          nilai teks jika sel diformat berwarna untuk nilai negatif. Mengembalikan
          &quot;()&quot; di akhir nilai teks jika sel diformat dengan tanda kurung
          untuk nilai positif atau semua nilai.</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;parentheses&quot;</td>
      <td style="text-align:left">
        <p>Nilai 1 jika sel diformat dengan tanda kurung untuk nilai positif atau
          semua nilai; jika tidak, mengembalikan 0.</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;prefix&quot;</td>
      <td style="text-align:left">
        <p>Nilai teks terkait &quot;label prefix&quot; sel. Mengembalikan tanda kutip
          tunggal (&apos;) jika sel berisi teks rata kiri, tanda petik ganda (&quot;)
          jika sel berisi teks rata kanan, tanda sisipan (^) jika sel berisi teks
          rata tengah, garis miring terbalik (\) jika sel itu berisi teks rata isi,
          dan teks kosong (&quot;&quot;) jika sel berisi hal lain.</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;protect&quot;</td>
      <td style="text-align:left">
        <p>Nilai 0 jika sel tidak dikunci; jika tidak, mengembalikan 1 jika sel dikunci.</p>
        <p><b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;row&quot;</td>
      <td style="text-align:left">Nomor baris sel dalam referensi.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;type&quot;</td>
      <td style="text-align:left">Nilai teks terkait tipe data dalam sel. Mengembalikan &quot;b&quot; untuk
        kosong jika sel kosong, &quot;l&quot; untuk label jika sel berisi konstanta
        teks, dan &quot;v&quot; untuk nilai jika sel berisi sesuatu yang lain.</td>
    </tr>
    <tr>
      <td style="text-align:left">&quot;width&quot;</td>
      <td style="text-align:left">
        <p>Lebar kolom sel, yang dibulatkan ke bilangan bulat. Masing-masing unit
          lebar kolom sama dengan lebar satu karakter dalam ukuran font default.</p>
        <p> <b>Catatan:</b> Nilai ini tidak didukung di Excel Online, Excel Mobile,
          dan Excel Starter.</p>
      </td>
    </tr>
  </tbody>
</table>*  **Referensi**    Opsional. Sel yang Anda inginkan informasinya. Jika dihilangkan, informasi yang ditentukan dalam argumen Info\_type dikembalikan untuk sel terakhir yang diubah. Jika argumen referensi adalah rentang sel, fungsi CELL mengembalikan informasi hanya untuk sel kiri atas rentang tersebut.

### Kode Format CELL

Daftar berikut menguraikan nilai teks yang dikembalikan fungsi CELL ketika argumen Info\_type adalah "format" dan argumen referensi adalah sel yang diformat dengan format angka bawaan.

|  **Jika format Excel adalah** |  **Fungsi CELL mengembalikan** |
| :--- | :--- |
| Umum | "G" |
| 0 | "F0" |
| \#,\#\#0 | ",0" |
| 0.00 | "F2" |
| \#,\#\#0.00 | ",2" |
| $\#,\#\#0\_\);\($\#,\#\#0\) | "C0" |
| $\#,\#\#0\_\);\[Red\]\($\#,\#\#0\) | "C0-" |
| $\#,\#\#0.00\_\);\($\#,\#\#0.00\) | "C2" |
| $\#,\#\#0.00\_\);\[Red\]\($\#,\#\#0.00\) | "C2-" |
| 0% | "P0" |
| 0.00% | "P2" |
| 0.00E+00 | "S2" |
| \#?/? atau \#??/?? | "G" |
| m/d/yy atau m/d/yy h:mm atau mm/dd/yy | "D4" |
| d-mmm-yy atau dd-mmm-yy | "D1" |
| d-mmm atau dd-mmm | "D2" |
| mmm-yy | "D3" |
| mm/dd | "D5" |
| h:mm AM/PM | "D7" |
| h:mm:ss AM/PM | "D6" |
| h:mm | "D9" |
| h:mm:ss | "D8" |

{% hint style="info" %}
 **Catatan:** Jika argumen Info\_type dalam fungsi CELL adalah "format" dan kemudian Anda menerapkan format lain ke sel referensi, Anda harus menghitung ulang lembar kerja tersebut untuk memperbarui hasil fungsi CELL.
{% endhint %}

### Contoh

| Data |
| :--- |
| 75 |
| Halo, dunia! |

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =CELL\("row", A20\) | Jumlah baris sel A20. | 20 |
| =CELL\("content", A3\) | Konten sel A3. | Halo, dunia! |
| =CELL\("type", A2\) | Tipe data sel A2. Tipe data "v" mengindikasikan nilai. | v |



