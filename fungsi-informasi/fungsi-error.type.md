# Fungsi ERROR.TYPE

### Deskripsi

Mengembalikan angka yang berhubungan dengan tipe kesalahan

### Sintaks

ERROR.TYPE\(error\_val\)

Sintaks fungsi ERROR.TYPE memiliki argumen berikut:

*  **Error\_val**    Diperlukan. Nilai kesalahan yang angka pengidentifikasinya ingin Anda temukan. Meskipun error\_val dapat menjadi nilai kesalahan aktual, biasanya nilai kesalahan itu akan menjadi referensi ke sel berisi rumus yang ingin Anda uji.



|  **Jika** **error\_val** **adalah** |  **ERROR.TYPE akan mengembalikan** |
| :--- | :--- |
| \#NULL! | 1 |
| \#DIV/0! | 2 |
| \#VALUE! | 3 |
| \#REF! | 4 |
| \#NAME? | 5 |
| \#NUM! | 6 |
| \#N/A | 7 |
| \#GETTING\_DATA | 8 |
| Yang lainnya | \#N/A |

### Contoh

Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.



|  **Data** |  |  |
| :--- | :--- | :--- |
| \#NULL! |  |  |
| \#DIV/0! |  |  |
|  **Rumus** |  **Deskripsi** |  **Hasil** |
| =ERROR.TYPE\(A2\) | Angka \#NULL! Error\(1\). | 1 |
| =IF\(ERROR.TYPE\(A3\)&lt;3,CHOOSE\(ERROR.TYPE\(A3\),"Rentang tidak beririsan","Pembagi adalah nol"\)\) | Memeriksa sel A3 untuk melihat apakah sel tersebut berisi nilai kesalahan \#NULL! atau pun nilai kesalahan \#DIV/0!. Jika ya, maka angka untuk nilai kesalahan digunakan dalam fungsi lembar kerja CHOOSE untuk menampilkan salah satu dari dua pesan; jika tidak, nilai kesalahan \#N/A dikembalikan. | Pembagi adalah nol |

