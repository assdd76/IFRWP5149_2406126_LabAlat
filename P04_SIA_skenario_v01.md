# P04_SIA_skenario_v01

Status: LATIHAN USE CASE DIAGRAM LANJUTAN (diagram kumulatif; bukan model lengkap sistem)
Kasus: Sistem Informasi Akademik (SIA) - Layanan Hasil Studi
NIM: 2406126

## 1. Skenario tugas
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

Skenario ini fiktif untuk praktikum dan berbeda dari tugas Pertemuan 2 (jadwal kuliah) dan Pertemuan 3 (pengajuan KRS).

## 2. Aktor dan kedudukannya (Langkah 3: generalization aktor)

| Aktor | Kedudukan | Tujuan terhadap sistem |
|---|---|---|
| Civitas Akademika | Umum (general), baru pada Pertemuan 4 | Peran umum bagi pengguna kalender akademik. Fungsinya diwariskan ke Mahasiswa dan Dosen |
| Mahasiswa | Khusus dari Civitas Akademika | Melihat kalender akademik (diwariskan); tetap memiliki asosiasi langsung sendiri ke Lihat Jadwal Kuliah, Ajukan KRS, Unduh Bukti Pengajuan KRS, dan Lihat KHS |
| Dosen | Khusus dari Civitas Akademika, baru pada Pertemuan 4 | Melihat kalender akademik (diwariskan); menginput nilai mata kuliah yang diampunya |
| Admin Akademik | Tetap dari pertemuan sebelumnya | Mengelola jadwal kuliah dan mengelola data mahasiswa |
| Dosen Wali | Tetap dari Pertemuan 3 | Memproses keputusan KRS |

### Keputusan: Mahasiswa dan Dosen adalah bentuk khusus dari Civitas Akademika
Tiga pertanyaan penentu dari modul:
1. Apakah dua peran atau lebih memakai fungsi sistem yang sama persis? Ya: melihat kalender akademik.
2. Apakah kesamaan itu tetap berlaku selama sistem berkembang, bukan kebetulan satu skenario? Ya: semua anggota civitas akademika memang berhak melihat agenda resmi institusi.
3. Apakah nama peran umum membuat diagram lebih jelas? Ya: garis ke Lihat Kalender Akademik cukup digambar satu kali.

Ketiganya ya, sehingga generalization aktor layak dipakai.

Aturan gambar:
- Dua panah generalization (garis utuh, ujung segitiga kosong): Mahasiswa menuju Civitas Akademika dan Dosen menuju Civitas Akademika. Segitiga kosong menempel pada Civitas Akademika.
- Asosiasi Civitas Akademika ke SIA-UC07 digambar satu kali dari aktor umum. Tidak digambar ulang dari Mahasiswa atau Dosen.
- Asosiasi milik aktor khusus tidak diwariskan dan tidak dihapus: Mahasiswa tetap terhubung langsung ke SIA-UC01, SIA-UC03, SIA-UC05, dan SIA-UC09; Dosen terhubung langsung ke SIA-UC08.
- Dosen Wali tidak dijadikan aktor khusus dari Civitas Akademika. Modul menyebutnya tetap dari pertemuan sebelumnya, dan kebutuhan SIA-R07 hanya menyebut Mahasiswa dan Dosen.
- Admin Akademik tidak dimasukkan ke hierarki karena tidak ada kebutuhan yang menyatakan Admin Akademik melihat kalender akademik.

## 3. Alasan generalization use case (Langkah 4)
SIA-UC11, SIA-UC12, dan SIA-UC13 adalah bentuk khusus dari SIA-UC10 Kelola Data Mahasiswa, karena ketiganya sama-sama mengelola data mahasiswa (perilaku umum) tetapi hasil akhirnya berbeda.

## 4. Alasan collaboration (Langkah 5)
Input Nilai Mata Kuliah dan Lihat KHS adalah dua use case utama pada tugas ini (SIA-R12), sehingga realisasinya ditunjukkan eksplisit. Use case lain tidak diberi collaboration pada pertemuan ini.
