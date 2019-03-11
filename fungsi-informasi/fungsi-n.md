# Fungsi N

### Deskripsi

Mengembalikan nilai yang dikonversikan menjadi angka.

### Sintaks

N\(value\)

Sintaks fungsi N memiliki argumen berikut:

*  **Value**    Diperlukan. Nilai yang ingin Anda konversikan. N mengonversikan nilai yang terdapat dalam tabel berikut ini.



|  **Jika nilai adalah atau merujuk ke** |  **N mengembalikan** |
| :--- | :--- |
| Sebuah angka | Angka tersebut |
| Sebuah tanggal, dalam salah satu format tanggal bawaan yang tersedia dalam Microsoft Excel | Nomor seri tanggal tersebut |
| TRUE | 1 |
| FALSE | {0} |
| Nilai kesalahan, seperti \#DIV/0! | Nilai kesalahan |
| Yang lainnya | {0} |

### Keterangan

* Pada umumnya tidak perlu digunakan fungsi N dalam rumus, karena Excel secara otomatis mengonversi nilai jika diperlukan. Fungsi ini disediakan agar kompatibel dengan program-program lembar bentang lainnya.
* Microsoft Excel menyimpan tanggal sebagai nomor seri yang berurutan sehingga bisa digunakan dalam perhitungan. Secara default, 1 Januari 1900 adalah nomor seri 1, dan 1 Januari 2008 adalah nomor seri 39448 karena 39.448 hari setelah 1 Januari 1900.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Data** |  |  |
| :--- | :--- | :--- |
| 7 |  |  |
| Genap |  |  |
| TRUE |  |  |
| 17/04/2011 |  |  |
|  **Rumus** |  **Deskripsi** |  **Hasil** |
| =N\(A2\) | Karena A2 berisi angka, angka itu dikembalikan. | 7 |
| =N\(A3\) | Karena A3 berisi teks, 0 dikembalikan. | {0} |
| =N\(A4\) | Karena A4 adalah nilai logika TRUE, 1 dikembalikan. | 1 |
| =N\(A5\) | Karena A5 adalah tanggal, nomor seri tanggal dikembalikan \(bervariasi dengan sistem tanggal yang digunakan\). | 40650 |
| =N\("7"\) | Karena "7" adalah teks, 0 dikembalikan. | {0} |

