# Fungsi SHEET

### Deskripsi

Mengembalikan nomor lembar dari lembar referensi.

### Sintaks

SHEET\(value\)

Sintaks fungsi SHEET memiliki argumen berikut.

*  **Value**    Optional. Value adalah nama dari sebuah lembar atau referensi yang Anda inginkan nomornya. Jika value diabaikan, SHEET mengembalikan nomor lembar yang berisi fungsi.

### Keterangan

* SHEET berisi semua lembar kerja \(terlihat, tersembunyi, atau sangat tersembunyi\) selain semua tipe lembar lainnya \(lembar makro, bagan, atau dialog\).
* Jika argumen value bukan nilai yang valid, SHEET mengembalikan nilai kesalahan \#REF!. Misalnya, =SHEET\(Sheet1!\#REF\) akan mengembalikan nilai kesalahan \#REF!.
* Jika argumen value adalah nama lembar yang tidak valid, SHEET mengembalikan nilai kesalahan \#NA. Misalnya =SHEET\(“badSheetName”\) akan mengembalikan nilai kesalahan \#NA.
* SHEET tidak tersedia di Object Model \(OM\) karena Object Model sudah berisi fungsionalitas serupa.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Rumus** |  **Deskripsi** |  **Hasil** |
| :--- | :--- | :--- |
| =SHEET\(QSalesByRegion\) | Mengembalikan nomor lembar yang berisi nama QSalesByRegion yang ditentukan di Sheet2, dan memiliki lingkup yang membuatnya tersedia untuk seluruh buku kerja. | 2 |
| =SHEET\(Table1\) | Mengembalikan nomor lembar yang berisi tabel bernama Table1 di Sheet2, dan memiliki lingkup yang membuatnya tersedia untuk seluruh buku kerja. | 2 |
| =SHEET\(Hi\_Temps\) | Mengembalikan nilai kesalahan \#NAME? karena nama yang ditentukan Hi\_Temps terbatas untuk lembar kerja yang memilikinya, yaitu Sheet2. | \#NAME? |
| =SHEET\("Stuff"\) | Mengembalikan nomor lembar dari lembar kerja bernama Stuff. | 3 |

