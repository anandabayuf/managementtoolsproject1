# Fungsi IF

### Pengertian

Fungsi `IF` merupakan salah satu fungsi paling populer di Excel, yang memungkinkan Anda membuat perbandingan logis antara nilai dan perkiraan.

Oleh karena itu, pernyataan `IF` dapat memiliki dua hasil. Hasil pertama jika perbandingan Anda Benar dan hasil kedua jika perbandingan Salah.

Misalnya, `=IF(C2="Yes",1,2)` mengatakan `IF (C2 = ya, jadi Kembalikan 1, jika tidak Kembalikan 2).`

### Sintaks

Gunakan fungsi `IF`, salah satu dari fungsi Logika, untuk mengembalikan satu nilai jika kondisi benar dan nilai lain jika kondisi salah.

```text
IF(logical_test, value_if_true, [value_if_false])
```

Misalnya :

```text
=IF(A2>B2,"Melebihi Budget","OK")
```

```text
=IF(A2=B2,B4-A4,"")
```

| **Nama argumen** | **Deskripsi** |
| :--- | :--- |
| **`logical_test`**    \(diperlukan\) | Kondisi yang ingin Anda uji. |
| **`value_if_true`**    \(diperlukan\) | Nilai yang ingin Anda kembalikan jika hasil **`logical_test`**adalah `TRUE`. |
| **`value_if_false`**    \(opsional\) | Nilai yang ingin Anda kembalikan jika hasil **`logical_test`**adalah `False`. |

### Contoh `IF` sederhana

![Sel D2 berisi rumus =IF\(C2=&quot;Ya&quot;,1,2\)](https://support.content.office.net/id-id/media/9f8095f1-ed25-451b-a818-e2b9db01d829.png)

```text
=IF(C2=”Ya”,1,2)
```

Dalam contoh di atas, sel D2 mengatakan: `IF(C2 = Ya, jadi kembalikan 1, jika tidak kembalikan 2)`

![Sel D2 berisi rumus =IF\(C2=1,&quot;YA&quot;,&quot;TIDAK&quot;\)](https://support.content.office.net/id-id/media/d0ae94da-d05f-4600-8331-7ef742c126fb.png)

```text
=IF(C2=1,”Ya”,”Tidak”)
```

Dalam contoh ini, rumus di sel D2 mengatakan: `IF(C2 = 1, then return Yes, otherwise return No)`seperti yang Anda lihat, fungsi `IF` dapat digunakan untuk mengevaluasi teks dan nilai. Juga dapat digunakan untuk mengevaluasi kesalahan. Tidak terbatas untuk memeriksa hanya jika satu hal sama dengan yang lain dan mengembalikan hasil tunggal, Anda bisa juga menggunakan operator matematika dan melakukan perhitungan tambahan tergantung pada kriteria Anda. Anda juga dapat menumpuk beberapa fungsi `IF` bersama-sama agar dapat melakukan beberapa perbandingan.

![Rumus di sel D2=IF \(C2&amp;gt;B2,&quot;Melebihi Budget&quot;,&quot;Dalam Budget&quot;\)](https://support.content.office.net/id-id/media/219d0e3f-36d1-4d82-87df-29ac68330edb.png)

```text
=IF(C2>B2,”Melebihi Budget”,”Dalam Budget”)
```

Dalam contoh di atas, fungsi `IF` di D2 mengatakan `IF(C2 Lebih Besar Dari B2, kembalikan "Melebihi Budget", jika tidak kembalikan "Dalam Budget")`

![Rumus di sel E2 adalah=IF\(C2&amp;gt;B2,C2-B2,&quot;&quot;\)](https://support.content.office.net/id-id/media/4bbae039-b79d-4998-b8b3-a18950f4350e.png)

```text
=IF(C2>B2,C2-B2,0)
```

Dalam ilustrasi di atas, kita akan mengembalikan perhitungan matematis, bukan mengembalikan hasil teks. Rumus di E2 mengatakan `IF(Aktual Lebih Besar daripada Anggaran, maka Kurangi jumlah Anggaran dari jumlah Aktual, jika tidak kembalikan nol).`

![Rumus di Sel F7 adalah IF\(E7=&quot;Ya&quot;,F5\*0,0825.0\)](https://support.content.office.net/id-id/media/d263a33c-3229-4e4d-9631-0568abc55d63.png)

```text
=IF(E7=”Ya”,F5*0,0825.0)
```

Dalam contoh ini, rumus dalam F7 mengatakan `IF(E7 = "Ya", lalu hitung Jumlah Total di F5 * 8,25%, selain itu tidak ada Pajak Penjualan yang jatuh tempo, maka kembalikan 0)`

**Catatan:** Jika Anda akan menggunakan teks dalam rumus, Anda perlu membungkus teks dalam tanda petik \(misalnya "teks"\). Satu-satunya pengecualian yang menggunakan `TRUE` atau `FALSE`, yang Excel secara otomatis memahami.

### Masalah umum

| Masalah | Apa yang salah |
| :--- | :--- |
| 0 \(nol\) di sel | Tidak ada argumen untuk argumen **`value_if_true`** atau **`value_if_False`**. Untuk melihat nilai benar yang dikembalikan, tambahkan teks argumen pada dua argumen, atau tambahkan `TRUE` atau `FALSE` ke argumen. |
| `#NAME?` dalam sel | Ini biasanya berarti bahwa rumus salah eja. |

{% page-ref page="fungsi-logika.md" %}

