# Fungsi IFS

### Pengertian

JIKA fungsi memeriksa apakah satu atau beberapa kondisi terpenuhi, dan mengembalikan nilai yang berhubungan pertama syarat yang benar. Jika dapat berlangsung beberapa pernyataan IF bertumpuk, dan lebih mudah untuk dibaca dengan beberapa kondisi.

### Sintaks

Biasanya, sintaks untuk fungsi jika adalah:  
  
`= jika ([ada True1, nilai jika True1, ada True2, nilai jika True2, ada True3, nilai jika True3)`

Harap diperhatikan bahwa jika fungsi memungkinkan Anda untuk menguji hingga 127 kondisi yang berbeda. Namun, kami tidak merekomendasikan penumpukan terlalu banyak kondisi dengan jika atau jika pernyataan. Ini adalah karena beberapa kondisi harus dimasukkan dalam urutan yang benar, dan bisa sangat sulit untuk menyusun, menguji, dan memperbarui.

Sintaks

```text
IFS(logical_test1, value_if_true1, [logical_test2, value_if_true2], [logical_test3, value_if_true3],…)
```

| **Argumen** | **Deskripsi** |
| :--- | :--- |
| **`kondisi_logika1`**\(diperlukan\) | Kondisi yang menilai ke `TRUE` atau `FALSE`. |
| **`nilai_jika_benar1`**\(diperlukan\) | Hasil dikembalikan jika `logical_test1` menilai `TRUE`. Dapat dikosongkan. |
| **`kondisi_logika2`…`kondisi_logika127`**\(opsional\) | Kondisi yang menilai ke `TRUE` atau `FALSE`. |
| **`nilai_jika_benar2`…`nilai_jika_benar127`**\(opsional\) | Hasil yang dikembalikan jika **`logical_testN`** menilai `TRUE`. Setiap **`value_if_trueN`** sesuai dengan kondisi **`logical_testN`**. Dapat dikosongkan. |

### Contoh 1

![Contoh Nilai fungsi IFS. Rumus di sel B2 adalah &#xF0A7;=IFS\(A2&amp;gt;89,&quot;A&quot;,A2&amp;gt;79,&quot;B&quot;,A2&amp;gt;69,&quot;C&quot;,A2&amp;gt;59,&quot;D&quot;,TRUE,&quot;F&quot;\)](https://support.content.office.net/id-id/media/80f9a63f-0874-49c3-8081-bab6dadbdfa1.png)

Rumus untuk sel A2:A6 adalah:

```text
=IFS(A2>89,"A",A2>79,"B",A2>69,"C",A2>59,"D",TRUE,"F")
```

Yang berbunyi `IF(A2 Lebih Besar Dari 89, kembalikan "A", JIKA A2 Lebih Besar Dari 79, kembalikan "B", dan sebagainya lalu untuk semua nilai lainnya yang kurang dari 59, kembalikan "F").`

### Contoh 2

![Fungsi IFS - contoh Hari dalam Seminggu - Rumus dalam sel G2 adalah &#xF0A7;	=IFS\(F2=1,D2,F2=2,D3,F2=3,D4,F2=4,D5,F2=5,D6,F2=6,D7,F2=7,D8\)](https://support.content.office.net/id-id/media/96e58a74-c58e-4688-9389-9612cff13e8a.png)

Rumus di sel G7 adalah:

```text
=IFS(F2=1,D2,F2=2,D3,F2=3,D4,F2=4,D5,F2=5,D6,F2=6,D7,F2=7,D8)
```

Yang berbunyi`IF(nilai dalam sel F2 sama dengan 1, kembalikan nilai di sel D2, JIKA nilai dalam sel F2 sama dengan 2, kembalikan nilai di sel D3, dan seterusnya, akhirnya berakhiran dengan nilai di sel D8 jika tidak ada kondisi lainnya yang terpenuhi).`

### Keterangan

* Untuk menentukan hasil default, masukkan `TRUE` untuk argumen akhir kondisi\_logika Anda. Jika tidak ada kondisi lain yang terpenuhi, nilai yang terkait akan dihasilkan. Dalam Contoh 1, baris 6 dan 7 \(dengan nilai 58\) mendemonstrasikan hal ini.
* Jika suatu argumen `kondisi_logika` disediakan tanpa `nilai_jika_benar`, fungsi ini akan menampilkan pesan kesalahan "Anda memasukkan terlalu sedikit argumen untuk fungsi ini".
* Jika suatu argumen `kondisi_logika` dievaluasi dan menghasilkan nilai selain `TRUE` atau `FALSE`, fungsi ini akan menghasilkan kesalahan `#VALUE!`.
* Jika tidak ada kondisi `TRUE` yang ditemukan, fungsi ini akan menghasilkan kesalahan `#N/A`.

{% page-ref page="fungsi-logika.md" %}

