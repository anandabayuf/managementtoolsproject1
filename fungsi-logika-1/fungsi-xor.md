# Fungsi XOR

### Pengertian

Mengembalikan logika Exclusive Or dari semua argumen.

### Sintaks

```text
XOR(logical1, [logical2],…)
```

Sintaks fungsi `XOR` memiliki argumen berikut.

* **`Logical1, [logical2],…`**    Logical 1 diperlukan, nilai logika berikutnya adalah opsional. 1 hingga 254 kondisi yang ingin Anda uji yang bisa berupa `TRUE` atau `FALSE`, dan bisa berupa nilai, array, atau referensi logika.

### Keterangan

* Argumen harus mengevaluasi terhadap nilai logika seperti `TRUE` atau `FALSE`, atau dalam array atau referensi yang berisi nilai logika.
* Jika sebuah argumen array atau referensi berisi teks atau sel kosong, nilai tersebut diabaikan.
* Jika rentang tertentu tidak berisi nilai logika, `XOR` menghasilkan nilai kesalahan `#VALUE!`
* Anda dapat menggunakan rumus array `XOR` untuk mengetahui apakah nilai muncul dalam array. Untuk memasukkan rumus array, tekan Ctrl+Shift+Enter.
* Hasil `XOR` adalah `TRUE` jika jumlah input `TRUE` ganjil dan `FALSE` jika jumlah input `TRUE` genap.

### Contoh

Salin contoh data di dalam tabel berikut ini dan tempel ke dalam sel A lembar kerja Excel yang baru. Agar rumus menunjukkan hasil, pilih datanya, tekan F2, lalu tekan Enter. Jika perlu, Anda bisa menyesuaikan lebar kolom untuk melihat semua data.

| **Rumus** | **Deskripsi** | **Hasil** |
| :--- | :--- | :--- |
| `=XOR(3>0,2<9)` | Karena salah satu dari dua uji mengevaluasi ke True, maka `TRUE` dikembalikan. | `TRUE` |
| `=XOR(3>12,4>6)` | Karena semua hasil uji mengevaluasi ke False, maka `FALSE` dikembalikan. Sedikitnya satu dari hasil uji tersebut harus mengevaluasi ke True untuk mengembalikan `TRUE`. | `FALSE` |

{% page-ref page="fungsi-logika.md" %}

