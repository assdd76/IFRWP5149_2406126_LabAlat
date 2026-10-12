 Uji konsistensi tiga situasi
| Situasi | Diagram | Deskripsi | Konsisten? |
|---|---|---|---|
| **a. Validasi berhasil, tidak mengunduh bukti** | UC01 menjalankan UC02 (include). Kondisi extend tidak terpenuhi, UC03 tidak berjalan | UC01 langkah 1-7 tanpa 6a. Pengajuan tersimpan, status Menunggu persetujuan dosen wali | Ya. Pengajuan berhasil tanpa perilaku tambahan |
| **b. Validasi gagal** | UC02 tetap berjalan (include tidak opsional). Extension point tidak tercapai, UC03 tidak mungkin berjalan | UC01 langkah 4a: alasan ditampilkan, tidak disimpan. UC02 alur 5a: hasil tidak valid. Pascakondisi gagal | Ya. Tidak ada pengajuan tersimpan dan bukti tidak tersedia |
| **c. Validasi berhasil, mahasiswa mengunduh bukti** | UC03 memperluas UC01 pada Bukti pengajuan tersedia dengan kondisi [mahasiswa memilih unduh] | UC01 langkah 6a lalu UC03 alur utama, kembali ke langkah 7. Status tidak berubah | Ya. Kondisi dan extension point sama di diagram dan deskripsi |


Keterlacakan kebutuhan
| Kebutuhan | Use case | Di diagram | Di deskripsi |
|---|---|---|---|
| SIA-R03 | SIA-UC01 | Ya | Ya |
| SIA-R04 | SIA-UC02 | Ya (include) | Ya |
| SIA-R05 | SIA-UC03 | Ya (extend) | Ya |
| SIA-R06 | SIA-UC04 | Ya | Ya |


Log review rekan/asisten (isi setelah review nyata)
| No | Temuan (arah panah / kondisi / extension point / pascakondisi) | Perbaikan | Versi |
|---|---|---|---|
| 1 | | | v02 |
| 2 | | | v02 |
