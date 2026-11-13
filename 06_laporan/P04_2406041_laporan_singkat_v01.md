LAPORAN REVIEW DAN LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 4
Use Case Diagram Lanjutan: Generalization dan Collaboration

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Status Artefak : LATIHAN USE CASE DIAGRAM LANJUTAN

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan keempat ini bertujuan agar mahasiswa mampu menyusun hierarki generalization aktor (aktor khusus menuju aktor umum tanpa menggambar ulang asosiasi yang diwarisi), menyusun generalization use case beserta perilaku pembeda pada setiap use case khusus, menempatkan elemen collaboration dan menghubungkannya melalui relasi realization menuju use case yang diwujudkan, membangun use case diagram kumulatif yang mempertahankan seluruh model Pertemuan 3 secara utuh, serta menyusun use case description lanjutan yang terlacakan ke daftar kebutuhan.

B. Dasar Teori
Pengembangan model use case pada Pertemuan 4 bersifat kumulatif dan memperdalam pemodelan dengan menambahkan tiga konsep utama sesuai standar OMG UML 2.5.1:
1. Generalization Aktor: Menyatakan hubungan pewarisan dari aktor umum (general) kepada aktor khusus (specialized). Aktor khusus mewarisi seluruh asosiasi yang dimiliki aktor umum sehingga garis asosiasi cukup digambar satu kali dari aktor umum, sementara aktor khusus tetap dapat memiliki asosiasi tambahan tersendiri. Notasinya berupa garis utuh dengan panah segitiga kosong yang menunjuk dari aktor khusus ke aktor umum.
2. Generalization Use Case: Menyatakan bahwa satu use case bersifat umum dan use case lainnya merupakan bentuk spesialisasi yang mewarisi tujuan dasar namun memiliki hasil akhir spesifik. Panah segitiga kosong mengarah dari use case khusus menuju use case umum.
3. Collaboration dan Realization: Collaboration merepresentasikan sekumpulan peran dan elemen di dalam sistem yang bekerja sama mewujudkan perilaku suatu use case, digambarkan sebagai elips bergaris putus-putus dengan nama yang sama persis seperti use case terkait dan tidak dihubungkan langsung ke aktor. Relasi realization digambarkan dengan garis putus-putus berujung segitiga kosong dari collaboration menuju use case.

C. Hasil Praktikum
Seluruh artefak Pertemuan 4 disusun secara kumulatif tanpa mengubah berkas Pertemuan 1 hingga 3 pada folder induk IFRWP5149_2406041_LabAlat menggunakan kakas [draw.io / diagrams.net (Desktop/Web) - sesuaikan]:

1. Studi Kasus Terbimbing - Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (Kode: LAB):
   - Berkas: P04_LAB_skenario_v01.md, P04_LAB_kebutuhan_v01.md (LAB-R07 s.d. LAB-R11), serta diagram kumulatif P04_2406041_LAB_usecase_v01.drawio dan .png pada 04_model_analisis/P04/LAB.
   - Pemodelan Kumulatif (17 Hubungan): Mempertahankan 3 aktor dan LAB-UC01 s.d. LAB-UC07 beserta relasi include dan extend dari Pertemuan 3. Ditambahkan aktor umum Peminjam (mewariskan LAB-UC01 dan LAB-UC03 kepada Mahasiswa dan Dosen, sementara asosiasi khusus Mahasiswa ke LAB-UC05 tetap), tiga use case khusus (LAB-UC08 Tambah, LAB-UC09 Ubah, LAB-UC10 Hapus Data Peralatan) yang mengarah ke LAB-UC02, fungsi baru LAB-UC11 Catat Pengembalian Peralatan (include LAB-UC12 Periksa Kondisi Peralatan), serta collaboration LAB-CO01 (Ajukan Peminjaman) dan LAB-CO02 (Catat Pengembalian Peralatan) dengan relasi realization.
   - Dokumentasi: Menyusun use case description lengkap untuk LAB-UC11 dengan tambahan baris Include dan Collaboration.

2. Tugas Praktik - Sistem Informasi Akademik, Layanan Hasil Studi (Kode: SIA):
   - Berkas: P04_SIA_skenario_v01.md, P04_SIA_kebutuhan_v01.md (SIA-R07 s.d. SIA-R12), deskripsi use case, serta diagram kumulatif P04_2406041_SIA_usecase_v01.drawio dan .png pada 04_model_analisis/P04/SIA.
   - Pemodelan Kumulatif: Menggabungkan model jadwal kuliah (Pertemuan 2) dan pengajuan KRS (Pertemuan 3) dengan layanan hasil studi. Ditambahkan aktor umum Civitas Akademika yang mewariskan SIA-UC07 Lihat Kalender Akademik kepada Mahasiswa dan Dosen, use case khusus SIA-UC11 s.d. SIA-UC13 (Tambah, Ubah, Hapus Data Mahasiswa) yang mengarah ke SIA-UC10 Kelola Data Mahasiswa, serta collaboration SIA-CO01 (Input Nilai Mata Kuliah) dan SIA-CO02 (Lihat KHS) dengan relasi realization.
   - Dokumentasi: Menyusun deskripsi lengkap untuk Input Nilai Mata Kuliah dan deskripsi ringkas untuk Lihat KHS.

D. Analisis
Berdasarkan uji konsistensi skenario pada tugas praktik Layanan Hasil Studi (SIA) serta pemeriksaan checklist kualitas, diperoleh hasil analisis berikut:
1. Situasi A (Mahasiswa Melihat Kalender Akademik Tanpa Garis Asosiasi Langsung): Kondisi ini tetap sah dan valid dalam pemodelan UML karena Mahasiswa merupakan aktor khusus dari Civitas Akademika, sehingga secara otomatis mewarisi seluruh kemampuan interaksi dan asosiasi yang terhubung ke Civitas Akademika (SIA-UC07).
2. Situasi B (Dosen Bukan Pengampu Mencoba Menginput Nilai): Berdasarkan prasyarat dan alur alternatif pada use case description Input Nilai Mata Kuliah, sistem akan menolak akses/penyimpanan dan memicu pascakondisi gagal sehingga tidak ada perubahan data nilai yang tersimpan.
3. Situasi C (Admin Akademik Menghapus Data Mahasiswa Aktif): Berdasarkan aturan bisnis tugas, operasi Hapus Data Mahasiswa hanya berlaku jika mahasiswa tidak memiliki data akademik aktif. Jika masih aktif, sistem membatalkan penghapusan dan mempertahankan data mahasiswa tersebut.

Dalam penerapannya, pemisahan antara asosiasi warisan pada aktor umum dengan asosiasi khusus (seperti Cetak Bukti Pengajuan pada Mahasiswa) menjaga diagram tetap ringkas tanpa duplikasi garis. Selain itu, seluruh berkas sumber .drawio telah diuji buka ulang dan dipastikan sinkron dengan berkas ekspor .png. [Jika ada revisi ke v02 setelah review teman/asisten, tuliskan di sini; jika tidak ada, tulis: Tidak ditemukan kesalahan arah panah generalization maupun realization saat pemeriksaan checklist sehingga berkas tetap pada versi v01].

E. Kesimpulan
Praktikum Pertemuan 4 berhasil memperluas use case diagram secara kumulatif dengan menerapkan teknik generalization aktor, generalization use case, serta collaboration dan relasi realization pada kasus laboratorium dan akademik. Seluruh elemen baru terlacakan secara konsisten terhadap daftar kebutuhan, katalog fungsi, serta use case description tanpa merusak struktur model dari pertemuan sebelumnya.