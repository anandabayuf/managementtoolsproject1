# Fungsi SWITCH

### Pengertian

Fungsi `SWITCH` mengevaluasi satu nilai \(disebut **`ekspresi`**\) terhadap daftar nilai, dan mengembalikan hasil yang terkait dengan nilai cocok pertama. Jika tidak terdapat kecocokan, nilai default opsional mungkin akan dikembalikan.

### **Sintaks**

```text
SWITCH(expression, value1, result1, [default or value2, result2],…[default or value3, result3])
```

| **Argumen** | **Deskripsi** |
| :--- | :--- |
| **`ekspresi`**  \(diperlukan\) | `ekspresi` merupakan nilai \(seperti angka, tanggal, atau teks\) yang akan dibandingkan terhadap `nilai1`...`nilai126`. |
| **`nilai1`…`nilai126`** | **`NilaiN`** adalah nilai yang akan dibandingkan terhadap ekspresi. |
| **`hasil1`…`hasil126`** | **`HasilN`** adalah nilai yang akan dikembalikan jika argumen **`nilaiN`** yang terkait sesuai dengan ekspresi **`HasilN`** dan harus tersedia untuk setiap argumen **`nilaiN`** yang terkait. |
| **`default`**  \(opsional\) | Default adalah nilai yang dikembalikan jika tidak ada kecocokan yang ditemukan dalam ekspresi **`nilaiN`**. Argumen Default diidentifikasi dengan tidak adanya ekspresi **`hasilN`** yang terkait \(lihat contoh\). Default harus menjadi argumen akhir dalam fungsi. |

Karena fungsi dibatasi hingga 254 argumen, Anda dapat menggunakan 126 pasang nilai beserta hasil argumennya.

### Gambaran Umum

Dalam bentuk paling sederhananya, fungsi SWITCH mengatakan:

* **`=SWITCH(Nilai untuk dialihkan, Nilai agar hasil1... [2-126], Nilai untuk mengembalikan jika terdapat hasil1... [2-126], Nilai untuk mengembalikan jika tidak ada kecocokan)`**

Tempat untuk Anda mengevaluasi hingga 126 nilai dan hasil yang cocok.

Lihat rumus berikut:

![Uraian dari argumen fungsi SWITCH](https://support.content.office.net/id-id/media/4b6126f8-3a63-4a14-8699-6cf57712511e.png)

1. Nilai untuk dialihkan? Dalam hal ini, `HARI KERJA(A2)` sama dengan **2**.
2. Nilai apa yang ingin Anda sesuaikan? Dalam hal ini, nilai tersebut adalah 1, **2**, dan 3.
3. Jika terdapat kecocokan, apakah yang ingin Anda kembalikan sebagai hasilnya? Dalam hal ini, Minggu akan menjadi untuk 1, **Senin untuk 2** dan Selasa untuk 3.
4. Nilai default untuk dikembalikan jika tidak ditemukan kecocokan. Dalam hal ini, teks berupa "Tidak ada kecocokan".

   **Catatan:** Jika tidak terdapat nilai yang cocok, dan tidak ada argumen default yang disertakan, fungsi `SWITCH` akan mengembalikan kesalahan `#N/A!`.

### Contoh

Anda dapat menyalin data contoh dalam tabel berikut dan menempelkannya di sel A1 dalam lembar kerja Excel baru untuk mengetahui fungsi `SWITCH` berfungsi. Jika rumus tidak memperlihatkan hasil, Anda dapat memilihnya, kemudian menekan **F2** &gt; **Enter**. Jika menginginkannya, lebar kolom dapat disesuaikan untuk melihat semua data.

#### **Contoh**

| **Nilai** | **Rumus** | **Hasil** |
| :--- | :--- | :--- |
| 2 | `=SWITCH(HARI KERJA(A2),1,"Minggu",2,"Senin",3,"Selasa","Tidak ada kecocokan")` | Karena A2=2, dan Senin adalah argumen hasil yang terkait dengan nilai 2, `SWITCH` mengembalikan sel A2 ke Senin |
| 99 | `=SWITCH(A3,1,"Minggu",2,"Senin",3,"Selasa")` | Karena tidak ada kesesuaian dan tidak ada argumen lain, `SWITCH` mengembalikan `#N/A!` |
| 99 | `=SWITCH(A4,1,"Minggu",2,"Senin",3,"Selasa","Tidak ada kecocokan")` | Tidak ada kesesuaian |
| 2 | `=SWITCH(A5,1,"Minggu",7,"Sabtu","hari kerja")` | hari kerja |
| 3 | `=SWITCH(A6,1,"Minggu",2,"Senin",3,"Selasa","Tidak ada kecocokan")` | Selasa |

{% page-ref page="fungsi-logika.md" %}

