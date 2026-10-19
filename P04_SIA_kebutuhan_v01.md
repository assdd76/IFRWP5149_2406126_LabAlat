# P04_SIA_kebutuhan_v01

Status: LATIHAN USE CASE DIAGRAM LANJUTAN (diagram kumulatif)
Kasus: Sistem Informasi Akademik (SIA) - Layanan Hasil Studi
NIM: 2406126

## Metadata (template Pertemuan 1 + baris tambahan Pertemuan 4)

| Elemen | Isi |
|---|---|
| Nama berkas diagram | P04_2406126_SIA_usecase_v01.drawio dan .png |
| Versi | v01 (sumber dan ekspor sama) |
| Basis | Diagram SIA Pertemuan 2 dan 3, dipertahankan utuh |
| Generalization yang digunakan | Aktor: Mahasiswa dan Dosen ke Civitas Akademika. Use case: SIA-UC11, SIA-UC12, SIA-UC13 ke SIA-UC10 |
| Collaboration yang digunakan | SIA-CO01 Input Nilai Mata Kuliah (merealisasikan SIA-UC08); SIA-CO02 Lihat KHS (merealisasikan SIA-UC09) |
| Sumber kebutuhan baru | SIA-R07 sampai SIA-R12 |

## 1. Kebutuhan

### Kebutuhan lama (tetap berlaku, tidak diulang)
SIA-R01 dan SIA-R02 (Pertemuan 2: jadwal kuliah), SIA-R03 sampai SIA-R06 (Pertemuan 3: pengajuan KRS). Artinya tidak diubah.

### Kebutuhan baru Pertemuan 4

| ID | Kebutuhan |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS |

## 2. Batas dan asumsi
- Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 (Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap punya identitas berbeda.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik adalah agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya). Tidak sama dengan jadwal kuliah Pertemuan 2.
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai yang diinput belum terpublikasi sebelum dinyatakan resmi; KHS hanya menampilkan nilai yang sudah dipublikasikan.
- Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif (ketentuan fiktif untuk latihan).
- Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari Pertemuan 3.
- Pembayaran dan perancangan basis data di luar tugas.

## 3. Pertanyaan terbuka (belum dimodelkan, bukan dianggap selesai)
- Siapa dan lewat use case apa nilai dipublikasikan? Tugas hanya menyebut nilai "dipublikasikan" tanpa menyebut use case publikasi, sehingga tidak dimodelkan.
- Berapa rentang nilai yang sah? Tugas tidak menyebut angka, jadi tidak ditentukan.
- Apakah dosen dapat mengubah nilai setelah tersimpan? Tidak disebut, tidak dimodelkan.
- Apakah Dosen Wali juga seorang Dosen? Pada diagram keduanya tetap aktor terpisah sesuai petunjuk modul.

## 4. Penyelarasan ID dengan Pertemuan 3 (penting)
Berkas SIA Pertemuan 3 (v01) memakai ID sementara SIA-UC01 sampai SIA-UC04 untuk KRS. Modul Pertemuan 4 menetapkan ID gabungan, sehingga untuk Pertemuan 4 dipakai:

| ID di berkas P03 v01 | Nama | ID resmi mulai Pertemuan 4 |
|---|---|---|
| SIA-UC01 | Ajukan KRS | SIA-UC03 |
| SIA-UC02 | Validasi KRS | SIA-UC04 |
| SIA-UC03 | Unduh bukti pengajuan KRS | SIA-UC05 |
| SIA-UC04 | Proses keputusan KRS | SIA-UC06 |

Nama use case dan semua relasinya tidak berubah, hanya nomor ID. Berkas P03 v01 tidak ditimpa; jika ingin selaras, catat sebagai perbaikan v02 pada logbook.

## 5. Katalog use case gabungan (Langkah 2)

| ID | Nama use case | Aktor terkait | Sumber kebutuhan | Tanda |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 | Tetap (Pertemuan 2) |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 | Tetap (Pertemuan 2) |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03 | Tetap (Pertemuan 3); menyertakan SIA-UC04 |
| SIA-UC04 | Validasi KRS | (lewat SIA-UC03) | SIA-R04 | Tetap (Pertemuan 3); perilaku yang disertakan |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 | Tetap (Pertemuan 3); memperluas SIA-UC03 |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 | Tetap (Pertemuan 3) |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika (diwarisi Mahasiswa dan Dosen) | SIA-R07 | Baru |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08, SIA-R12 | Baru; direalisasikan SIA-CO01 |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09, SIA-R12 | Baru; direalisasikan SIA-CO02 |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10 | Baru; use case umum |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik (diwarisi) | SIA-R11 | Baru; khusus dari SIA-UC10 |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik (diwarisi) | SIA-R11 | Baru; khusus dari SIA-UC10 |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik (diwarisi) | SIA-R11 | Baru; khusus dari SIA-UC10 |

Catatan: Admin Akademik cukup terhubung ke SIA-UC10 (use case umum), dan tidak digambar ke SIA-UC11 sampai UC13 satu per satu.

## 6. Generalization aktor (Langkah 3)
Lihat 01_skenario/P04_SIA_skenario_v01.md untuk tabel aktor lengkap. Ringkasan:
- Mahasiswa adalah bentuk khusus dari Civitas Akademika. Dosen adalah bentuk khusus dari Civitas Akademika.
- Alasan: keduanya berbagi fungsi yang sama, yaitu melihat kalender akademik.
- Asosiasi ke SIA-UC07 digambar satu kali, dari Civitas Akademika.
- Fungsi khusus tidak diwariskan: Mahasiswa punya asosiasi sendiri ke SIA-UC01, UC03, UC05, UC09; Dosen punya asosiasi sendiri ke SIA-UC08.

## 7. Generalization use case (Langkah 4)
Use case umum: **SIA-UC10 Kelola Data Mahasiswa**.

| Use case khusus | Perilaku pembeda (satu kalimat) |
|---|---|
| SIA-UC11 Tambah Data Mahasiswa | Menghasilkan data mahasiswa baru yang tersimpan |
| SIA-UC12 Ubah Data Mahasiswa | Menghasilkan data mahasiswa yang berubah |
| SIA-UC13 Hapus Data Mahasiswa | Menghasilkan data mahasiswa yang terhapus, dengan syarat mahasiswa tidak memiliki data akademik aktif |

Yang diwarisi dari SIA-UC10: tujuan (mengelola data mahasiswa), aktor terkait (Admin Akademik), dan perilaku dasar (membuka data mahasiswa). Ketiganya sah sebagai bentuk khusus karena hasilnya sejenis, yaitu data mahasiswa yang terkelola. Generalization tidak dicampur dengan include atau extend pada pasangan yang sama.

## 8. Collaboration dan realization (Langkah 5)

| ID | Nama collaboration (sama dengan nama use case) | Use case yang direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08: Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09: Lihat KHS |

Alasan: keduanya adalah use case utama pada tugas ini (SIA-R12), sehingga realisasinya ditunjukkan eksplisit. Collaboration untuk use case lain tidak digambar pada pertemuan ini. Aturan: collaboration tidak terhubung ke aktor, tidak diberi ID use case, dan panah realization selalu dari collaboration menuju use case. Kesamaan nama collaboration dan use case disengaja, bukan duplikasi.

## 9. Spesifikasi hubungan diagram kumulatif SIA (18 hubungan)

| No | Sumber | Hubungan | Tujuan | Asal |
|---|---|---|---|---|
| 1 | Civitas Akademika | Asosiasi | SIA-UC07 Lihat Kalender Akademik | Baru |
| 2 | Mahasiswa | Asosiasi | SIA-UC01 Lihat Jadwal Kuliah | Tetap (P2) |
| 3 | Mahasiswa | Asosiasi | SIA-UC03 Ajukan KRS | Tetap (P3) |
| 4 | Mahasiswa | Asosiasi | SIA-UC05 Unduh Bukti Pengajuan KRS | Tetap (P3) |
| 5 | Mahasiswa | Asosiasi | SIA-UC09 Lihat KHS | Baru |
| 6 | Dosen | Asosiasi | SIA-UC08 Input Nilai Mata Kuliah | Baru |
| 7 | Admin Akademik | Asosiasi | SIA-UC02 Kelola Jadwal Kuliah | Tetap (P2) |
| 8 | Admin Akademik | Asosiasi | SIA-UC10 Kelola Data Mahasiswa | Baru |
| 9 | Dosen Wali | Asosiasi | SIA-UC06 Proses Keputusan KRS | Tetap (P3) |
| 10 | SIA-UC03 Ajukan KRS | «include» | SIA-UC04 Validasi KRS | Tetap (P3) |
| 11 | SIA-UC05 Unduh Bukti Pengajuan KRS | «extend» | SIA-UC03 Ajukan KRS | Tetap (P3) |
| 12 | Mahasiswa | Generalization | Civitas Akademika | Baru |
| 13 | Dosen | Generalization | Civitas Akademika | Baru |
| 14 | SIA-UC11 Tambah Data Mahasiswa | Generalization | SIA-UC10 Kelola Data Mahasiswa | Baru |
| 15 | SIA-UC12 Ubah Data Mahasiswa | Generalization | SIA-UC10 Kelola Data Mahasiswa | Baru |
| 16 | SIA-UC13 Hapus Data Mahasiswa | Generalization | SIA-UC10 Kelola Data Mahasiswa | Baru |
| 17 | SIA-CO01 Input Nilai Mata Kuliah | Realization | SIA-UC08 Input Nilai Mata Kuliah | Baru |
| 18 | SIA-CO02 Lihat KHS | Realization | SIA-UC09 Lihat KHS | Baru |

Relasi extend membawa catatan: condition: [mahasiswa memilih unduh bukti]; extension point: Bukti pengajuan tersedia (tetap dari Pertemuan 3).

Asumsi penting: asosiasi lama Mahasiswa ke SIA-UC01 dan Admin Akademik ke SIA-UC02 (Pertemuan 2) saya tulis berdasarkan kebutuhan SIA-R01 dan SIA-R02. Cocokkan dengan diagram Pertemuan 2 asli Anda. Jika berbeda, sesuaikan.

## 10. Keterlacakan elemen baru

| Elemen baru | Kebutuhan dasar |
|---|---|
| Aktor Civitas Akademika | SIA-R07 |
| Aktor Dosen | SIA-R07, SIA-R08 |
| Generalization aktor (2 panah) | SIA-R07 |
| SIA-UC07 | SIA-R07 |
| SIA-UC08 | SIA-R08 |
| SIA-UC09 | SIA-R09 |
| SIA-UC10 | SIA-R10 |
| SIA-UC11, UC12, UC13 dan 3 generalization use case | SIA-R11 |
| SIA-CO01 dan realization ke SIA-UC08 | SIA-R12 (dan SIA-R08) |
| SIA-CO02 dan realization ke SIA-UC09 | SIA-R12 (dan SIA-R09) |

## 11. Perbandingan diagram Pertemuan 3 dan Pertemuan 4 (jenis Tabel 4.4)

| Kelompok | Isi |
|---|---|
| Tetap sama | Aktor Mahasiswa, Admin Akademik, dan Dosen Wali; use case jadwal kuliah (SIA-UC01, UC02) dan KRS (SIA-UC03 sampai UC06); relasi «include» SIA-UC03 ke SIA-UC04; relasi «extend» SIA-UC05 ke SIA-UC03 lengkap dengan condition dan extension point; asosiasi Mahasiswa ke SIA-UC01, UC03, UC05; Admin Akademik ke SIA-UC02; Dosen Wali ke SIA-UC06 |
| Berubah karena aturan baru | Tidak ada garis lama yang dipindahkan: asosiasi Mahasiswa pada diagram SIA tetap digambar langsung karena fungsi itu khusus Mahasiswa, bukan fungsi bersama dengan Dosen |
| Ditambah pada Pertemuan 4 | Aktor Civitas Akademika dan Dosen; dua generalization aktor; SIA-UC07 sampai SIA-UC13; tiga generalization use case ke SIA-UC10; collaboration SIA-CO01 dan SIA-CO02 beserta dua realization; asosiasi baru (Civitas ke UC07, Mahasiswa ke UC09, Dosen ke UC08, Admin Akademik ke UC10) |

## 12. Uji konsistensi (Langkah 8)

### Situasi A: Mahasiswa melihat kalender akademik tanpa garis asosiasi langsung dari Mahasiswa
Tetap benar menurut diagram. Mahasiswa adalah bentuk khusus dari Civitas Akademika (panah generalization menuju Civitas Akademika). Civitas Akademika punya asosiasi ke SIA-UC07. Karena aktor khusus mewarisi seluruh asosiasi aktor umum, Mahasiswa dapat melakukan SIA-UC07 tanpa garis sendiri. Hal yang sama berlaku untuk Dosen. Menggambar garis kedua justru menggandakan asosiasi warisan, yang dilarang aturan jobsheet.

### Situasi B: Dosen yang bukan pengampu mencoba menginput nilai
Menurut deskripsi SIA-UC08, prasyaratnya adalah dosen pengampu mata kuliah itu (alur alternatif A2): sistem menolak input, tidak ada nilai yang tersimpan, dan data mata kuliah tidak berubah. Pascakondisi gagal berlaku.

### Situasi C: Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif
Menurut aturan tugas, Hapus Data Mahasiswa hanya untuk mahasiswa tanpa data akademik aktif. Maka sistem menolak penghapusan, menampilkan alasan penolakan, dan data mahasiswa tetap ada. Hal ini dicatat sebagai alur alternatif SIA-UC13 (lihat berkas deskripsi).

## 13. Review dan revisi (isi saat review)

Reviewer: ______________________  Tanggal: ______________

| Pemeriksaan | Hasil |
|---|---|
| Elemen Pertemuan 3 tetap ada dan tidak berubah nama | [ ] |
| Segitiga kosong generalization aktor menempel pada Civitas Akademika | [ ] |
| Tidak ada asosiasi warisan digambar ulang dari Mahasiswa atau Dosen | [ ] |
| Asosiasi khusus Mahasiswa dan Dosen tetap ada | [ ] |
| Tiga panah generalization use case menuju SIA-UC10, segitiga kosong di SIA-UC10 | [ ] |
| Collaboration berupa elips garis putus-putus, nama sama persis dengan use case, tidak terhubung ke aktor | [ ] |
| Realization dari collaboration menuju use case, garis putus-putus segitiga kosong | [ ] |
| Aktor di luar batas sistem; use case dan collaboration di dalam batas | [ ] |
| Nama dan ID sama di diagram, katalog, dan deskripsi | [ ] |
| Sumber dapat dibuka kembali; versi sumber dan ekspor sama | [ ] |
| 18 hubungan pada Bagian 9 semua ada | [ ] |
| Pertanyaan terbuka (Bagian 3) ditandai belum dimodelkan | [ ] |

Catatan revisi (bila ada perubahan isi simpan sebagai v02, pertahankan v01):

| Temuan reviewer | Perbaikan | Versi |
|---|---|---|
| (belum ada) | | |
