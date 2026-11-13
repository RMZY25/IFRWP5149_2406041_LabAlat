LAPORAN REVIEW DAN LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 3
Use Case Diagram dan Use Case Description

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Status Artefak : LATIHAN USE CASE DIAGRAM

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan ketiga ini bertujuan agar mahasiswa mampu merumuskan batas sistem, aktor, kebutuhan, aturan bisnis, dan asumsi dari skenario yang diberikan, menentukan use case berdasarkan tujuan aktor, menyusun use case diagram yang konsisten beserta relasi asosiasi, include, dan extend, menyusun use case description secara terstruktur (mencakup pemicu, prasyarat, alur utama, alur alternatif, dan pascakondisi), serta menjamin keterlacakan antara kebutuhan, diagram, dan deskripsi.

B. Dasar Teori
Use case diagram adalah pemodelan UML yang memvisualisasikan fungsionalitas sistem dari sudut pandang pengguna beserta interaksi antara aktor eksternal dengan layanan di dalam batas sistem. Selain asosiasi dasar, terdapat dua relasi antar-use case yang digunakan pada pertemuan ini:
1. Relasi Include: Menyatakan bahwa perilaku suatu use case selalu disertakan sebagai bagian wajib dalam pelaksanaan use case penyerta. Arah panah putus-putus mengarah dari use case penyerta menuju use case yang disertakan.
2. Relasi Extend: Menambahkan perilaku opsional ke use case dasar pada titik perluasan (extension point) dan kondisi tertentu. Use case dasar tetap dapat berjalan dan bermakna tanpa perilaku tambahan tersebut, dengan arah panah putus-putus dari use case tambahan menuju use case dasar.

Untuk menjelaskan rincian skenario secara operasional, digunakan Use Case Description yang mendokumentasikan pemicu, prasyarat (keadaan yang sudah terpenuhi sebelumnya, bukan dianggap sebagai relasi include), alur utama ketika berhasil, alur alternatif atau pengecualian ketika terjadi kegagalan, serta pascakondisi akhir.

C. Hasil Praktikum
Seluruh artefak Pertemuan 3 telah disusun pada folder proyek IFRWP5149_2406041_LabAlat (mencakup P03_2406041_logbook_v01.md, dokumen skenario/kebutuhan, diagram sumber .drawio, hasil ekspor .png, serta berkas deskripsi .md) dengan menggunakan kakas [draw.io / diagrams.net (Desktop/Web) - sesuaikan]:

1. Studi Kasus Terbimbing - Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (Kode: LAB):
   - Aktor: Mahasiswa, Petugas laboratorium, dan Kepala laboratorium.
   - Use Case (7 fungsi): LAB-UC01 Lihat ketersediaan peralatan, LAB-UC02 Kelola data peralatan, LAB-UC03 Ajukan peminjaman, LAB-UC04 Periksa ketersediaan, LAB-UC05 Cetak bukti pengajuan, LAB-UC06 Proses keputusan peminjaman, dan LAB-UC07 Lihat laporan peminjaman.
   - Relasi Antar-Use Case: LAB-UC03 memiliki relasi include menuju LAB-UC04 (validasi ketersediaan wajib saat pengajuan), sedangkan LAB-UC05 memiliki relasi extend menuju LAB-UC03 pada extension point "Bukti pengajuan tersedia" dengan kondisi [mahasiswa memilih cetak].
   - Dokumentasi: Dilengkapi use case description utama untuk LAB-UC03 Ajukan peminjaman beserta alur utama dan alternatifnya.

2. Tugas Praktik - Sistem Informasi Akademik (Kode: SIA):
   - Aktor: Mahasiswa dan Dosen wali (aktor Admin akademik tidak disertakan karena berada di luar skenario kebutuhan SIA-R03 hingga SIA-R06).
   - Use Case (4 fungsi): Ajukan KRS (SIA-R03), Validasi KRS (SIA-R04), Unduh bukti pengajuan KRS (SIA-R05), dan Proses keputusan KRS (SIA-R06).
   - Relasi Antar-Use Case: Ajukan KRS memiliki relasi include menuju Validasi KRS untuk memeriksa kelengkapan, prasyarat, dan benturan jadwal. Unduh bukti pengajuan KRS memiliki relasi extend menuju Ajukan KRS pada extension point konfirmasi penyimpanan dengan kondisi [mahasiswa memilih mengunduh bukti].
   - Dokumentasi: Dilengkapi keempat use case description pada P03_2406041_SIA_deskripsi_v01.md beserta diagram pada P03_2406041_SIA_usecase_v01.drawio dan .png.

D. Analisis
Berdasarkan pengujian konsistensi antara diagram dan use case description pada tiga skenario kondisi sistem (khususnya pada tugas praktik pengajuan KRS), diperoleh hasil analisis sebagai berikut:
1. Situasi Validasi Berhasil dan Tidak Mengunduh Bukti: Alur utama berjalan hingga penyimpanan data KRS dengan status menunggu persetujuan dosen wali. Karena relasi Unduh bukti pengajuan KRS bersifat extend (opsional), proses pengajuan tetap dinyatakan berhasil tanpa harus mengeksekusi fungsi tambahan tersebut.
2. Situasi Validasi Gagal: Ketika fungsi include (Validasi KRS / Periksa ketersediaan) menemukan ketidaksesuaian seperti benturan jadwal atau alat tidak tersedia, sistem memicu alur alternatif/pengecualian sehingga pengajuan dibatalkan dan pascakondisi gagal terpenuhi (tidak ada pengajuan baru yang tersimpan).
3. Situasi Validasi Berhasil dan Memilih Mengunduh Bukti: Setelah pengajuan tersimpan dan mencapai extension point pada tampilan konfirmasi, kondisi terpenuhi sehingga sistem menjalankan perilaku tambahan untuk mengunduh/mencetak bukti pengajuan.

Selain itu, pembedaan antara prasyarat (pengguna telah terautentikasi) dengan relasi include berhasil menjaga diagram tetap fokus pada perilaku inti tanpa menambahkan use case Login secara berlebihan. Berdasarkan pemeriksaan checklist kualitas dan uji buka ulang sumber, arah panah include dan extend, penamaan ID, serta sinkronisasi antara berkas sumber .drawio dan ekspor .png telah sesuai. [Jika ada revisi ke v02 setelah review teman/asisten, tuliskan di sini; jika tidak ada, tulis: Tidak ditemukan kesalahan arah relasi maupun inkonsistensi deskripsi saat review sehingga berkas tetap pada versi v01].

E. Kesimpulan
Praktikum Pertemuan 3 berhasil memodelkan kebutuhan fungsional sistem ke dalam use case diagram dan use case description secara terlacakan untuk kasus laboratorium maupun akademik. Penerapan relasi include untuk perilaku wajib dan extend untuk perilaku bersyarat terbukti mampu memisahkan alur inti, validasi, serta opsi tambahan secara jelas dan konsisten.