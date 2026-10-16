<!-- Tabel Model Analisis -->
| Sumber | Jenis Hubungan | Tujuan |
| :--- | :---: | :--- |
| **Mahasiswa** | Asosiasi | **Lihat jadwal kuliah** |
| **Mahasiswa** | Asosiasi | **Ajukan KRS** |
| **Mahasiswa** | Asosiasi | **Unduh bukti pengajuan KRS** |
| **Dosen Wali** | Asosiasi | **Proses keputusan KRS** |
| **Ajukan KRS** | <<include>> | **Validasi KRS** |
| **Unduh bukti pengajuan KRS** | <<extend>> | **Ajukan KRS** |