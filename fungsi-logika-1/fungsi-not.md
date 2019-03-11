# Fungsi NOT

### Pengertian

Gunakan fungsi **`NOT`**, salah satu fungsi logika, ketika ingin memastikan satu nilai tidak sama dengan yang lain.

### Contoh 1

![Contoh fungsi NOT untuk membalikkan argumen.  CONTOH =NOT\(1+1=2\)](https://support.content.office.net/id-id/media/78c8be8a-4291-4663-9cb2-6f073fa570aa.png)

Fungsi **`NOT`**membalikkan nilai argumennya.

Salah satu penggunaan umum untuk fungsi **`NOT`** adalah memperluas kegunaan fungsi lain yang menjalankan pengujian logika. Misalnya, fungsi **`IF`** menjalankan pengujian logika, kemudian mengembalikan satu nilai jika pengujian tersebut mengevaluasi menjadi `TRUE` dan nilai lain jika pengujian mengevaluasi menjadi `FALSE`. Dengan fungsi **`NOT`** sebagai argumen logical\_test dari fungsi **`IF`**, Anda dapat menguji banyak kondisi berbeda bukan hanya satu.

#### **Sintaks**

```text
NOT(logika)
```

Sintaks fungsi **`NOT`** memiliki argumen berikut:

* **`Logical`**    Diperlukan. Nilai atau ekspresi yang bisa dievaluasi ke TRUE atau FALSE.

#### **Keterangan**

Jika logikanya adalah `FALSE`, **`NOT`** mengembalikan `TRUE`; jika logikanya adalah `TRUE`, **`NOT`** mengembalikan `FALSE`.

### Contoh 2

Berikut beberapa contoh umum menggunakan **`NOT`** sendiri, dan dalam hubungannya dengan **`IF`**, **`AND`**, dan **`OR`**.

![Contoh NOT dengan fungsi IF, AND, dan OR](https://support.content.office.net/id-id/media/d2b3f677-3cee-4bb0-9b22-6227fd767d62.png)

| **Rumus** | **Deskripsi** |
| :--- | :--- |
| `=NOT(A2>100)` | A2 **`NOT`** \(tidak\) lebih besar dari 100 |
| `=IF(AND(NOT(A2>1),NOT(A2<100)),A2,"Nilai berada di luar rentang")` | 50 lebih besar dari 1 \(`TRUE`\), **`AND`** 50 lebih kecil dari 100 \(`TRUE`\), sehingga **`NOT`** akan membalikkan kedua argumen menjadi `FALSE`. **`AND`** memerlukan kedua argumen untuk menjadi `TRUE`, maka hasil akan dikembalikan jika `FALSE`. |
| `=IF(OR(NOT(A3<0),NOT(A3>50)),A3,"Nilai berada di luar rentang")` | 100 tidak kurang dari 0 \(`FALSE`\), dan 100 lebih besar dari 50 \(`TRUE`\), sehingga **`NOT`** akan membalikkan argumen menjadi `TRUE`/`FALSE`. **`OR`** hanya memerlukan satu argumen untuk menjadi `TRUE`, maka hasil akan dikembalikan jika `TRUE`. |

### **Penghitungan Komisi Penjualan**

Berikut adalah skenario yang cukup umum ketika kita perlu menghitung apakah staf penjualan memenuhi syarat untuk bonus menggunakan **`NOT`** dengan **`IF`** dan **`AND`**.

![Contoh penghitungan bonus penjualan dengan IF, AND, dan NOT.  Rumus di sel E14 adalah =IF\(AND\(NOT\(B14&amp;lt;$B$7\),NOT\(C14&amp;lt;$B$5\)\),B14\*$B$8,0\)](https://support.content.office.net/id-id/media/0a3ed63d-8c68-4eea-a352-b354475ac92e.png)

```text
=IF(AND(NOT(B14<$B$7),NOT(C14<$B$5)),B14*$B$8,0)
```

* - **`IF`** Total Penjualan **`NOT`** \(tidak\) kurang dari Sasaran Penjualan, **`AND`** Akun **`NOT`** \(tidak\) kurang dari Sasaran Akun, kali Total Penjualan dengan % Komisi, jika tidak kembalikan 0.

{% page-ref page="fungsi-logika.md" %}

