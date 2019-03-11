# Fungsi OR

### Pengertian

Gunakan fungsi **`OR`**, salah satu fungsi logika, untuk menentukan jika semua kondisi dalam sebuah tes adalah `TRUE`.



### Contoh 1

![Contoh penggunaan fungsi OR.](https://support.content.office.net/id-id/media/d68e210e-aa81-4806-a4b6-12576ce832a4.png)

Fungsi **`OR`** mengembalikan `TRUE` jika semua argumennya mengevaluasi ke `TRUE`, dan mengembalikan `FALSE` jika semua argumennya mengevaluasi ke `FALSE`.

Satu penggunaan umum fungsi **`OR`** adalah untuk memperluas kegunaan fungsi-fungsi lain yang menjalankan pengujian logika. Misalnya, fungsi **`IF`** menjalankan pengujian logika lalu mengembalikan satu nilai jika pengujian tersebut mengevaluasi ke `TRUE` dan nilai lain jika pengujian mengevaluasi ke `FALSE`. Dengan fungsi **`OR`** sebagai argumen logical\_test dari fungsi **`IF`**, Anda dapat menguji banyak kondisi berbeda, tidak hanya satu.

#### **Sintaks**

```text
OR(logika1, [logika2], ...)
```

Sintaks fungsi **`OR`** memiliki argumen berikut:

| **Argumen** | **Deskripsi** |
| :--- | :--- |
| **`Logika1`** | Diperlukan. Kondisi pertama yang ingin Anda uji dan dapat mengevaluasi ke `TRUE` maupun `FALSE`. |
| **`Logika2`, ...** | Opsional. Kondisi tambahan yang ingin Anda uji yang mengevaluasi ke `TRUE` atau `FALSE`, hingga maksimal 255 kondisi. |

#### **Keterangan**

* Argumen harus mengevaluasi terhadap nilai logika seperti `TRUE` atau `FALSE`, atau dalam array atau referensi yang berisi nilai logika.
* Jika array atau argumen referensi berisi teks atau sel kosong, nilai-nilai itu diabaikan.
* Jika rentang tertentu tidak berisi nilai logika, **`OR`** mengembalikan nilai kesalahan `#VALUE!`.
* Anda dapat menggunakan rumus array **`OR`** untuk melihat apakah sebuah nilai muncul dalam larik. Untuk memasukkan rumus array, tekan CTRL+SHIFT+ENTER.

### Contoh 2

Berikut beberapa contoh umum dari menggunakan **`OR`** sendiri, dan dalam hubungannya dengan **`IF`**.

![Contoh penggunaan fungsi OR dengan fungsi IF.](https://support.content.office.net/id-id/media/f331ccff-906c-4c3d-aa07-091127f50a1d.png)

| **Rumus** | **Deskripsi** |
| :--- | :--- |
| `=OR(A2>1,A2<100)` | Menampilkan `TRUE` jika A2 lebih besar dari 1 **`OR`** \(atau\) kurang dari 100, jika tidak, rumus akan menampilkan `FALSE`. |
| `=IF(OR(A2>1,A2<100),A3,"Nilai berada di luar rentang")` | Menampilkan nilai di sel A3 jika lebih besar dari 1 **`OR`** \(atau\) kurang dari 100, jika tidak, sel akan menampilkan pesan "Nilai berada di luar rentang". |
| `=IF(OR(A2<0,A2>50),A2,"Nilai berada di luar rentang")` | Menampilkan nilai di sel A2 jika kurang dari 0 **`OR`** \(atau\) lebih besar dari 50, jika tidak, sel akan menampilkan pesan. |

### **Penghitungan Komisi Penjualan**

Berikut adalah skenario yang cukup umum ketika Anda perlu menghitung apakah staf penjualan memenuhi syarat untuk komisi menggunakan **`IF`** dan **`OR`**.

![Contoh penggunaan IF dan OR untuk menghitung komisi penjualan.](https://support.content.office.net/id-id/media/66a0b795-7c88-4467-b64b-b4448c8c48ac.png)

```text
=IF(OR(B14>=$B$4,C14>=$B$5),B14*$B$6,0) 
```

* - **`IF`** Total Penjualan lebih besar dari atau sama dengan \(&gt;=\) Sasaran Penjualan, **`OR`** Akun lebih besar dari atau sama dengan \(&gt;=\) Sasaran Akun, lalu kalikan Total Penjualan dengan % Komisi, jika tidak akan mengembalikan 0.

{% page-ref page="fungsi-logika.md" %}

