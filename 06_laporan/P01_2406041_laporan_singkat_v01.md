LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 1
Pengenalan Lingkungan Praktikum dan Kakas Pemodelan UML

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Studi Kasus : Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus
Status Artefak : Latihan - Belum Divalidasi Sebagai Model Proses

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan pertama ini bertujuan untuk memastikan mahasiswa mampu menyiapkan ruang kerja (workspace) proyek pemodelan yang tertib sesuai standar operasional, mengoperasikan fitur-fitur dasar kakas pemodelan UML (membuat kanvas baru, menambahkan elemen, menghubungkan relasi, menyimpan, dan mengekspor), serta membuktikan bahwa berkas sumber diagram dapat dibuka dan disunting kembali untuk pekerjaan analisis pada pertemuan berikutnya.

B. Dasar Teori
Unified Modeling Language (UML) merupakan bahasa pemodelan visual yang digunakan dalam analisis dan perancangan sistem berorientasi objek, sedangkan aplikasi seperti draw.io (diagrams.net), Visual Paradigm, dan StarUML adalah kakas (tools) untuk menggambar serta mengelola model tersebut. Dalam pengelolaan proyek pemodelan, terdapat perbedaan mendasar antara berkas sumber (seperti format .drawio) yang menyimpan struktur objek diagram agar dapat diedit ulang, dengan berkas hasil ekspor (seperti .png atau .svg) yang berfungsi sebagai media peninjauan visual. Selain itu, pemisahan direktori antara artefak latihan uji kakas dengan artefak model analisis tervalidasi sangat penting dilakukan agar draf awal tidak tertukar dengan spesifikasi sistem yang telah disahkan.

C. Hasil Praktikum
Seluruh artefak dan prosedur kerja pada Jobsheet Pertemuan 1 telah berhasil diselesaikan dalam folder proyek IFRWP5149_2406041_LabAlat dengan rincian sebagai berikut:
1. Pembuatan Struktur Workspace: Menyiapkan folder induk beserta tujuh subfolder sesuai SOP (00_administrasi hingga 06_laporan). Folder 04_model_analisis dan 05_model_desain dibiarkan kosong sesuai ketentuan.
2. Dokumentasi Administrasi dan Skenario: Melengkapi identitas proyek pada README.md, mencatat ruang lingkup latihan pada S-ORI-01_orientasi_kasus_v01.md, menyiapkan template_metadata_artefak_v01.md, serta mengisi catatan kegiatan pada P01_2406041_logbook_v01.md.
3. Pembuatan Diagram Aktivitas Latihan (S-ORI-01): Menggunakan kakas [draw.io / diagrams.net (Desktop/Web) - sesuaikan] untuk membuat diagram aktivitas sederhana berisi empat elemen berurutan (node awal -> aktivitas "Buka daftar peralatan" -> aktivitas "Lihat informasi ketersediaan" -> node akhir aktivitas) yang dihubungkan dengan tiga garis alur kontrol. Berkas disimpan sebagai P01_2406041_latihan_activity_v01.drawio dan diekspor menjadi P01_2406041_latihan_activity_v01.png dengan status latihan belum divalidasi.
4. Uji Buka Ulang (Re-open Test): Berkas sumber .drawio ditutup sepenuhnya lalu dibuka kembali langsung dari folder 03_latihan_tools. Posisi elemen sempat digeser untuk menguji kemampuan penyuntingan, kemudian disimpan dan diekspor ulang agar berkas gambar sinkron dengan berkas sumber.

D. Analisis
Berdasarkan hasil pengujian dan pemeriksaan checklist validasi, struktur penamaan berkas dengan pola P01_2406041_jenis_v01 terbukti memudahkan pelacakan versi serta menjaga konsistensi antara berkas sumber dan hasil ekspor. Pemisahan folder 03_latihan_tools dari folder model utama berhasil menjaga kejelasan status artefak bahwa diagram S-ORI-01 murni merupakan uji operasional kakas, bukan aturan bisnis final. 

Terkait kendala selama praktik, [contoh: tidak ditemukan hambatan teknis yang berarti pada kakas pemodelan / atau tulis kendala spesifik Anda dan solusinya, misalnya: sempat terjadi garis konektor tidak menempel pada simpul elemen, namun berhasil diperbaiki menggunakan titik sambung otomatis]. Adapun hal yang masih memerlukan konfirmasi lebih lanjut pada pertemuan berikutnya adalah aturan bisnis mengenai apakah mahasiswa wajib melakukan login sebelum melihat daftar peralatan, serta mekanisme dan pihak yang berwenang memperbarui status ketersediaan alat.

E. Kesimpulan
Lingkungan kerja praktikum beserta seluruh artefak dasar Pertemuan 1 berhasil disiapkan secara tertib pada direktori IFRWP5149_2406041_LabAlat. Pengoperasian fitur dasar kakas pemodelan UML untuk skenario S-ORI-01 berjalan dengan baik, dan hasil uji buka ulang membuktikan bahwa berkas sumber diagram tetap dapat disunting kembali untuk tahap analisis sistem selanjutnya.