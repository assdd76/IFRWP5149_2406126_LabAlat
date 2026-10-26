

## A. Diagram acuan (kumulatif Pertemuan 4)

Diagram memuat 5 aktor, 12 use case, 2 collaboration, dan 17 hubungan. Rincian disusun dari relasi yang disebut pada jobsheet; cocokkan dengan berkas .drawio Anda.

| No. | Jenis relasi | Hubungan |
|---|---|---|
| 1-7 | Asosiasi (7) | Peminjam–UC01; Peminjam–UC03; Mahasiswa–UC05 (asosiasi khusus); Petugas Laboratorium–UC02; Petugas Laboratorium–UC06; Petugas Laboratorium–UC11; Kepala Laboratorium–UC07 |
| 8-9 | Generalization aktor (2) | Mahasiswa → Peminjam; Dosen → Peminjam |
| 10-11 | Include (2) | UC03 → UC04; UC11 → UC12 |
| 12 | Extend (1) | UC05 → UC03 (condition [mahasiswa memilih cetak], extension point Bukti pengajuan tersedia) |
| 13-15 | Generalization use case (3) | UC08 → UC02; UC09 → UC02; UC10 → UC02 |
| 16-17 | Realization (2) | UC03 – LAB-CO01; UC11 – LAB-CO02 |

## B. Lembar telaah per tabel (kolom penelusuran)

| No. | Tabel yang ditelaah | Relasi yang ditelusur | Hasil pencocokan terhadap diagram |
|---|---|---|---|
| 1 | Tabel 5.3 LAB-UC01 Lihat Ketersediaan Peralatan | Asosiasi Peminjam–UC01; generalization aktor Mahasiswa dan Dosen → Peminjam | Cocok. Aktor "Peminjam (berlaku untuk Mahasiswa dan Dosen)" sama dengan diagram, ditulis satu kali tanpa tabel ganda. Tidak ada include, extend, atau realization pada UC01 dan tidak ada langkah yang menyiratkannya. |
| 2 | Tabel 5.1 LAB-UC03 Ajukan Peminjaman | Asosiasi Peminjam–UC03; include UC03 → UC04 (langkah 2); extend UC05 → UC03 (langkah 11–12); realization UC03–LAB-CO01 (keterangan) | Cocok. Include menjadi langkah rujukan 2 pada Skenario Normal; extend ada di Skenario Alternative lengkap dengan condition dan extension point; CO01 disebut di keterangan tanpa langkah. Catatan: lihat temuan T-01. |
| 3 | Tabel 5.4 LAB-UC04 Periksa Ketersediaan | Include UC03 → UC04 (UC04 sebagai use case yang disertakan); tidak ada asosiasi aktor langsung | Cocok. ID dan nama sama dengan diagram; Aktor ditulis Peminjam dengan keterangan berjalan di dalam UC03, sesuai deskripsi bahwa tidak ada interaksi langsung. Catatan: lihat temuan T-02. |
| 4 | Tabel 5.5 LAB-UC05 Cetak Bukti Pengajuan | Extend UC05 → UC03; asosiasi khusus Mahasiswa–UC05 | Cocok. Aktor Mahasiswa sama dengan diagram; condition [mahasiswa memilih cetak] dan extension point Bukti pengajuan tersedia identik dengan Tabel 5.1. Catatan: lihat temuan T-03. |
| 5 | Tabel 5.6 LAB-UC02 Kelola Data Peralatan | Asosiasi Petugas Laboratorium–UC02; UC02 sebagai use case umum pada generalization UC08/UC09/UC10 → UC02 | Cocok. Memuat perilaku bersama (buka, pilih bentuk pengelolaan, isi, periksa, simpan) dan menyebut UC08–UC10 pada Deskripsi. Catatan: lihat temuan T-04. |
| 6 | Tabel 5.7 LAB-UC08 Tambah Data Peralatan | Generalization UC08 → UC02 | Cocok. Keterangan menyebut use case khusus dari UC02 dan merujuk ke Tabel 5.6; perilaku pembeda: data baru tersimpan. |
| 7 | Tabel 5.8 LAB-UC09 Ubah Data Peralatan | Generalization UC09 → UC02 | Cocok. Perilaku pembeda: data peralatan berubah. Catatan: lihat temuan T-05. |
| 8 | Tabel 5.9 LAB-UC10 Hapus Data Peralatan | Generalization UC10 → UC02 | Cocok. Perilaku pembeda dan syarat (tidak sedang dipinjam, tidak ada pengajuan aktif) tertulis pada langkah 2 dan cabang 5–6 serta keterangan. |
| 9 | Tabel 5.10 LAB-UC06 Proses Keputusan Peminjaman | Asosiasi Petugas Laboratorium–UC06; berdiri sendiri tanpa relasi antar use case | Cocok. Tidak ada langkah include, extend, generalization, atau realization. Catatan: lihat temuan T-06. |
| 10 | Tabel 5.11 LAB-UC07 Lihat Laporan Peminjaman | Asosiasi Kepala Laboratorium–UC07 (satu-satunya use case aktor ini); tanpa relasi lain | Cocok. Berdiri sendiri; tidak memuat langkah include, extend, generalization, atau realization; keterangan menyatakannya. |
| 11 | Tabel 5.12 LAB-UC11 Catat Pengembalian Peralatan | Asosiasi Petugas Laboratorium–UC11; include UC11 → UC12 (langkah 6); realization UC11–LAB-CO02 (keterangan) | Cocok. Include menjadi langkah rujukan 6 tanpa menyalin langkah UC12; CO02 di keterangan tanpa langkah. Catatan: lihat temuan T-07. |
| 12 | Tabel 5.13 LAB-UC12 Periksa Kondisi Peralatan | Include UC11 → UC12 (UC12 sebagai use case yang disertakan); tanpa asosiasi aktor langsung | Cocok. Aktor Petugas Laboratorium dengan keterangan berjalan di dalam UC11. Catatan: lihat temuan T-08. |

## C. Checklist penilaian (bagian C.4)

| No. | Butir checklist | Hasil | Keterangan |
|---|---|---|---|
| 1 | Seluruh field tabel terisi (Nama use case, Aktor, Tujuan, Deskripsi, kolom, Normal, Alternative, Akhir) | ✓ | Terpenuhi pada ke-12 tabel. |
| 2 | Langkah berurutan, satu aksi per langkah, penomoran berlanjut tanpa pengulangan | ✓ dengan catatan | Penomoran berlanjut terpenuhi di semua tabel. Beberapa langkah memuat lebih dari satu aksi atau isian: Tabel 5.1 langkah 3, Tabel 5.6 langkah 5, Tabel 5.10 langkah 3, Tabel 5.12 langkah 3 (T-01, T-04, T-06, T-07). |
| 3 | Kolom Kegiatan hanya aksi aktor; kolom Respon sistem hanya tanggapan sistem | ✓ dengan catatan | Berdasarkan tata letak PDF, ada langkah sistem pada kolom Kegiatan: Tabel 5.4 langkah 3, Tabel 5.12 langkah 5 dan 13; langkah "Alur … memanggil" pada Tabel 5.4 dan 5.13 bukan aksi aktor (T-02, T-07, T-08). |
| 4 | Data masukan dan data tampilan disebut eksplisit (field, nilai, status) | ✓ dengan catatan | Status dan field eksplisit pada UC03, UC05, UC06, UC11, UC12. Masih generik: "data" pada Tabel 5.6 langkah 5 dan Tabel 5.7 langkah 3 (T-04). |
| 5 | Include = langkah rujukan di Skenario Normal (nama, ID, tabel), tanpa menyalin langkah | ✓ | UC03 langkah 2 → UC04; UC11 langkah 6 → UC12. |
| 6 | Extend = cabang bersyarat di Skenario Alternative dengan condition, extension point, dan rujukan tabel | ✓ dengan catatan | UC03 langkah 11–12 → UC05 lengkap. Awal langkah 11 belum memuat frasa "cabang dari langkah N" (T-01). |
| 7 | Generalization aktor: satu tabel atas nama aktor umum; tidak ada tabel ganda | ✓ | UC01 dan UC03 atas nama Peminjam; tidak ada tabel terpisah untuk Mahasiswa/Dosen. |
| 8 | Generalization use case: skenario umum + khusus yang merujuk ke umum | ✓ | UC02 umum; UC08, UC09, UC10 merujuk Tabel 5.6 pada Deskripsi dan Keterangan. |
| 9 | Collaboration disebut di keterangan, tanpa langkah dan tanpa tabel sendiri | ✓ | LAB-CO01 pada UC03; LAB-CO02 pada UC11; tidak ada tabel CO. |
| 10 | Setiap tabel punya Skenario Alternative dan Skenario Akhir | ✓ | Terpenuhi pada ke-12 tabel. |
| 11 | Nama, ID, aktor, condition, extension point sama persis dengan diagram P04 | ✓ | Condition dan extension point identik pada Tabel 5.1 dan 5.5. Pencocokan akhir terhadap berkas .drawio perlu dikonfirmasi pada komputer Anda. |
| 12 | Kepala Laboratorium hanya punya LAB-UC07, tanpa relasi lain | ✓ | Tabel 5.11 berdiri sendiri. |
| 13 | Berkas diagram P04 tidak diubah; dokumen disimpan di 01_skenario dengan nama/versi benar | ✓ | Tidak ada diagram baru; nama berkas P05_<NIM>_LAB_telaah_skenario_v01.docx. |

## D. Temuan dan usulan perbaikan

| ID | Tabel | Temuan | Usulan perbaikan |
|---|---|---|---|
| T-01 | Tabel 5.1 LAB-UC03 | Langkah 11 (extend LAB-UC05) belum diawali frasa "cabang dari langkah N", padahal kaidah B.3.e mewajibkannya untuk setiap cabang. Langkah 3 juga memuat tiga isian dalam satu langkah. | Tambahkan "cabang dari langkah 6" (titik setelah pengajuan tersimpan dan konfirmasi tampil, tempat extension point Bukti pengajuan tersedia). Tiga isian satu formulir dapat dipertahankan sebagai satu aksi isi formulir, sesuai contoh acuan. |
| T-02 | Tabel 5.4 LAB-UC04 | Langkah 1 dan 4 menyebut "Alur pengajuan" (bukan aksi aktor). Langkah 3 "Sistem menyatakan peralatan tersedia" tampak berada di kolom Kegiatan. | Pindahkan langkah 3 ke kolom Respon sistem; atau tulis aksi pemicu dari sisi aktor (Peminjam memilih peralatan) dan jadikan 1–4 respon sistem berurutan. |
| T-03 | Tabel 5.5 LAB-UC05 | Cabang 5 "Mahasiswa tidak memilih cetak (cabang dari langkah 1)" bertentangan dengan Skenario Normal yang dimulai saat mahasiswa sudah memilih cetak; bila condition tidak terpenuhi, UC05 tidak dijalankan. | Pertegas bahwa cabang 5–6 menggambarkan kondisi condition tidak terpenuhi pada konfirmasi UC03, atau ganti dengan cabang pembatalan pada langkah 3. |
| T-04 | Tabel 5.6 LAB-UC02 (dan 5.7) | Langkah 5 "mengisi atau mengonfirmasi data" memuat dua kata kerja dan "data" tidak spesifik. | Pisahkan menurut bentuk (tambah/ubah mengisi; hapus mengonfirmasi) di tabel khusus, dan sebut "data peralatan" beserta field utamanya. |
| T-05 | Tabel 5.8 LAB-UC09 | Langkah 4 memeriksa perubahan data, namun tidak ada cabang untuk data tidak lengkap atau tidak sah seperti pada UC02 (cabang 9–10) dan UC08. | Tambahkan cabang "data tidak sah (cabang dari langkah 4)" atau nyatakan bahwa cabang tersebut mengikuti Tabel 5.6. |
| T-06 | Tabel 5.10 LAB-UC06 | Langkah 3 memuat dua aksi (memilih pengajuan dan menetapkan persetujuan). Cabang 5 "penolakan (cabang dari langkah 4)": keputusan dibuat aktor pada langkah 3. | Pecah langkah 3 menjadi memilih pengajuan, lalu menetapkan keputusan; ubah rujukan cabang penolakan ke langkah keputusan. |
| T-07 | Tabel 5.12 LAB-UC11 | Langkah 3 memuat dua aksi (alat dan jumlah). Langkah 4–6 berturut-turut sistem dan langkah 5 tampak di kolom Kegiatan. Langkah 9 "Petugas melihat konfirmasi" bukan aksi. Langkah 13 adalah peristiwa sistem di kolom Kegiatan. Cabang 15 merujuk langkah 3 padahal pemeriksaan jumlah tidak tertulis pada langkah 4. Skenario Akhir tidak mencakup cabang jumlah tidak sesuai. | Pisahkan langkah 3; satukan pemeriksaan status dan jumlah pada satu langkah Respon sistem; hapus langkah 9 atau ganti dengan "Petugas menyimpan" yang sudah ada; tempatkan kondisi kerusakan pada kolom Respon sistem; tambahkan kondisi jumlah tidak sesuai pada Skenario Akhir. |
| T-08 | Tabel 5.13 LAB-UC12 | Langkah 1 "Alur pengembalian memanggil …" bukan aksi aktor. Cabang 5 merujuk langkah 4, sedangkan kekosongan nilai terjadi saat langkah 3. | Ganti langkah 1 menjadi aksi yang dimulai dari UC11 (rujukan include), dan ubah rujukan cabang ke langkah 3. |
| T-09 | Dokumen jobsheet | Bagian B.6.d merujuk "Tabel 5.0", sedangkan tabel aturan pemetaan diberi judul "Tabel 5". | Catat sebagai salah ketik penomoran; tidak memengaruhi isi skenario. |

## E. Logbook

| Tanggal | Kegiatan | Status |
|---|---|---|
| 26 Okt 2026 | Membaca Jobsheet Pertemuan 5 dan mencocokkan struktur tabel dengan Tabel 5.1 | Selesai |
| 26 Okt 2026 | Menelaah 12 tabel skenario studi kasus LAB (UC01–UC12) terhadap diagram acuan | Selesai |
| 26 Okt 2026 | Pemeriksaan dengan checklist bagian C.4 | Selesai |
