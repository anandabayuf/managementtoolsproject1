# Fungsi ISEVEN

### Deskripsi

Mengembalikan TRUE jika bilangannya genap, atau FALSE jika bilangannya ganjil.

### Sintaks

ISEVEN\(number\)

Sintaks fungsi ISEVEN memiliki argumen berikut:

*  **Angka**    Diperlukan. Nilai untuk menguji. Jika bilangannya bukan bilangan bulat, maka bilangan tersebut dipotong.

### Keterangan

Jika angkanya nonnumerik, maka ISEVEN mengembalikan nilai kesalahan \#VALUE!.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =ISEVEN\(-1\) | Menguji apakah -1 genap | FALSE |
| =ISEVEN\(2,5\) | Memeriksa apakah 2,5 genap. Bagian desimal, ,5, terpotong, sehingga 2 diuji. | TRUE |
| =ISEVEN\(5\) | Menguji apakah 5 genap. | FALSE |
| =ISEVEN\(0\) | Nol \(0\) dianggap genap. | TRUE |
| 23/12/2011 | Menguji tanggal dalam A6. Representasi desimal dari 23/12/2011 adalah 40900. | TRUE |

