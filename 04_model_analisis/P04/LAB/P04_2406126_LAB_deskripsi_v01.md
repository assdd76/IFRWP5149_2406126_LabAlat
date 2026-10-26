# P04_2406126_LAB_deskripsi_v01

Status: LATIHAN USE CASE DIAGRAM LANJUTAN. Nama dan ID sama dengan diagram P04_2406126_LAB_usecase_v01.
Template sama dengan Pertemuan 3, ditambah baris Generalization dan Collaboration. Deskripsi ditulis untuk use case, bukan untuk collaboration.

---

## LAB-UC11: Catat Pengembalian Peralatan

| Elemen | Isi |
|---|---|
| ID dan nama | LAB-UC11: Catat Pengembalian Peralatan |
| Sumber kebutuhan | LAB-R09 dan LAB-R10 |
| Tujuan | Pengembalian tercatat dan status peminjaman serta kondisi peralatan terbarui |
| Aktor utama | Petugas Laboratorium |
| Aktor pendukung | - |
| Pemicu | Petugas memilih fungsi pencatatan pengembalian dan menentukan peminjaman yang akan dikembalikan |
| Prasyarat | Petugas telah terautentikasi; peminjaman terpilih berstatus Dipinjam |
| Pascakondisi berhasil | Pengembalian tercatat dengan tanggal kembali dan kondisi peralatan; status peminjaman menjadi Selesai |
| Pascakondisi gagal | Tidak ada pengembalian baru yang tercatat; status peminjaman tidak berubah |
| Include | LAB-UC12: Periksa Kondisi Peralatan |
| Generalization | Tidak ada (bukan bagian hierarki use case) |
| Collaboration | LAB-CO02: Catat Pengembalian Peralatan |
| Aturan bisnis/asumsi | Pengembalian hanya untuk peminjaman berstatus Dipinjam. Kondisi dicatat sebagai Baik, Rusak Ringan, atau Rusak Berat. Keterlambatan dan denda belum dimodelkan |

**Alur utama**

| Langkah | Tindakan petugas | Respons sistem |
|---|---|---|
| 1 | Memilih peminjaman yang akan dikembalikan | Menampilkan data peminjaman terpilih dan statusnya |
| 2 | Mengonfirmasi alat yang kembali dan jumlahnya | Menampung konfirmasi petugas |
| 3 | Tidak ada | Memeriksa status peminjaman harus Dipinjam |
| 4 | Tidak ada | Menjalankan LAB-UC12: memeriksa dan mencatat kondisi peralatan |
| 5 | Menyimpan pencatatan pengembalian | Menyimpan tanggal kembali dan kondisi; mengubah status peminjaman menjadi Selesai |
| 6 | Melihat konfirmasi | Menampilkan ringkasan pengembalian |

**Alur alternatif / pengecualian**
- **A1: Status bukan Dipinjam (pada langkah 3):** sistem menolak pencatatan dan menampilkan status peminjaman saat ini. Pascakondisi gagal berlaku; tidak ada data yang disimpan.
- **A2: Kondisi Rusak Ringan atau Rusak Berat (pada langkah 4):** sistem tetap menyimpan pencatatan, menandai kondisi tersebut pada data peralatan, dan pengembalian tetap tercatat. Kerusakan tidak otomatis menimbulkan denda pada model ini.
- **A3: Jumlah alat yang kembali tidak sesuai (pada langkah 2):** sistem meminta petugas memeriksa kembali isian sebelum penyimpanan; pencatatan tidak disimpan sampai jumlah sesuai atau dikoreksi.

---

## Tambahan baris pada deskripsi use case Pertemuan 3 yang terlibat hierarki atau collaboration

Baris di bawah ditambahkan pada deskripsi Pertemuan 3 (isi baris lain tidak diubah).

| Use case | Generalization | Collaboration |
|---|---|---|
| LAB-UC02 Kelola Data Peralatan | Use case umum bagi LAB-UC08, LAB-UC09, LAB-UC10 | - |
| LAB-UC03 Ajukan Peminjaman | Tidak ada | LAB-CO01: Ajukan Peminjaman |
| LAB-UC08 Tambah Data Peralatan | Khusus dari LAB-UC02; menghasilkan data peralatan baru | - |
| LAB-UC09 Ubah Data Peralatan | Khusus dari LAB-UC02; menghasilkan data peralatan yang berubah | - |
| LAB-UC10 Hapus Data Peralatan | Khusus dari LAB-UC02; menghasilkan data peralatan yang terhapus (syarat: tidak sedang dipinjam dan tidak memiliki pengajuan aktif) | - |

Aktor pada deskripsi LAB-UC01 dan LAB-UC03 menjadi **Peminjam** (aktor umum; Mahasiswa dan Dosen mewarisinya).
