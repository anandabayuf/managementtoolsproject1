# Fungsi TYPE

### Deskripsi

Mengembalikan tipe nilai. Gunakan TYPE saat perilaku fungsi lain bergantung pada tipe nilai di sel tertentu.

### Sintaks

TYPE\(value\)

Sintaks fungsi TYPE memiliki argumen berikut:

*  **Value**    Diperlukan. Bisa berupa nilai Microsoft Excel apa pun, seperti angka, teks, nilai logika, dan lain-lain.



|  **Jika nilai adalah** |  **TYPE mengembalikan** |
| :--- | :--- |
| Angka | 1 |
| Teks | 2 |
| Nilai logika | 4 |
| Nilai kesalahan | 16 |
| Array | 6,4 |

### Keterangan

* TYPE paling berguna saat Anda menggunakan fungsi yang bisa menerima tipe data berbeda, seperti ARGUMENT dan INPUT. Gunakan TYPE untuk menemukan tipe data yang dikembalikan oleh fungsi atau rumus.
* Anda tidak bisa menggunakan TYPE untuk menentukan apakah sel berisi rumus. TYPE hanya menentukan tipe dari nilai yang dikembalikan atau ditampilkan. Jika nilai adalah referensi sel yang berisi rumus, TYPE mengembalikan tipe dari nilai yang dikembalikan oleh rumus tersebut.

### Contoh



Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

|  **Data** |  |  |
| :--- | :--- | :--- |
| Smith |  |  |
|  **Rumus** |  **Deskripsi** |  **Hasil** |
| =TYPE\(A2\) | Mengembalikan tipe nilai di A2. Tipe Teks ditunjukkan oleh 2. | 2 |
| =TYPE\("Mr. "&A2\) | Mengembalikan tipe "Mr. Smith, yang berupa Teks. | 2 |
| =TYPE\(2+A2\) | Mengembalikan tipe rumus di C6, yang mengembalikan 16, tipe untuk nilai kesalahan \#VALUE! Nilai kesalahan \#VALUE! ditunjukkan di C7. | 16 |
| =\(2+A2\) | Nilai kesalahan yang dikembalikan oleh rumus =\(2+A2\), yang digunakan di C2. | \#VALUE! |
| =TYPE\({1,2;3,4}\) | Mengembalikan tipe konstanta array, yaitu 64. | 6,4 |

