LAPORAN REVIEW DAN LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 2
Unified Modelling Language (UML) - Latihan Notasi Use Case Diagram

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Status Artefak : LATIHAN NOTASI

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan kedua ini bertujuan agar mahasiswa mampu menempatkan simbol aktor, use case, batas sistem, dan asosiasi pada diagram sederhana secara tepat, menggunakan penamaan aktor dan fungsi secara konsisten dengan skenario, melengkapi metadata artefak menggunakan template yang tersedia, menyimpan berkas sumber serta ekspor dengan penamaan dan nomor versi yang konsisten, serta memperbaiki kesalahan notasi dan dokumentasi berdasarkan hasil review.

B. Dasar Teori
Unified Modeling Language (UML) merupakan bahasa pemodelan standar yang digunakan untuk memvisualisasikan, merancang, dan mendokumentasikan analisis serta desain sistem berorientasi objek. Dalam pemodelan use case diagram dasar, terdapat empat komponen notasi utama yang digunakan:
1. Actor: Entitas eksternal (orang, sistem lain, atau proses) yang berinteraksi langsung dengan sistem dan ditempatkan di luar batas sistem.
2. Use Case: Fungsionalitas atau layanan yang disediakan oleh sistem kepada aktor, digambarkan dalam bentuk elips dengan label kata kerja dan ditempatkan di dalam batas sistem.
3. Batas Sistem (System Boundary): Kotak persegi panjang yang membatasi ruang lingkup sistem yang sedang dimodelkan dan memuat nama sistem pada bagian atasnya.
4. Association: Garis lurus utuh tanpa anak panah yang menghubungkan aktor dengan use case untuk menunjukkan hubungan partisipasi atau interaksi, bukan urutan langkah maupun aliran proses kerja.

C. Hasil Praktikum
Seluruh kegiatan pada Jobsheet Pertemuan 2 telah dikerjakan di dalam folder induk IFRWP5149_2406041_LabAlat dengan rincian sebagai berikut:
1. Penyiapan Struktur dan Dokumentasi: Menambahkan subfolder Pertemuan 2 pada 03_latihan_tools/P02/LAB dan 03_latihan_tools/P02/SIA, mencatat kebutuhan pada P02_LAB_skenario_v01.md serta P02_SIA_skenario_v01.md, dan mengisi P02_2406041_logbook_v01.md. Kakas yang digunakan adalah [draw.io / diagrams.net (Desktop/Web) - sesuaikan] dengan mengaktifkan pustaka simbol UML dan UML 2.5.
2. Studi Kasus Terbimbing (Kode: LAB): Membuat diagram P02_2406041_LAB_notasi_usecase_v01.drawio dan ekspor .png untuk Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus. Diagram memuat dua aktor di luar batas sistem (Mahasiswa dan Petugas laboratorium) serta dua use case di dalam batas sistem (Lihat ketersediaan peralatan dan Kelola data peralatan) yang dihubungkan sesuai kebutuhan LAB-R01 dan LAB-R02, lengkap dengan metadata ID artefak LAB-P02-UC.
3. Tugas Praktik Perbaikan Notasi (Kode: SIA): Melakukan pemeriksaan terhadap diagram awal yang keliru (P02_2406041_SIA_perbaikan_notasi_v01.drawio) dan menghasilkan diagram hasil revisi (P02_2406041_SIA_notasi_v01.drawio dan .png) untuk Sistem Informasi Akademik yang menghubungkan aktor Mahasiswa dengan Lihat jadwal kuliah, serta Admin akademik dengan Kelola jadwal kuliah.

| No. | Temuan | Perbaikan yang diperlukan | Alasan |
| :---: | :--- | :--- | :--- |
| 1 | Aktor Mahasiswa berada di dalam batas sistem. | Pindahkan Mahasiswa ke luar batas sistem. | Aktor merupakan pihak yang berinteraksi dengan sistem. |
| 2 | Fungsi Lihat jadwal kuliah berbentuk kotak biasa. | Ubah bentuknya menjadi elips. | Use case digambarkan menggunakan elips. |
| 3 | Mahasiswa terhubung dengan Kelola jadwal kuliah. | Hubungkan Mahasiswa dengan Lihat jadwal kuliah. | Hubungan aktor harus sesuai dengan skenario tugas. |
| 4 | Judul diagram menggunakan nama sistem laboratorium. | Ganti judul menjadi Sistem Informasi Akademik. | Judul diagram harus sesuai dengan sistem yang dimodelkan. |

D. Analisis
Berdasarkan pemeriksaan pada tugas praktik kasus SIA, ditemukan empat kesalahan notasi mendasar yang berhasil diperbaiki beserta alasan konseptualnya:
1. Temuan: Aktor Mahasiswa ditempatkan di dalam batas sistem.
   Perbaikan dan Alasan: Aktor dipindahkan ke luar persegi panjang batas sistem karena aktor adalah pengguna eksternal yang berinteraksi dengan sistem, bukan komponen internal sistem.
2. Temuan: Fungsi "Lihat jadwal kuliah" digambarkan menggunakan bentuk kotak biasa.
   Perbaikan dan Alasan: Simbol diubah menjadi bentuk elips karena dalam standar UML, elips merupakan representasi resmi untuk use case atau fungsionalitas sistem.
3. Temuan: Aktor Mahasiswa dihubungkan dengan fungsi "Kelola jadwal kuliah".
   Perbaikan dan Alasan: Garis asosiasi dialihkan sehingga Mahasiswa hanya terhubung ke "Lihat jadwal kuliah", sedangkan "Kelola jadwal kuliah" dihubungkan ke Admin akademik agar sesuai dengan batasan skenario SIA-R01 dan SIA-R02.
4. Temuan: Judul batas sistem masih menggunakan nama sistem laboratorium.
   Perbaikan dan Alasan: Judul diubah menjadi "Sistem Informasi Akademik" untuk menjaga konsistensi identitas antara skenario, diagram, dan metadata kasus SIA.

Secara konseptual, garis asosiasi pada kedua diagram digambar tanpa anak panah karena berfungsi menunjukkan keterlibatan aktor dalam menjalankan fungsi sistem, bukan menggambarkan alur urutan aktivitas. Selain itu, berdasarkan hasil review dan uji buka ulang sumber, seluruh berkas .drawio dapat dibuka kembali dari direktori proyek untuk disunting dan sinkron dengan berkas ekspor .png. [Jika ada revisi ke v02 setelah review teman/asisten, tuliskan di sini; jika tidak ada, tulis: Tidak ditemukan kesalahan notasi lanjutan saat pemeriksaan checklist sehingga versi berkas tetap pada v01].

E. Kesimpulan
Praktikum Pertemuan 2 berhasil dilaksanakan dengan menerapkan aturan penempatan notasi dasar use case diagram (aktor, use case, batas sistem, dan asosiasi) secara konsisten pada studi kasus laboratorium maupun tugas perbaikan sistem informasi akademik. Pemisahan folder kasus LAB dan SIA serta kelengkapan metadata memastikan seluruh artefak latihan siap digunakan sebagai dasar pada pertemuan analisis berikutnya.