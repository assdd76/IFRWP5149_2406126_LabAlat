 Uji konsistensi tiga situasi (tugas SIA)
| Situasi | Diagram | Deskripsi | Konsisten? |
|---|---|---|---|
| **A. Mahasiswa melihat kalender akademik tanpa garis langsung dari Mahasiswa** | Mahasiswa menuju Civitas Akademika (generalization). Civitas Akademika punya asosiasi ke SIA-UC07 | Aktor khusus mewarisi asosiasi aktor umum, jadi Mahasiswa dapat menjalankan SIA-UC07 | Ya. Garis kedua dari Mahasiswa justru menggandakan asosiasi warisan |
| **B. Dosen bukan pengampu menginput nilai** | Dosen terhubung ke SIA-UC08 | Prasyarat SIA-UC08: dosen pengampu. Alur alternatif A2: input ditolak, tidak ada nilai tersimpan | Ya. Pascakondisi gagal berlaku |
| **C. Admin Akademik menghapus data mahasiswa dengan data akademik aktif** | Admin Akademik terhubung ke SIA-UC10; SIA-UC13 khusus dari SIA-UC10 | Aturan tugas: hanya mahasiswa tanpa data akademik aktif. SIA-UC13 alur A1: penghapusan ditolak, data tetap | Ya |


Keterlacakan elemen baru
| Elemen | Kebutuhan | Di diagram | Di deskripsi |
|---|---|---|---|
| Civitas Akademika, Dosen, SIA-UC07 | SIA-R07 | Ya | Ya (katalog) |
| SIA-UC08 | SIA-R08 | Ya | Ya |
| SIA-UC09 | SIA-R09 | Ya | Ya |
| SIA-UC10 | SIA-R10 | Ya | Ya (katalog) |
| SIA-UC11, UC12, UC13 | SIA-R11 | Ya | Ya (UC13 ringkas) |
| SIA-CO01, SIA-CO02 | SIA-R12 | Ya | Ya |
| Peminjam, Dosen | LAB-R07 | Ya | Ya |
| LAB-UC08, UC09, UC10 | LAB-R08 | Ya | Ya |
| LAB-UC11 | LAB-R09 | Ya | Ya |
| LAB-UC12 | LAB-R10 | Ya | Ya |
| LAB-CO01, LAB-CO02 | LAB-R11 | Ya | Ya |


Catatan penyelarasan
| No | Catatan |
|---|---|
| 1 | ID KRS pada berkas P03 SIA (SIA-UC01 s.d. SIA-UC04) berbeda dengan ID gabungan jobsheet P04 (SIA-UC03 s.d. SIA-UC06). Berkas P03 tidak ditimpa; pemetaannya ada di P04_SIA_kebutuhan_v01.md Bagian 4 |
| 2 | Asosiasi lama Mahasiswa ke SIA-UC01 dan Admin Akademik ke SIA-UC02 (Pertemuan 2) perlu dicocokkan dengan diagram P02 asli |


Log review rekan/asisten (isi setelah review nyata)
| No | Temuan (arah panah / nama collaboration / pascakondisi) | Perbaikan | Versi |
|---|---|---|---|
| 1 | | | v02 |
| 2 | | | v02 |
