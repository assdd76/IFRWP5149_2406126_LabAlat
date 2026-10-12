SIA-UC01 — Ajukan KRS
| Bagian | Isi |
|---|---|
| ID dan nama | SIA-UC01 — Ajukan KRS |
| Sumber kebutuhan | SIA-R03 |
| Tujuan | Menghasilkan pengajuan KRS yang tersimpan dan menunggu persetujuan dosen wali |
| Aktor utama | Mahasiswa |
| Aktor pendukung | — |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS |
| Prasyarat | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia |
| Include | SIA-UC02 — Validasi KRS (dipanggil pada langkah 4) |
| Extension point | Bukti pengajuan tersedia, pada langkah 6 |
| Extend | SIA-UC03 jika [mahasiswa memilih unduh] |
| Pascakondisi berhasil | Pengajuan tersimpan dengan nomor dan status Menunggu persetujuan dosen wali |
| Pascakondisi gagal | Tidak ada pengajuan baru yang berhasil tersimpan |
| Aturan bisnis/asumsi | Validasi gagal = tidak tersimpan; unduh bukti bukan syarat keberhasilan; tersimpan ≠ disetujui |

Alur utama**
| Langkah | Tindakan mahasiswa | Respons sistem |
|---|---|---|
| 1 | Membuka pengajuan KRS | Menampilkan formulir dan daftar mata kuliah |
| 2 | Memilih mata kuliah | Menampung pilihan |
| 3 | Mengirim pengajuan | Menerima pengajuan |
| 4 | — | Menjalankan SIA-UC02 (hasil: valid) |
| 5 | — | Jika valid, menyimpan pengajuan, memberi nomor, status Menunggu persetujuan dosen wali |
| 6 | Melihat konfirmasi | Menampilkan nomor dan status; mencapai extension point Bukti pengajuan tersedia |
| 7 | Mengakhiri pengajuan | Menutup proses pengajuan |

Alur alternatif/pengecualian
| Rujukan | Kondisi | Respons dan hasil akhir |
|---|---|---|
| 4a | Validasi tidak valid | Sistem menampilkan alasan (data tidak lengkap, prasyarat tidak terpenuhi, atau benturan jadwal). Pengajuan tidak disimpan. Mahasiswa kembali ke langkah 2 untuk memperbaiki atau membatalkan. Jika membatalkan: pascakondisi gagal. |
| 2a | Mahasiswa membatalkan sebelum mengirim | Tidak ada data disimpan; pascakondisi gagal |
| 6a | Mahasiswa memilih unduh bukti | Menjalankan SIA-UC03, lalu kembali ke langkah 7. Status pengajuan tidak berubah. |

---

SIA-UC02 — Validasi KRS
| Bagian | Isi |
|---|---|
| ID dan nama | SIA-UC02 — Validasi KRS |
| Sumber kebutuhan | SIA-R04 |
| Tujuan | Memastikan pilihan mata kuliah lengkap, memenuhi prasyarat, dan tidak berbenturan jadwal |
| Aktor utama | Tidak ada aktor langsung; dijalankan sistem atas permintaan SIA-UC01 (mahasiswa memulainya lewat UC01) |
| Aktor pendukung | — |
| Pemicu | SIA-UC01 mencapai langkah 4 (memanggil validasi) |
| Prasyarat | Pilihan mata kuliah sudah diterima dari UC01; data mata kuliah, prasyarat, dan jadwal tersedia |
| Pascakondisi berhasil | Hasil "valid" dikembalikan ke UC01. Belum ada penyimpanan; penyimpanan dilakukan UC01 |
| Pascakondisi gagal | Hasil "tidak valid" beserta alasan dikembalikan ke UC01; data tidak berubah |
| Aturan bisnis/asumsi | Validasi mencakup tiga pemeriksaan; semua temuan ditampilkan sekaligus (asumsi A1) |

Alur utama
| Langkah | Respons sistem |
|---|---|
| 1 | Menerima pilihan mata kuliah dari SIA-UC01 |
| 2 | Memeriksa kelengkapan (ada mata kuliah dipilih, data wajib terisi) |
| 3 | Memeriksa prasyarat setiap mata kuliah yang dipilih |
| 4 | Memeriksa benturan jadwal antar mata kuliah yang dipilih |
| 5 | Menetapkan hasil "valid" bila ketiganya lolos, lalu mengembalikannya ke UC01 |

Alur alternatif/pengecualian
| Rujukan | Kondisi | Respons dan hasil akhir |
|---|---|---|
| 2a | Data tidak lengkap | Mencatat temuan "tidak lengkap", lanjut ke langkah 3 |
| 3a | Prasyarat belum terpenuhi | Mencatat mata kuliah yang bermasalah, lanjut ke langkah 4 |
| 4a | Terdapat benturan jadwal | Mencatat pasangan mata kuliah yang berbenturan, lanjut ke langkah 5 |
| 5a | Ada minimal satu temuan (2a/3a/4a) | Menetapkan hasil "tidak valid", mengembalikan semua alasan ke UC01 (UC01 lanjut ke 4a) |

---

SIA-UC03 — Unduh bukti pengajuan KRS
| Bagian | Isi |
|---|---|
| ID dan nama | SIA-UC03 — Unduh bukti pengajuan KRS |
| Sumber kebutuhan | SIA-R05 |
| Tujuan | Mahasiswa memperoleh bukti pengajuan KRS yang dapat disimpan |
| Aktor utama | Mahasiswa |
| Aktor pendukung | — |
| Pemicu | Pada konfirmasi pengajuan, mahasiswa memilih mengunduh bukti |
| Prasyarat | Mahasiswa terautentikasi; SIA-UC01 mencapai extension point Bukti pengajuan tersedia (pengajuan sudah tersimpan dan bernomor) |
| Extend terhadap | SIA-UC01 pada extension point Bukti pengajuan tersedia, kondisi [mahasiswa memilih unduh] |
| Pascakondisi berhasil | Bukti pengajuan diterima mahasiswa; pengajuan dan statusnya tidak berubah |
| Pascakondisi gagal | Bukti tidak terunduh; pengajuan tetap tersimpan dan berstatus sama |
| Aturan bisnis/asumsi | Unduh bukti bukan syarat keberhasilan pengajuan |

Alur utama
| Langkah | Tindakan mahasiswa | Respons sistem |
|---|---|---|
| 1 | Memilih unduh bukti pengajuan | Menerima pilihan |
| 2 | — | Menyiapkan bukti (nomor, status, daftar mata kuliah, waktu pengajuan) |
| 3 | — | Menyediakan berkas untuk diunduh |
| 4 | Menerima berkas | Kembali ke SIA-UC01 langkah 7 |

Alur alternatif/pengecualian
| Rujukan | Kondisi | Respons dan hasil akhir |
|---|---|---|
| 2a | Bukti gagal disiapkan | Menampilkan pesan kegagalan; pascakondisi gagal; pengajuan tetap tersimpan |

---

SIA-UC04 — Proses keputusan KRS
| Bagian | Isi |
|---|---|
| ID dan nama | SIA-UC04 — Proses keputusan KRS |
| Sumber kebutuhan | SIA-R06 |
| Tujuan | Menetapkan KRS mahasiswa menjadi Disetujui atau Ditolak beserta catatan keputusan |
| Aktor utama | Dosen wali |
| Aktor pendukung | — |
| Pemicu | Dosen wali memilih fungsi proses keputusan KRS |
| Prasyarat | Dosen wali terautentikasi; ada pengajuan mahasiswa bimbingannya berstatus Menunggu persetujuan dosen wali |
| Pascakondisi berhasil | Status pengajuan menjadi Disetujui atau Ditolak, dengan catatan keputusan tersimpan |
| Pascakondisi gagal | Status pengajuan tetap Menunggu persetujuan dosen wali |
| Aturan bisnis/asumsi | KRS tersimpan belum berarti disetujui; persetujuan dan penolakan adalah dua hasil dari satu tujuan, bukan dua use case |

Alur utama (persetujuan)
| Langkah | Tindakan dosen wali | Respons sistem |
|---|---|---|
| 1 | Membuka fungsi proses keputusan | Menampilkan daftar pengajuan berstatus menunggu |
| 2 | Memilih satu pengajuan | Menampilkan rincian KRS |
| 3 | Memilih keputusan Setuju | Menampung keputusan |
| 4 | Mengisi catatan keputusan | Menampung catatan |
| 5 | Mengonfirmasi keputusan | Menyimpan keputusan, mengubah status menjadi Disetujui |
| 6 | Melihat konfirmasi | Menampilkan status akhir dan catatan |

Alur alternatif/pengecualian
| Rujukan | Kondisi | Respons dan hasil akhir |
|---|---|---|
| 3a | Dosen wali memilih Tolak | Lanjut ke langkah 4; pada langkah 5 status menjadi Ditolak, catatan tersimpan. Pascakondisi berhasil (tujuan "menetapkan keputusan" tercapai) |
| 2a | Tidak ada pengajuan menunggu | Menampilkan informasi daftar kosong; pascakondisi gagal |
| 5a | Dosen wali membatalkan sebelum konfirmasi | Tidak ada perubahan; status tetap Menunggu persetujuan; pascakondisi gagal |
