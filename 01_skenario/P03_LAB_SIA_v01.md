<!-- Deskripsi Skenario -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- Tabel Kebutuhan -->
| ID | Kebutuhan tugas |
| :--- | :--- |
| SIA-R01 | Mahasiswa dapat melihat jadwal kuliah |
| SIA-R02 | Admin akademik dapat mengelola jadwal kuliah |
| SIA-R03 | Mahasiswa dapat mengajukan KRS |
| SIA-R04 | Sistem memvalidasi KRS sebagai bagian pengajuan |
| SIA-R05 | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
| SIA-R06 | Dosen wali dapat memproses persetujuan atau penolakan KRS |

<!-- Batas Sistem dan Aturan -->
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas

<!-- Tabel Identifikasi Aktor -->
| Aktor | Peran / Jenis | Tujuan Terhadap Sistem |
| :--- | :--- | :--- |
| **Mahasiswa** | Aktor Utama (Manusia) | Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan KRS. |
| **Dosen Wali** | Aktor Utama (Manusia) | Memproses keputusan (persetujuan/penolakan) KRS dan memberikan catatan keputusan. |

<!-- Tabel Katalog Use Case -->
| ID | Nama Use Case | Aktor Terkait | Peran Dalam Model | Sumber Kebutuhan |
| :---: | :--- | :--- | :--- | :---: |
| **SIA-UC01** | Lihat jadwal kuliah | Mahasiswa | Fungsi utama mahasiswa untuk melihat informasi jadwal kuliah | SIA-R01 |
| **SIA-UC02** | Ajukan KRS | Mahasiswa | Fungsi utama mahasiswa untuk memilih mata kuliah dan mengajukan KRS | SIA-R03 |
| **SIA-UC03** | Validasi KRS | *(Sistem)* | Perilaku yang disertakan oleh SIA-UC02 untuk memeriksa kelengkapan, prasyarat, dan benturan jadwal | SIA-R04 |
| **SIA-UC04** | Unduh bukti pengajuan KRS | Mahasiswa | Tambahan bersyarat pada SIA-UC02 jika mahasiswa memilih untuk mengunduh bukti | SIA-R05 |
| **SIA-UC05** | Proses keputusan KRS | Dosen Wali | Fungsi utama dosen wali untuk memproses persetujuan atau penolakan KRS serta memberikan catatan | SIA-R06 |

<!-- Relasi Include -->
SIA-UC02 «include» SIA-UC03
Alasan: pemeriksaan kelengkapan, prasyarat mata kuliah, dan benturan jadwal selalu dijalankan oleh sistem sebagai bagian dari validasi pengajuan KRS.

<!-- Relasi Extend -->
SIA-UC04 «extend» SIA-UC02
Extension point: Bukti KRS tersedia.
Kondisi: [mahasiswa memilih unduh].
Alasan: pengajuan KRS tetap berhasil tersimpan dengan status menunggu persetujuan meskipun mahasiswa tidak memilih untuk mengunduh bukti.