# Fungsi ISNA



### Deskripsi

Masing-masing fungsi ini, secara kolektif disebut fungsi **IS**, memeriksa nilai tertentu dan mengembalikan TRUE atau FALSE bergantung pada hasilnya. Misalnya, fungsi **ISBLANK** mengembalikan nilai logika TRUE jika argumen nilainya merupakan referensi ke sel kosong; jika tidak maka fungsi ini mengembalikan FALSE.

Anda bisa menggunakan fungsi **IS** untuk mendapatkan informasi tentang sebuah nilai sebelum melakukan perhitungan atau tindakan lainnya dengannya. Misalnya, Anda dapat menggunakan fungsi **ISERROR** bersama fungsi **IF** untuk melakukan tindakan berbeda jika timbul kesalahan:

 **=** **IF\(** **ISERROR\(A1\), "An error occurred.", A1 \* 2\)**

Rumus ini memeriksa apakah ada kondisi kesalahan di A1. Jika ada, maka fungsi **IF** mengembalikan pesan "Terjadi kesalahan." Jika tidak ada kesalahan, maka fungsi **IF** melakukan perhitungan A1\*2.

### Sintaks

ISBLANK\(nilai\)

ISERR\(nilai\)

ISERROR\(nilai\)

ISLOGICAL\(nilai\)

ISNA\(nilai\)

ISNONTEXT\(nilai\)

ISNUMBER\(nilai\)

ISREF\(nilai\)

ISTEXT\(nilai\)

Sintaks fungsi **IS** memiliki argumen berikut:

*  **nilai**    Diperlukan. Nilai yang ingin Anda uji. Argumen nilai dapat berupa kesalahan, nilai logika, teks, angka, atau nilai referensi kosong \(sel kosong\), atau nama yang merujuk ke salah satu dari ini.



|  **Fungsi** |  **Mengembalikan TRUE jika** |
| :--- | :--- |
| ISBLANK | Nilai merujuk ke sel kosong. |
| ISERR | Nilai merujuk ke nilai kesalahan kecuali \#N/A. |
| ISERROR | Nilai yang merujuk ke setiap nilai kesalahan \(\#N/A, \#VALUE!, \#REF!, \#DIV/0!, \#NUM!, \#NAME?, atau \#NULL!\). |
| ISLOGICAL | Nilai yang merujuk ke nilai logika. |
| ISNA | Nilai yang merujuk ke nilai kesalahan \#N/A \(nilai tidak tersedia\). |
| ISNONTEXT | Nilai yang merujuk ke item yang bukan teks. \(Perhatikan bahwa fungsi ini mengembalikan TRUE jika nilainya merujuk ke sel kosong.\) |
| ISNUMBER | Nilai yang merujuk ke sebuah angka. |
| ISREF | Nilai yang merujuk ke sebuah referensi. |
| ISTEXT | Nilai yang merujuk ke teks. |

### Keterangan

*  Argumen nilai fungsi **IS** tidak dikonversi. Nilai numerik yang berada di antara tanda kutip ganda diperlakukan sebagai teks. Misalnya, pada banyak fungsi lain di mana angka diperlukan, nilai teks "19" dikonversikan menjadi angka 19. Akan tetapi, di dalam rumus **ISNUMBER\("19"\)**, "19" tidak dikonversikan dari nilai teks menjadi nilai angka, dan fungsi **ISNUMBER** mengembalikan FALSE.
*  Fungsi **IS** berguna dalam rumus-rumus untuk menguji hasil dari sebuah perhitungan. Ketika dikombinasikan dengan fungsi **IF**, fungsi-fungsi ini menyediakan metode untuk menemukan kesalahan di dalam rumus \(lihat contoh-contoh berikut ini\).

### Contoh

#### Contoh 1



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =ISLOGICAL\(TRUE\) | Memeriksa apakah TRUE adalah nilai logika | TRUE |
| =ISLOGICAL\("TRUE"\) | Memeriksa apakah "TRUE" adalah nilai logika | FALSE |
| =ISNUMBER\(4\) | Memeriksa apakah 4 sebuah angka | TRUE |
| =ISREF\(G8\) | Memeriksa apakah G8 adalah referensi valid | TRUE |
| =ISREF\(XYZ1\) | Memeriksa apakah XYZ1 adalah referensi valid | FALSE |

#### Contoh 2



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Data** |  |  |
| :--- | :--- | :--- |
| Emas |  |  |
| Wilayah1 |  |  |
| \#REF! |  |  |
| 330,92 |  |  |
| \#N/A |  |  |
|  **Rumus** |  **Deskripsi** |  **Hasil** |
| =ISBLANK\(A2\) | Memeriksa apakah sel A2 kosong. | FALSE |
| =ISERROR\(A4\) | Memeriksa apakah nilai dalam sel A4, \#REF!, adalah kesalahan. | TRUE |
| =ISNA\(A4\) | Memeriksa apakah nilai dalam sel A4, \#REF!, adalah kesalahan \#N/A. | FALSE |
| =ISNA\(A6\) | Memeriksa apakah nilai dalam sel A6, \#N/A, adalah kesalahan \#N/A. | TRUE |
| =ISERR\(A6\) | Memeriksa apakah nilai dalam sel A6, \#N/A, adalah kesalahan. | FALSE |
| =ISNUMBER\(A5\) | Memeriksa apakah nilai dalam sel A5, 330,92, adalah sebuah angka. | TRUE |
| =ISTEXT\(A3\) | Memeriksa apakah nilai dalam sel A3, Wilayah1, adalah teks. | TRUE |

