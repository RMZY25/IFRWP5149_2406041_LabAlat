LAPORAN REVIEW DAN LAPORAN SINGKAT PRAKTIKUM PERTEMUAN 5
Skenario Use Case: Dari Diagram ke Langkah Kegiatan

Mata Kuliah : Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)
NIM : 2406041
Nama : Muhammad Ramzy Sunda Permana
Status Artefak : SKENARIO USE CASE

------------------------------------------------------------------------

A. Tujuan Praktikum
Praktikum pertemuan kelima ini bertujuan agar mahasiswa mampu menyusun tabel skenario use case secara terstruktur dan lengkap (mencakup baris Nama use case, Aktor, Tujuan, Deskripsi, kolom Kegiatan dan Respon sistem, Skenario Normal, Skenario Alternative, serta Skenario Akhir), menuliskan langkah interaksi secara berurutan dengan pemisahan aksi aktor dan tanggapan sistem serta penomoran berlanjut, memetakan seluruh relasi diagram (include, extend, generalization aktor, generalization use case, dan collaboration) ke dalam langkah skenario secara tepat, serta menelaah konsistensi tabel skenario terhadap diagram kumulatif Pertemuan 4.

B. Dasar Teori
Skenario use case merupakan uraian langkah demi langkah yang menjelaskan bagaimana interaksi antara aktor eksternal dan sistem berlangsung dari awal hingga kondisi akhir tercapai. Skenario melengkapi use case diagram dengan urutan langkah operasional yang dapat diuji satu per satu tanpa mengubah atau menggambar ulang diagram acuan. Dalam menyusun tabel skenario dua kolom (kolom Kegiatan untuk aksi aktor dan kolom Respon sistem untuk tanggapan sistem), berlaku aturan pemetaan relasi sebagai berikut:
1. Relasi Include: Dipetakan sebagai langkah rujukan wajib di dalam Skenario Normal pada urutan yang sesuai tanpa menyalin langkah dari tabel use case yang disertakan.
2. Relasi Extend: Dipetakan sebagai cabang bersyarat pada Skenario Alternative yang dilengkapi dengan condition dan extension point, sementara use case dasar tetap dapat selesai meski cabang ini tidak dijalankan.
3. Generalization Aktor dan Use Case: Skenario aktor umum ditulis satu kali beserta catatan aktor khusus yang berlaku, sedangkan skenario use case umum memuat perilaku bersama dan masing-masing use case khusus hanya memuat perilaku pembedanya.
4. Collaboration dan Realization: Tidak dibuatkan tabel maupun langkah kegiatan tersendiri, melainkan cukup dicantumkan pada keterangan tabel use case yang direalisasikannya.

C. Hasil Praktikum
Seluruh pekerjaan pada Pertemuan 5 disusun dengan menjadikan diagram kumulatif Pertemuan 4 sebagai acuan tanpa mengubah berkas diagram P04 di dalam folder proyek IFRWP5149_2406041_LabAlat:

1. Studi Kasus Terbimbing - Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (Kode: LAB):
   - Berkas: P05_2406041_LAB_skenario_v01.md pada folder 01_skenario dan logbook P05_2406041_logbook_v01.md.
   - Hasil Telaah 12 Tabel Skenario: Melakukan pemeriksaan dan pencocokan 12 tabel skenario yang terbagi ke dalam empat kelompok: peminjaman (LAB-UC01, LAB-UC03, LAB-UC04, LAB-UC05), pengelolaan data (LAB-UC02, LAB-UC08, LAB-UC09, LAB-UC10), keputusan dan laporan (LAB-UC06, LAB-UC07), serta pengembalian (LAB-UC11, LAB-UC12). Setiap tabel telah dilengkapi kolom penelusuran relasi terhadap 5 aktor, 12 use case, 2 collaboration, dan 17 hubungan pada diagram acuan P04_2406041_LAB_usecase_v01.drawio.

2. Tugas Praktik - Sistem Informasi Akademik, Layanan Hasil Studi (Kode: SIA):
   - Berkas: Dokumen skenario untuk 7 use case pada folder 01_skenario yang disusun mengacu pada diagram kumulatif P04_2406041_SIA_usecase_v01.drawio.
   - Hasil Penyusunan 7 Tabel Skenario: Menyusun tabel skenario lengkap untuk SIA-UC07 (Lihat Kalender Akademik atas nama aktor umum Civitas Akademika untuk Mahasiswa dan Dosen), SIA-UC08 (Input Nilai Mata Kuliah oleh Dosen dengan keterangan realisasi SIA-CO01), SIA-UC09 (Lihat KHS oleh Mahasiswa dengan keterangan realisasi SIA-CO02), SIA-UC10 (Kelola Data Mahasiswa sebagai skenario umum bagi Admin Akademik), serta SIA-UC11, SIA-UC12, dan SIA-UC13 (Tambah, Ubah, dan Hapus Data Mahasiswa sebagai skenario khusus yang memuat perilaku pembeda).

D. Analisis
Berdasarkan pemeriksaan terhadap struktur penulisan dan pencocokan checklist kualitas Pertemuan 5, penerapan penomoran berlanjut dari Skenario Normal ke Skenario Alternative terbukti menghilangkan ambiguitas rujukan cabang, karena setiap langkah penyimpangan langsung menunjuk nomor langkah asal (dengan frasa cabang dari langkah N). Pemisahan aksi aktor pada kolom Kegiatan dan tanggapan sistem pada kolom Respon sistem dengan satu aksi per langkah juga membuat alur interaksi mudah ditelusuri dan diuji.

Pada penelaahan kasus LAB, tercatat bahwa tabel skenario LAB-UC07 (Lihat Laporan Peminjaman) untuk aktor Kepala Laboratorium berdiri sendiri tanpa memuat rujukan include, extend, generalization, maupun realization, selaras dengan diagram kumulatif Pertemuan 4. Pada tugas SIA, penerapan pewarisan pada SIA-UC07 berhasil menghindari penulisan tabel ganda untuk Mahasiswa dan Dosen, sementara pembagian SIA-UC10 dengan SIA-UC11 hingga SIA-UC13 menjaga pemisahan antara langkah pengelolaan umum dengan aturan khusus (seperti syarat penghapusan hanya bagi mahasiswa tanpa data akademik aktif). Seluruh berkas skenario juga telah diperiksa agar tidak mengubah berkas acuan P04. [Jika ada kendala atau perbaikan setelah review, tuliskan di sini; jika tidak ada, tulis: Tidak ditemukan ketidaksesuaian nama, ID, maupun pemetaan relasi saat pemeriksaan checklist sehingga berkas tetap pada versi v01].

E. Kesimpulan
Praktikum Pertemuan 5 berhasil menjabarkan elemen dan relasi pada use case diagram kumulatif menjadi langkah-langkah interaksi operasional dalam bentuk tabel skenario. Seluruh 12 tabel skenario studi kasus laboratorium telah ditelaah keterlacakannya dan 7 tabel skenario layanan hasil studi akademik telah disusun secara konsisten sesuai kaidah pemetaan relasi UML.