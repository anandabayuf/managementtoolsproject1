# Fungsi SHEETS

### Deskripsi

Mengembalikan jumlah lembar dalam sebuah referensi.

### Sintaks

SHEETS\(reference\)

Sintaks fungsi SHEETS memiliki argumen berikut.

*  **Reference**    Opsional. Reference adalah sebuah referensi yang ingin Anda ketahui jumlah lembar di dalamnya. Jika Reference diabaikan, SHEETS mengembalikan jumlah lembar di buku kerja yang berisi fungsi ini.

### Keterangan

* SHEETS berisi semua lembar kerja \(terlihat, tersembunyi, atau sangat tersembunyi\) selain semua tipe lembar lainnya \(lembar makro, bagan, atau dialog\).
* Jika reference bukan nilai yang valid, SHEETS mengembalikan nilai kesalahan \#REF!.
* SHEETS tidak tersedia di Object Model \(OM\) karena Object Model sudah berisi fungsionalitas serupa.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =SHEETS\(\) | Karena tidak ada argumen Reference yang ditentukan, total jumlah lembar dalam buku kerja dikembalikan \(3\). | 3 |
| =SHEETS\(My3DRef\) | Mengembalikan jumlah lembar dalam referensi 3D dengan nama yang ditentukan yaitu My3DRef, yang mencakup Sheet2 dan Sheet3 \(2\). | 2 |

