# Fungsi CUBEKPIMEMBER

### Deskripsi

Mengembalikan properti indikator kinerja utama \(KPI, key performance indicator\) dan menampilkan nama KPI dalam sel. KPI adalah pengukuran yang dapat dihitung, seperti laba kotor bulanan atau pergantian karyawan per kuartal, yang digunakan untuk memantau kinerja organisasi.  **Catatan:** Fungsi CUBEKPIMEMBER hanya didukung bila buku kerja tersambung ke Microsoft SQL Server 2005 Analysis Services atau sumber data yang lebih baru.

### Sintaks

CUBEKPIMEMBER\(connection, kpi\_name, kpi\_property, \[caption\]\)

Sintaks fungsi CUBEKPIMEMBER memiliki argumen berikut:

*  **Connection**    Diperlukan. String teks nama koneksi ke kubus.
*  **Kpi\_name**    Diperlukan. String teks nama KPI dalam kubus.
*  **Kpi\_property**    Diperlukan. Komponen KPI dikembalikan dan dapat berupa salah satu dari yang berikut:

| Bilangan bulat | Konten yang dijumlahkan | Deskripsi |
| :--- | :--- | :--- |
| 1 | KPIValue | Nilai aktual |
| 2 | KPIGoal | Nilai target |
| 3 | KPIStatus | Status KPI pada periode waktu tertentu |
| 4 | KPITrend | Ukuran nilai selama periode tertentu |
| 5 | KPIWeight | Kepentingan relatif yang ditetapkan ke KPI |
| 6 | KPICurrentTimeMember | Konteks sementara untuk KPI |

* Jika menentukan KPIValue untuk kpi\_property, hanya kpi\_name yang ditampilkan di dalam sel.
*  **Keterangan**    Opsional. String teks alternatif yang ditampilkan dalam sel sebagai ganti kpi\_name dan kpi\_property.

### Keterangan

* Bila fungsi CUBEKPIMEMBER mengevaluasi, fungsi ini sementara akan menampilkan pesan "\#GETTING\_DATA…" dalam sel sebelum semua data diambil.
* Untuk menggunakan KPI dalam perhitungan, tentukan fungsi CUBEKPIMEMBER sebagai argumen member\_expression dalam fungsi CUBEVALUE.
* Jika nama koneksi bukan merupakan koneksi buku kerja valid yang disimpan dalam buku kerja, CUBEKPIMEMBER akan mengembalikan nilai kesalahan \#NAME? . Jika server Pemrosesan Analitik Online \(OLAP, Online Analytical Processing\) tidak berjalan, tidak tersedia, atau mengembalikan pesan kesalahan, maka CUBEKPIMEMBER akan mengembalikan nilai kesalahan \#NAME?.
* CUBEKPIMEMBER mengembalikan nilai kesalahan \#N/A bila kpi\_name atau kpi\_property tidak valid.
*  CUBEKPIMEMBER dapat mengembalikan nilai kesalahan \#N/A jika Anda mereferensikan objek berbasis sesi, seperti anggota terhitung atau set bernama, dalam PivotTable saat berbagi koneksi, dan PivotTable tersebut dihapus atau Anda mengonversi PivotTable ke rumus. \(Pada tab **Opsi**, di grup **Alat**, klik **Alat OLAP**, lalu klik **Konversi ke Rumus**.\)

### Contoh

=CUBEKPIMEMBER\("Penjualan","PenjualanKPISaya",1\)

=CUBEKPIMEMBER\("Penjualan","PenjualanKPISaya", TargetKPI,"Target Penjualan KPI"\)







