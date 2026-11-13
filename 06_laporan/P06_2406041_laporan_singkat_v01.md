LAPORAN REVIEW DAN LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 6
Activity Diagram: Dari Skenario ke Alur Aktivitas

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Status Artefak : ACTIVITY DIAGRAM

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan keenam ini bertujuan agar mahasiswa mampu menyusun alur utama activity diagram dari Skenario Normal pada tabel skenario Pertemuan 5 dengan tepat satu initial node dan activity final node, memetakan Skenario Alternative menjadi cabang decision berlabel guard yang bermuara ke merge atau jalur akhir, menggunakan pasangan fork dan join untuk proses yang berjalan paralel, mengelompokkan action ke dalam swimlane sesuai pelaku pada tabel skenario, serta menelusurkan setiap action ke sumber langkah skenarionya secara konsisten.

B. Dasar Teori
Activity diagram adalah diagram UML yang memodelkan alur kegiatan dinamis suatu proses bisnis maupun alur fungsionalitas sistem dari awal hingga akhir. Masukan utama penyusunan activity diagram pada pertemuan ini adalah tabel skenario Pertemuan 5, dengan aturan pemetaan dan simbol OMG UML 2.5.1 sebagai berikut:
1. Initial Node dan Activity Final Node: Menandai titik mulai tunggal dan titik berakhirnya seluruh jalur aktivitas agar tidak ada alur yang menggantung.
2. Action dan Swimlane: Setiap langkah pada kolom Kegiatan maupun Respon sistem dipetakan menjadi action berbentuk persegi panjang bersudut tumpul dan ditempatkan pada swimlane (partisi) pelaku yang sesuai, termasuk swimlane Sistem untuk tanggapan sistem.
3. Decision dan Merge: Decision membagi alur berdasarkan syarat kondisi (guard di dalam tanda kurung siku yang saling lepas), sedangkan merge menyatukan kembali cabang alternatif ke alur utama.
4. Fork dan Join: Fork memecah satu alur menjadi dua atau lebih proses paralel yang tidak saling bergantung, sedangkan join menyinkronkan dan menyatukan kembali proses paralel tersebut sebelum alur dilanjutkan.
5. Pemetaan Relasi Skenario: Relasi include dipetakan sebagai action wajib pada alur utama, relasi extend dipetakan sebagai cabang decision bersyarat, sementara collaboration tidak digambar pada activity diagram.

C. Hasil Praktikum
Seluruh artefak Pertemuan 6 disusun di dalam direktori 04_model_analisis/P06 pada folder induk IFRWP5149_2406041_LabAlat tanpa mengubah berkas P04 dan P05, menggunakan kakas [draw.io / diagrams.net (Desktop/Web) - sesuaikan]:

1. Studi Kasus Terbimbing - Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (Kode: LAB):
   Menyusun tujuh berkas activity diagram (.drawio dan .png) pada 04_model_analisis/P06/LAB yang diturunkan dari tujuh use case utama Pertemuan 5:
   - P06_2406041_LAB_activity_lihat_ketersediaan_v01 (dari LAB-UC01, swimlane Peminjam dan Sistem).
   - P06_2406041_LAB_activity_kelola_data_v01 (dari LAB-UC02 yang melipat cabang varian LAB-UC08 tambah, LAB-UC09 ubah, dan LAB-UC10 hapus).
   - P06_2406041_LAB_activity_peminjaman_v01 (dari LAB-UC03, menyertakan action wajib LAB-UC04 Periksa Ketersediaan dan cabang extend LAB-UC05 Cetak Bukti Pengajuan).
   - P06_2406041_LAB_activity_cetak_bukti_v01 (dari LAB-UC05 yang dimulai pada extension point Bukti pengajuan tersedia).
   - P06_2406041_LAB_activity_keputusan_v01 (dari LAB-UC06 yang dikerjakan secara mandiri terlebih dahulu sebelum dibandingkan dengan lampiran).
   - P06_2406041_LAB_activity_pengembalian_v01 (dari LAB-UC11, menggunakan pasangan fork dan join untuk proses paralel Periksa Kondisi Peralatan dari LAB-UC12 dan unsur proses baru Periksa kelengkapan aksesori peralatan).
   - P06_2406041_LAB_activity_laporan_v01 (dari LAB-UC07, satu-satunya diagram yang memuat swimlane Kepala Laboratorium).

2. Tugas Praktik - Sistem Informasi Akademik, Proses Input Nilai hingga Lihat KHS (Kode: SIA):
   Menyusun satu activity diagram utuh pada 04_model_analisis/P06/SIA bernama P06_2406041_SIA_activity_v01.drawio dan .png yang menggabungkan alur SIA-UC08 Input Nilai Mata Kuliah hingga SIA-UC09 Lihat KHS dengan empat swimlane (Dosen, Sistem, Admin Akademik, Mahasiswa). Diagram memuat decision kelengkapan nilai ([lengkap] dan [belum lengkap] yang kembali ke Dosen melalui merge) serta pasangan fork dan join setelah nilai disahkan untuk menjalankan penerbitan KHS dan pengiriman pemberitahuan secara paralel sebelum mahasiswa melihat KHS.

D. Analisis
Berdasarkan pemeriksaan keterlacakan terhadap tabel skenario Pertemuan 5 dan pengecekan checklist kualitas, pemisahan swimlane terbukti memperjelas pembagian tanggung jawab eksekusi antara aktor manusia dan Sistem. Pada Activity Pengembalian (LAB) dan Activity Input Nilai hingga Lihat KHS (SIA), penggunaan pasangan fork dan join sangat tepat dibandingkan merge karena alur lanjutan (penentuan status kondisi alat atau tampilan KHS oleh mahasiswa) baru boleh dieksekusi setelah kedua proses paralel selesai sepenuhnya.

Selain itu, pemadatan use case pendukung (LAB-UC04 dan LAB-UC12 sebagai action include, serta LAB-UC08 s.d. LAB-UC10 sebagai cabang decision pada kelola data) menjaga diagram tetap ringkas dan terhindar dari duplikasi alur. Pada pengerjaan tugas mandiri Activity Proses Keputusan Peminjaman (LAB-UC06), [tuliskan catatan perbandingan Anda setelah melihat lampiran, misalnya: seluruh alur utama dan dua titik decision telah sesuai dengan skenario LAB-UC06, dengan penyesuaian kecil pada penulisan label guard agar sama persis dengan pembanding]. Seluruh berkas sumber .drawio juga telah diuji buka ulang dan dipastikan sinkron dengan berkas ekspor .png.

E. Kesimpulan
Praktikum Pertemuan 6 berhasil memodelkan langkah-langkah interaksi pada tabel skenario ke dalam tujuh activity diagram studi kasus laboratorium dan satu activity diagram layanan hasil studi akademik. Penerapan swimlane, decision-merge, serta fork-join secara konsisten menghasilkan alur proses yang logis, dapat ditelusuri ke skenario sumber, dan bebas dari alur yang terputus.