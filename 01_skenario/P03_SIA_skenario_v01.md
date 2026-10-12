
Skenario
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

Kebutuhan yang dimodelkan
| ID | Kebutuhan |
|---|---|
| SIA-R03 | Mahasiswa dapat mengajukan KRS |
| SIA-R04 | Sistem memvalidasi KRS sebagai bagian pengajuan |
| SIA-R05 | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
| SIA-R06 | Dosen wali dapat memproses persetujuan atau penolakan KRS |


Aturan dan asumsi yang sudah ditetapkan dalam tugas
1. Pengguna telah terautentikasi (dicatat sebagai prasyarat, bukan use case Login).
2. Data mata kuliah, prasyarat, dan jadwal tersedia.
3. Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
4. Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
5. KRS tersimpan belum berarti disetujui (status awal: Menunggu persetujuan dosen wali).


Asumsi tambahan saya (di luar teks tugas, bisa dikoreksi)
| No | Asumsi | Alasan |
|---|---|---|
| A1 | Validasi menjalankan ketiga pemeriksaan lalu menampilkan semua temuan sekaligus | Mahasiswa dapat memperbaiki dalam satu kali percobaan |
| A2 | Mahasiswa yang gagal validasi boleh memperbaiki pilihan atau membatalkan | Skenario tidak melarang |
| A3 | Dosen wali hanya memproses KRS mahasiswa bimbingannya | Konsekuensi dari peran "dosen wali" |

Keterlacakan
| Kebutuhan | Use case |
|---|---|
| SIA-R03 | SIA-UC01 |
| SIA-R04 | SIA-UC02 |
| SIA-R05 | SIA-UC03 |
| SIA-R06 | SIA-UC04 |
