# SKENARIO USE CASE – SISTEM INFORMASI AKADEMIK, LAYANAN HASIL STUDI

Praktikum ADBO (IFRWP5149) – Pertemuan 5

Nama / NIM: ______________________  |  S1 Teknik Informatika, Institut Teknologi Garut

Berkas: `P05_<NIM>_SIA_skenario_v01.docx` (folder `01_skenario`). Diagram SIA P04 tidak diubah.

## Indeks tabel skenario

| ID | Nama use case | Aktor |
|---|---|---|
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen |
| SIA-UC09 | Lihat KHS | Mahasiswa |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik |

## Tabel 5.15 Skenario Use Case SIA-UC07 Lihat Kalender Akademik

| | |
|---|---|
| **Nama use case** | SIA-UC07 Lihat Kalender Akademik |
| **Aktor** | Civitas Akademika (berlaku untuk Mahasiswa dan Dosen) |
| **Tujuan** | Civitas akademika dapat mengetahui jadwal kegiatan akademik pada periode yang dipilih |
| **Deskripsi** | Civitas Akademika membuka fungsi kalender akademik, memilih periode akademik, dan melihat kalender akademik periode tersebut |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Civitas Akademika membuka fungsi Lihat Kalender Akademik | 2. Sistem menampilkan daftar periode akademik (tahun akademik dan semester) |
| 3. Civitas Akademika memilih periode akademik | 4. Sistem menampilkan kalender akademik periode tersebut beserta tanggal kegiatan akademik |
| **Skenario Alternative** | |
| 5. Kalender akademik periode yang dipilih belum tersedia (cabang dari langkah 4) | 6. Sistem menampilkan pesan kalender akademik periode tersebut belum tersedia |
| **Skenario Akhir** | Use case selesai jika kalender akademik periode yang dipilih ditampilkan; jika kalender belum tersedia, use case selesai dengan pesan tersebut. |

*Keterangan: skenario ditulis satu kali atas nama aktor umum Civitas Akademika dan berlaku untuk Mahasiswa dan Dosen karena keduanya mewarisi SIA-UC07 dari Civitas Akademika. Tidak ada tabel terpisah untuk Mahasiswa maupun Dosen karena perilakunya sama.*

## Tabel 5.16 Skenario Use Case SIA-UC08 Input Nilai Mata Kuliah

| | |
|---|---|
| **Nama use case** | SIA-UC08 Input Nilai Mata Kuliah |
| **Aktor** | Dosen (prasyarat: dosen pengampu mata kuliah yang dipilih) |
| **Tujuan** | Nilai mahasiswa pada mata kuliah tercatat oleh dosen pengampu |
| **Deskripsi** | Dosen pengampu memilih mata kuliah yang diampu, mengisi nilai mahasiswa peserta, dan menyimpan nilai |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Dosen membuka fungsi Input Nilai Mata Kuliah | 2. Sistem menampilkan daftar mata kuliah yang diampu dosen tersebut |
| 3. Dosen memilih mata kuliah | 4. Sistem menampilkan daftar mahasiswa peserta beserta kolom nilai |
| 5. Dosen mengisi nilai mahasiswa | 6. Sistem memeriksa nilai berada dalam rentang yang sah |
| 7. Dosen menyimpan nilai | 8. Sistem menyimpan nilai mahasiswa dan menampilkan konfirmasi penyimpanan |
| **Skenario Alternative** | |
| 9. Nilai yang diisi di luar rentang yang sah (cabang dari langkah 6) | 10. Sistem menolak penyimpanan dan menampilkan pesan nilai di luar rentang yang sah |
| 11. Dosen memilih mata kuliah yang bukan diampunya (cabang dari langkah 3) | 12. Sistem menolak akses input nilai dan menampilkan pesan hanya dosen pengampu yang dapat menginput nilai |
| **Skenario Akhir** | Use case selesai jika nilai mahasiswa tersimpan; jika nilai di luar rentang yang sah atau dosen bukan pengampu, nilai tidak tersimpan. |

*Keterangan: use case ini direalisasikan oleh collaboration SIA-CO01. Collaboration tersebut tidak mempunyai langkah kegiatan pada tabel ini.*

## Tabel 5.17 Skenario Use Case SIA-UC09 Lihat KHS

| | |
|---|---|
| **Nama use case** | SIA-UC09 Lihat KHS |
| **Aktor** | Mahasiswa |
| **Tujuan** | Mahasiswa dapat mengetahui hasil studinya pada semester yang dipilih |
| **Deskripsi** | Mahasiswa membuka fungsi KHS, memilih semester, dan melihat daftar mata kuliah beserta nilai yang sudah dipublikasikan |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Mahasiswa membuka fungsi Lihat KHS | 2. Sistem menampilkan daftar semester milik mahasiswa tersebut |
| 3. Mahasiswa memilih semester | 4. Sistem menampilkan KHS semester tersebut berisi mata kuliah dan nilai yang sudah dipublikasikan |
| **Skenario Alternative** | |
| 5. Belum ada nilai yang dipublikasikan pada semester yang dipilih (cabang dari langkah 4) | 6. Sistem menampilkan pesan belum ada nilai yang dipublikasikan pada semester tersebut |
| **Skenario Akhir** | Use case selesai jika KHS semester yang dipilih ditampilkan dengan nilai yang sudah dipublikasikan; jika belum ada nilai yang dipublikasikan, use case selesai dengan pesan tersebut. |

*Keterangan: use case ini direalisasikan oleh collaboration SIA-CO02. Collaboration tersebut tidak mempunyai langkah kegiatan pada tabel ini. Nilai yang belum dipublikasikan tidak ditampilkan pada KHS.*

## Tabel 5.18 Skenario Use Case SIA-UC10 Kelola Data Mahasiswa

| | |
|---|---|
| **Nama use case** | SIA-UC10 Kelola Data Mahasiswa |
| **Aktor** | Admin Akademik |
| **Tujuan** | Data mahasiswa terkelola melalui satu fungsi pengelolaan bersama |
| **Deskripsi** | Admin Akademik membuka fungsi pengelolaan data mahasiswa, memilih bentuk pengelolaan, dan menyimpan perubahan. Bentuk tambah, ubah, dan hapus dijabarkan pada tabel khususnya masing-masing (SIA-UC11, SIA-UC12, dan SIA-UC13) |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Admin Akademik membuka fungsi Kelola Data Mahasiswa | 2. Sistem menampilkan daftar data mahasiswa |
| 3. Admin Akademik memilih bentuk pengelolaan, yaitu tambah, ubah, atau hapus | 4. Sistem menampilkan formulir sesuai bentuk pengelolaan yang dipilih |
| 5. Admin Akademik memasukkan data sesuai bentuk pengelolaan yang dipilih | 6. Sistem memeriksa kelengkapan dan keabsahan data |
| 7. Admin Akademik menyimpan perubahan | 8. Sistem menyimpan perubahan dan menampilkan konfirmasi |
| **Skenario Alternative** | |
| 9. Data tidak lengkap atau tidak sah (cabang dari langkah 6) | 10. Sistem menolak penyimpanan dan menampilkan pesan kesalahan data |
| **Skenario Akhir** | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak lengkap atau tidak sah, perubahan tidak tersimpan. |

*Keterangan: skenario umum pengelolaan. Langkah bersama ini dirujuk oleh SIA-UC11, SIA-UC12, dan SIA-UC13.*

## Tabel 5.19 Skenario Use Case SIA-UC11 Tambah Data Mahasiswa

| | |
|---|---|
| **Nama use case** | SIA-UC11 Tambah Data Mahasiswa |
| **Aktor** | Admin Akademik |
| **Tujuan** | Data mahasiswa baru tersimpan sebagai bentuk khusus dari pengelolaan data mahasiswa |
| **Deskripsi** | Admin Akademik mengisi data mahasiswa baru dan menyimpannya; langkah bersama mengikuti Tabel skenario SIA-UC10 |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Admin Akademik membuka fungsi Tambah Data Mahasiswa | 2. Sistem menampilkan formulir data mahasiswa baru |
| 3. Admin Akademik mengisi data mahasiswa baru | 4. Sistem memeriksa kelengkapan data |
| 5. Admin Akademik menyimpan data | 6. Sistem menyimpan data mahasiswa baru dan menampilkan konfirmasi |
| **Skenario Alternative** | |
| 7. Data tidak lengkap (cabang dari langkah 4) | 8. Sistem menolak penyimpanan dan meminta Admin Akademik melengkapi data |
| **Skenario Akhir** | Use case selesai jika data mahasiswa baru tersimpan; jika data tidak lengkap, data tidak tersimpan. |

*Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa baru tersimpan. Langkah bersama mengikuti Tabel skenario SIA-UC10.*

## Tabel 5.20 Skenario Use Case SIA-UC12 Ubah Data Mahasiswa

| | |
|---|---|
| **Nama use case** | SIA-UC12 Ubah Data Mahasiswa |
| **Aktor** | Admin Akademik |
| **Tujuan** | Data mahasiswa berubah sebagai bentuk khusus dari pengelolaan data mahasiswa |
| **Deskripsi** | Admin Akademik memilih data mahasiswa, mengubah datanya, dan menyimpan perubahan; langkah bersama mengikuti Tabel skenario SIA-UC10 |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Admin Akademik memilih data mahasiswa yang akan diubah | 2. Sistem menampilkan data mahasiswa saat ini |
| 3. Admin Akademik mengubah data mahasiswa | 4. Sistem memeriksa perubahan data |
| 5. Admin Akademik menyimpan perubahan | 6. Sistem menyimpan data yang diubah dan menampilkan konfirmasi |
| **Skenario Alternative** | |
| 7. Data mahasiswa tidak ditemukan (cabang dari langkah 2) | 8. Sistem menampilkan pesan data mahasiswa tidak ditemukan |
| **Skenario Akhir** | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak ditemukan, perubahan tidak tersimpan. |

*Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa berubah. Langkah bersama mengikuti Tabel skenario SIA-UC10.*

## Tabel 5.21 Skenario Use Case SIA-UC13 Hapus Data Mahasiswa

| | |
|---|---|
| **Nama use case** | SIA-UC13 Hapus Data Mahasiswa |
| **Aktor** | Admin Akademik |
| **Tujuan** | Data mahasiswa terhapus sebagai bentuk khusus dari pengelolaan data mahasiswa |
| **Deskripsi** | Admin Akademik memilih data mahasiswa, mengonfirmasi penghapusan, dan sistem menghapus data tersebut; langkah bersama mengikuti Tabel skenario SIA-UC10 |
| **Kegiatan** | **Respon sistem** |
| **Skenario Normal** | |
| 1. Admin Akademik memilih data mahasiswa yang akan dihapus | 2. Sistem memeriksa mahasiswa tidak memiliki data akademik aktif |
| 3. Admin Akademik mengonfirmasi penghapusan | 4. Sistem menghapus data mahasiswa dan menampilkan konfirmasi penghapusan |
| **Skenario Alternative** | |
| 5. Mahasiswa memiliki data akademik aktif (cabang dari langkah 2) | 6. Sistem menolak penghapusan dan menampilkan pesan mahasiswa masih memiliki data akademik aktif |
| **Skenario Akhir** | Use case selesai jika data mahasiswa terhapus; jika mahasiswa memiliki data akademik aktif, data tidak terhapus. |

*Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa terhapus, dengan syarat tidak ada data akademik aktif. Langkah bersama mengikuti Tabel skenario SIA-UC10.*

## Pemeriksaan mandiri (checklist C.4)

| No. | Butir | Hasil |
|---|---|---|
| 1 | Seluruh field terisi pada 7 tabel | ✓ |
| 2 | Satu aksi per langkah; penomoran Normal → Alternative berlanjut | ✓ |
| 3 | Kolom Kegiatan = aksi aktor; Respon sistem = tanggapan sistem | ✓ |
| 4 | Generalization aktor: UC07 ditulis satu kali atas nama Civitas Akademika (Mahasiswa dan Dosen) | ✓ |
| 5 | Generalization use case: UC10 umum; UC11, UC12, UC13 memuat perilaku pembeda dan merujuk Tabel UC10 | ✓ |
| 6 | Collaboration: SIA-CO01 pada keterangan UC08; SIA-CO02 pada keterangan UC09; tanpa langkah sendiri | ✓ |
| 7 | Setiap tabel punya Skenario Alternative dan Skenario Akhir | ✓ |
| 8 | ID, nama use case, dan aktor sama dengan Tabel 5.14 / diagram SIA P04; tidak ada use case, aktor, atau kebutuhan baru | ✓ |
| 9 | Aturan khusus: hanya dosen pengampu dapat input nilai; KHS hanya nilai terpublikasi; hapus hanya tanpa data akademik aktif | ✓ |

> Catatan untuk dicek: rentang nilai yang sah pada SIA-UC08 ditulis umum. Sesuaikan jika Tabel 4.6 pada Jobsheet Pertemuan 4 menyebut rentang atau status publikasi nilai.

## Logbook

| Tanggal | Kegiatan | Status |
|---|---|---|
| 26 Okt 2026 | Membaca Jobsheet Pertemuan 5 dan mencocokkan struktur tabel dengan Tabel 5.1 | Selesai |
| 26 Okt 2026 | Menulis 7 tabel skenario tugas SIA (UC07–UC13) | Selesai |
| 26 Okt 2026 | Pemeriksaan dengan checklist bagian C.4 | Selesai |
