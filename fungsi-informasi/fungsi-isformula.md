# Fungsi ISFORMULA

### Deskripsi

Memeriksa apakah ada referensi ke sel yang berisi rumus, dan mengembalikan TRUE atau FALSE.

### Sintaks

ISFORMULA\(reference\)

Sintaks fungsi ISFORMULA memiliki argumen berikut.

*  **Reference**    Diperlukan. Reference adalah referensi ke sel yang ingin Anda uji. Referensi dapat berupa referensi sel, rumus, atau nama yang merujuk pada suatu sel.

### Keterangan

* Jika referensi bukan merupakan tipe data yang valid, misalnya nama yang ditentukan yang bukan merupakan referensi, ISFORMULA mengembalikan nilai kesalahan \#VALUE!.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =TODAY\(\) | Mengembalikan TRUE karena =TODAY\(\) adalah sebuah rumus. | TRUE |
| 7 | Mengembalikan FALSE karena 7 adalah angka, bukan rumus. | FALSE |
| Halo, dunia! | Mengembalikan FALSE karena "Halo, dunia!" adalah teks, bukan rumus. | FALSE |
| =3/0 | Mengembalikan TRUE karena, meskipun membagi dengan 0 menghasilkan kesalahan, sel berisi sebuah rumus. | TRUE |

