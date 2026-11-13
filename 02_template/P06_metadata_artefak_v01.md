1. METADATA STUDI KASUS TERBIMBING (LAB)

ID artefak                  : LAB-P06-ACT
Judul                       : Activity Diagram Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (7 Use Case Utama)
Pertemuan                   : 06
Sumber kebutuhan            : LAB-R01 s.d. LAB-R11 (Jobsheet P04) dan Dokumen Skenario P05_2406041_LAB_skenario_v01.md
Tabel skenario sumber       : LAB-UC01 (Tabel 5.3), LAB-UC02 beserta pembeda LAB-UC08 s.d. LAB-UC10 (Tabel 5.6-5.9), LAB-UC03 beserta include LAB-UC04 dan extend LAB-UC05 (Tabel 5.1, 5.4, 5.5), LAB-UC06 (Tabel 5.10), LAB-UC07 (Tabel 5.11), dan LAB-UC11 beserta include LAB-UC12 (Tabel 5.12-5.13)
Unsur activity digunakan    : Initial node, Action, Control flow, Decision, Merge, Fork, Join, Activity final node, dan Swimlane
Unsur proses baru           : Periksa kelengkapan aksesori peralatan pada Activity Pengembalian Tahap 5 (untuk melatih pasangan fork dan join bersama Periksa Kondisi Peralatan)
Jenis/status                : Activity Diagram / Tugas Praktikum (7 berkas .drawio dan .png pada 04_model_analisis/P06/LAB)
Kakas                       : draw.io
Pembuat                     : Muhammad Ramzy Sunda Permana - 2406041
Versi dan tanggal           : v01 / 06-11-2026
Asumsi                      : Hak akses sesuai; autentikasi di luar latihan; diagram P04 dan skenario P05 tidak diubah
Pemeriksaan                 : Berhasil diperiksa sesuai checklist penilaian Bagian C.4 (7 diagram LAB lengkap, guard saling lepas, fork-join berpasangan, swimlane sesuai pelaku, serta perbandingan tugas mandiri LAB-UC06 telah dicocokkan dengan lampiran)
Riwayat revisi              : v01 (06-11-2026) - Pembuatan awal 7 activity diagram untuk studi kasus LAB (termasuk pengerjaan mandiri Activity Keputusan LAB-UC06 sebelum pengecekan lampiran)

------------------------------------------------------------------------

2. METADATA TUGAS PRAKTIK (SIA)

ID artefak                  : SIA-P06-ACT
Judul                       : Activity Diagram Input Nilai Mata Kuliah sampai Lihat KHS (Sistem Informasi Akademik)
Pertemuan                   : 06
Sumber kebutuhan            : SIA-R07 s.d. SIA-R12 (Jobsheet P04) dan Dokumen Skenario P05_2406041_SIA_skenario_v01.md
Tabel skenario sumber       : Tabel Skenario SIA-UC08 (Input Nilai Mata Kuliah) dan SIA-UC09 (Lihat KHS) pada Pertemuan 5
Unsur activity digunakan    : Initial node, Action, Control flow, Decision, Merge, Fork, Join, Activity final node, dan Swimlane (Dosen, Sistem, Admin Akademik, Mahasiswa)
Unsur proses baru           : Tidak ada (seluruh action tertelusur ke skenario SIA-UC08 dan SIA-UC09 Pertemuan 5)
Jenis/status                : Activity Diagram / Tugas Praktikum (1 berkas utuh .drawio dan .png pada 04_model_analisis/P06/SIA)
Kakas                       : draw.io
Pembuat                     : Muhammad Ramzy Sunda Permana - 2406041
Versi dan tanggal           : v01 / 06-11-2026
Asumsi                      : Hak akses sesuai; autentikasi di luar latihan; nilai hanya diinput dosen pengampu dan KHS hanya menampilkan nilai yang telah disahkan serta dipublikasikan
Pemeriksaan                 : Berhasil diperiksa sesuai checklist penilaian Bagian C.4 (4 swimlane sesuai aktor, decision kelengkapan nilai dengan guard dan melalui merge, serta pasangan fork-join untuk penerbitan KHS dan pengiriman pemberitahuan paralel)
Riwayat revisi              : v01 (06-11-2026) - Pembuatan awal activity diagram utuh Input Nilai Mata Kuliah sampai Lihat KHS untuk tugas praktik SIA