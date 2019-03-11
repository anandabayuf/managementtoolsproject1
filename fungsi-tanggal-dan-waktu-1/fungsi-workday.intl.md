# Fungsi WORKDAY.INTL

### Pengertian

Mengembalikan nomor seri tanggal sebelum atau setelah jumlah hari kerja yang ditentukan dengan parameter akhir pekan kustom. Parameter akhir pekan menunjukkan jumlah dan hari mana saja yang termasuk akhir pekan. Hari-hari akhir pekan dan hari yang ditentukan sebagai hari libur tidak dianggap hari kerja.

### Sintaks

`WORKDAY.INTL(start_date, days, [weekend], [holidays])`

Sintaks fungsi `WORKDAY.INTL` memiliki argumen berikut:

* **`Start_date`**    Diperlukan. Tanggal mulai, dipotong menjadi bilangan bulat.
* **`Days`**    Diperlukan. Jumlah hari kerja sebelum atau setelah `start_date`. Nilai positif menghasilkan tanggal mendatang, nilai negatif menghasilkan tanggal lampau, nilai nol mengembalikan `start_date`. Offset hari dipotong menjadi bilangan bulat.
* **`Weekend`**    Opsional. Menunjukkan hari dalam seminggu yang merupakan akhir pekan dan tidak dianggap hari kerja. Akhir pekan adalah jumlah akhir pekan atau string yang menentukan kapan akhir pekan terjadi.

  Nilai angka akhir pekan menunjukkan hari-hari akhir pekan berikut ini:

| **angka akhir pekan** | **Hari-hari akhir pekan** |
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

Nilai string akhir pekan panjangnya tujuh karakter dan setiap karakter dalam string menunjukkan satu hari dalam seminggu, dimulai dengan Senin. **1** mewakili hari libur dan **0** mewakili hari kerja. Hanya karakter **1** dan **0** yang diperbolehkan dalam string. **1111111**adalah string yang tidak valid.

Sebagai contoh, **0000011** akan mengembalikan akhir pekan yaitu Sabtu dan Minggu.

* **`Hari Libur`**    Opsional. Serangkaian tanggal opsional yang terdiri dari satu atau lebih tanggal yang akan dikecualikan dalam kalender hari kerja. Hari libur harus berupa rentang sel yang berisi tanggal, atau konstanta array dari nomor seri yang menunjukkan tanggal-tanggal tersebut. Urutan tanggal atau nilai seri dalam hari libur dapat berubah-ubah.

{% hint style="info" %}
### Keterangan

* Jika tanggal mulai di luar rentang untuk nilai basis tanggal saat ini, `WORKDAY.INTL` mengembalikan nilai kesalahan `#NUM!`.
* Jika tanggal dalam hari libur berada di luar rentang untuk nilai basis tanggal saat ini, `WORKDAY.INTL` mengembalikan nilai kesalahan `#NUM!`.
* Jika tanggal mulai plus day-offset mengembalikan tanggal yang tidak valid, `WORKDAY.INTL` mengembalikan nilai kesalahan `#NUM!`.
* Jika string akhir pekan panjangnya tidak valid atau berisi karakter yang tidak valid, `WORKDAY.INTL` mengembalikan nilai kesalahan `#VALUE!`.
{% endhint %}

### Contoh

| **Rumus** | **Deskripsi** | **Hasil Langsung** |
| :--- | :--- | :--- |
| `=WORKDAY.INTL(DATE(2012,1,1),30,0)` | Menggunakan 0 untuk hasil argumen Weekend dalam kesalahan \#NUM!. | `#NUM!` |
| `=WORKDAY.INTL(DATE(2012,1,1),90,11)` | Mencari tanggal 90 hari kerja dari 1/1/2012, hanya menghitung hari Minggu sebagai hari akhir pekan \(argumen Weekend adalah 11\). | 41013 |
| `=TEXT(WORKDAY.INTL(DATE(2012,1,1),30,17),"m/dd/yyyy")` | Menggunakan fungsi `TEXT` untuk memformat nomor seri yang dihasilkan \(40944\) dalam format "m/dd/yyyy". Mencari tanggal 30 hari kerja dari 1/1/2012, hanya menghitung hari Sabtu sebagai hari akhir pekan \(argumen Weekend adalah 17\). | 2/05/2012 |

