<!-- Tabel Use Case Description Ajukan KRS -->
| Elemen | SIA-UC02 — Ajukan KRS |
| :--- | :--- |
| **Tujuan** | Menghasilkan pengajuan KRS yang valid dan tersimpan berstatus menunggu persetujuan |
| **Aktor utama** | Mahasiswa |
| **Sumber kebutuhan** | SIA-R03, SIA-R04, dan SIA-R05 |
| **Pemicu** | Mahasiswa memilih fungsi pengajuan KRS |
| **Prasyarat** | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal kuliah tersedia |
| **Pascakondisi berhasil** | Pengajuan KRS tersimpan dengan status Menunggu persetujuan |
| **Pascakondisi gagal** | Tidak ada pengajuan KRS baru yang berhasil tersimpan |
| **Include** | SIA-UC03 — Validasi KRS |
| **Extension point** | Bukti KRS tersedia, pada langkah 6 |
| **Extend** | SIA-UC04 jika [mahasiswa memilih unduh] |