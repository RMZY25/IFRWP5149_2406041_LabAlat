### Tabel Identifikasi Aktor Umum dan Aktor Khusus
| Aktor | Kedudukan | Tujuan terhadap sistem |
| :--- | :--- | :--- |
| **Civitas Akademika** | Umum (*general*), baru pada Pertemuan 4 | Peran umum bagi pengguna layanan akademik kampus. Mewariskan fungsi melihat kalender akademik kepada Mahasiswa dan Dosen. |
| **Mahasiswa** | Khusus dari Civitas Akademika, tetap dari Pertemuan 2 & 3 | Melihat kalender akademik (diwarisi dari Civitas Akademika), melihat jadwal kuliah, mengajukan KRS, mengunduh bukti pengajuan KRS, dan melihat KHS sebagai asosiasi khususnya sendiri. |
| **Dosen** | Khusus dari Civitas Akademika, baru pada Pertemuan 4 | Melihat kalender akademik (diwarisi dari Civitas Akademika), ditambah menginput nilai mata kuliah yang diampunya sebagai asosiasi khususnya sendiri. |
| **Admin Akademik** | Tetap dari Pertemuan 2 & 3 | Mengelola jadwal kuliah dan mengelola data mahasiswa (tambah, ubah, dan hapus data mahasiswa). |
| **Dosen Wali** | Tetap dari Pertemuan 3 | Melakukan validasi KRS dan memproses keputusan KRS mahasiswa bimbingannya. |

### Tabel Katalog Use Case
| ID | Nama use case | Peran dalam model | Sumber kebutuhan |
| :--- | :--- | :--- | :--- |
| **SIA-UC01** | Lihat Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi khusus Mahasiswa | SIA-R01 |
| **SIA-UC02** | Kelola Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi utama Admin Akademik | SIA-R02 |
| **SIA-UC03** | Ajukan KRS | Tetap dari Pertemuan 3; fungsi khusus Mahasiswa; menyertakan SIA-UC04 | SIA-R03 |
| **SIA-UC04** | Validasi KRS | Tetap dari Pertemuan 3; perilaku yang disertakan SIA-UC03 | SIA-R03 |
| **SIA-UC05** | Unduh Bukti Pengajuan KRS | Tetap dari Pertemuan 3; tambahan bersyarat pada SIA-UC03 melalui «extend» | SIA-R04 |
| **SIA-UC06** | Proses Keputusan KRS | Tetap dari Pertemuan 3; fungsi utama Dosen Wali | SIA-R05, SIA-R06 |
| **SIA-UC07** | Lihat Kalender Akademik | Baru pada Pertemuan 4; fungsi aktor umum Civitas Akademika | SIA-R07 |
| **SIA-UC08** | Input Nilai Mata Kuliah | Baru pada Pertemuan 4; fungsi khusus Dosen; direalisasikan SIA-CO01 | SIA-R08, SIA-R12 |
| **SIA-UC09** | Lihat KHS | Baru pada Pertemuan 4; fungsi khusus Mahasiswa; direalisasikan SIA-CO02 | SIA-R09, SIA-R12 |
| **SIA-UC10** | Kelola Data Mahasiswa | Baru pada Pertemuan 4; use case UMUM bagi SIA-UC11, SIA-UC12, SIA-UC13 | SIA-R10, SIA-R11 |
| **SIA-UC11** | Tambah Data Mahasiswa | Baru pada Pertemuan 4; use case KHUSUS dari SIA-UC10 | SIA-R11 |
| **SIA-UC12** | Ubah Data Mahasiswa | Baru pada Pertemuan 4; use case KHUSUS dari SIA-UC10 | SIA-R11 |
| **SIA-UC13** | Hapus Data Mahasiswa | Baru pada Pertemuan 4; use case KHUSUS dari SIA-UC10 | SIA-R11 |

### Generalization Aktor
• Mahasiswa adalah bentuk khusus dari Civitas Akademika, dan Dosen adalah bentuk khusus dari Civitas Akademika. Alasan: keduanya berbagi fungsi yang sama, yaitu melihat kalender akademik.
• Asosiasi ke SIA-UC07 Lihat Kalender Akademik digambar satu kali, yaitu dari Civitas Akademika. Jangan menggambar garis yang sama dari Mahasiswa dan dari Dosen.
• Asosiasi khusus Mahasiswa ke SIA-UC01 (Lihat Jadwal Kuliah), SIA-UC03 (Ajukan KRS), SIA-UC05 (Unduh Bukti Pengajuan KRS), dan SIA-UC09 (Lihat KHS) tidak ikut dipindahkan dan tidak dihapus, karena fungsi-fungsi tersebut khusus mahasiswa. Asosiasi ini menjadi contoh asosiasi tambahan milik aktor khusus.
• Periksa arah panah pada gambar: ujung segitiga kosong harus menempel pada Civitas Akademika, bukan pada Mahasiswa dan bukan pada Dosen. Panah dari Mahasiswa dan panah dari Dosen keduanya berakhir dan menunjuk ke Civitas Akademika.

### Generalization Use Case
• SIA-UC11 (Tambah Data Mahasiswa), SIA-UC12 (Ubah Data Mahasiswa), dan SIA-UC13 (Hapus Data Mahasiswa) adalah bentuk khusus dari SIA-UC10 Kelola Data Mahasiswa. Alasan: ketiganya merupakan bentuk spesifik dari pengelolaan data mahasiswa oleh Admin Akademik.
• Tambah Data Mahasiswa menghasilkan data mahasiswa baru yang tersimpan di sistem.
• Ubah Data Mahasiswa menghasilkan pembaruan atau perubahan data mahasiswa yang sudah ada.
• Hapus Data Mahasiswa menghasilkan data mahasiswa yang terhapus dari sistem, dengan syarat mahasiswa tersebut tidak memiliki data akademik aktif.
• Periksa arah panah pada gambar: ketiga panah generalization digambar dari masing-masing use case khusus (SIA-UC11, SIA-UC12, SIA-UC13) menuju use case umum (SIA-UC10), dengan ujung segitiga kosong menempel pada SIA-UC10.
• Aktor Admin Akademik cukup dihubungkan dengan satu garis asosiasi ke use case umum SIA-UC10 Kelola Data Mahasiswa, tidak perlu ditarik garis ke seluruh use case khusus.

### Collaboration dan Realization
| ID | Nama collaboration (sama dengan nama use case) | Use case yang direalisasikan |
| :--- | :--- | :--- |
| **SIA-CO01** | Input Nilai Mata Kuliah | SIA-UC08: Input Nilai Mata Kuliah |
| **SIA-CO02** | Lihat KHS | SIA-UC09: Lihat KHS |

### Deskripsi Use Case (Input Nilai Mata Kuliah)
| Elemen | SIA-UC08: Input Nilai Mata Kuliah |
| :--- | :--- |
| **ID dan nama** | SIA-UC08: Input Nilai Mata Kuliah |
| **Sumber kebutuhan** | SIA-R08 dan SIA-R12 |
| **Tujuan** | Menyimpan data nilai mata kuliah mahasiswa yang diampu oleh dosen |
| **Aktor utama** | Dosen |
| **Pemicu** | Dosen memilih menu pengisian nilai mata kuliah setelah perkuliahan atau ujian selesai |
| **Prasyarat** | Dosen telah terautentikasi; Dosen adalah pengampu resmi dari mata kuliah yang dipilih |
| **Pascakondisi berhasil** | Nilai mata kuliah tersimpan di sistem dan siap untuk dipublikasikan |
| **Pascakondisi gagal** | Nilai mata kuliah tidak tersimpan; data nilai di sistem tidak mengalami perubahan |
| **Collaboration** | SIA-CO01: Input Nilai Mata Kuliah |

### Deskripsi Use Case (Lihat KHS)
| Elemen | SIA-UC09: Lihat KHS |
| :--- | :--- |
| **ID dan nama** | SIA-UC09: Lihat KHS |
| **Sumber kebutuhan** | SIA-R09 dan SIA-R12 |
| **Tujuan** | Menampilkan Kartu Hasil Studi (KHS) mahasiswa untuk semester yang telah dipublikasikan |
| **Aktor utama** | Mahasiswa |
| **Pemicu** | Mahasiswa memilih menu Lihat KHS dan menentukan semester yang ingin dilihat |
| **Prasyarat** | Mahasiswa telah terautentikasi; nilai semester yang dipilih sudah dinyatakan dipublikasikan secara resmi |
| **Pascakondisi berhasil** | Tampilan daftar nilai KHS beserta IP/IPK semester terpilih muncul pada layar |
| **Pascakondisi gagal** | KHS tidak ditampilkan; sistem memberikan informasi status publikasi nilai |
| **Collaboration** | SIA-CO02: Lihat KHS |