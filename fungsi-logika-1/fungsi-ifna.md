# Fungsi IFNA

### Pengertian

Mengembalikan nilai yang Anda tentukan jika rumus mengembalikan nilai kesalahan `#N/A;` jika tidak, mengembalikan hasil rumus.

### Sintaks

```text
IFNA(value, value_if_na)
```

Sintaks fungsi `IFNA` memiliki argumen berikut:

* **`Value`**    Diperlukan. Argumen yang diperiksa ada tidaknya nilai kesalahan `#N/A`.
* **`Value_if_na`**    Diperlukan. Nilai yang harus dikembalikan jika rumus mengevaluasi dengan nilai kesalahan `#N/A`.

### Keterangan

* Jika `Value` atau `Value_if_na` merupakan sel kosong, `IFNA` memperlakukannya sebagai nilai string kosong \(""\).
* Jika Value merupakan rumus array, `IFNA` mengembalikan array hasil untuk setiap sel dalam rentang yang ditentukan dalam nilai.

### Contoh

| **Rumus** | **Deskripsi** | **Hasil** |
| :--- | :--- | :--- |
| `=IFNA(VLOOKUP("Seattle",$A$5:$B$10,0),"Tidak ditemukan")` | `IFNA` menguji hasil fungsi `VLOOKUP`. Karena Seattle tidak ditemukan di rentang pencarian, `VLOOKUP`mengembalikan nilai kesalahan `#N/A`. `IFNA` mengembalikan string "Tidak ditemukan" dalam sel dan bukan nilai kesalahan `#N/A` yang standar. | Tidak ditemukan |
| **ID Kawasan** | **Kota** |  |
| Atlanta | 1:05 |  |
| Portland | 142 |  |
| Chicago | 175 |  |
| Los Angeles | 2.51 |  |
| Boise | 266 |  |
| Cleveland | 2,75 |  |

{% page-ref page="fungsi-logika.md" %}

