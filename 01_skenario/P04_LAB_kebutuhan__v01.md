# Kebutuhan Studi Kasus Laboratorium (Pertemuan 4)

## Skenario
Selain mahasiswa, dosen juga meminjam peralatan laboratorium untuk kegiatan praktikum dan penelitian. Mahasiswa dan dosen sama-sama dapat melihat ketersediaan peralatan dan mengajukan peminjaman. Petugas laboratorium mengelola data peralatan: menambah peralatan baru, mengubah data peralatan, dan menghapus data peralatan yang tidak lagi dipakai. Setelah peminjaman disetujui dan alat diambil, petugas mencatat pengembalian peralatan. Pada saat mencatat pengembalian, petugas memeriksa dan mencatat kondisi peralatan. Dua use case utama pada potongan model ini, Ajukan Peminjaman dan Catat Pengembalian Peralatan, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

Seluruh fungsi Pertemuan 3 tetap berlaku dan tetap digambar: pemeriksaan ketersediaan di dalam pengajuan, pencetakan bukti pengajuan oleh mahasiswa, proses keputusan peminjaman oleh petugas, dan laporan peminjaman untuk kepala laboratorium. Diagram Pertemuan 4 adalah diagram Pertemuan 3 yang ditambah, bukan diagram baru yang menggantikannya.

## Daftar Kebutuhan
| ID | Kebutuhan |
|---|---|
| LAB-R01 s.d. LAB-R06 | Kebutuhan Pertemuan 3 tetap berlaku dan tidak berubah arti (lihat Jobsheet Pertemuan 3). |
| LAB-R07 | Mahasiswa dan Dosen, sebagai Peminjam, dapat melihat ketersediaan peralatan dan mengajukan peminjaman. |
| LAB-R08 | Petugas laboratorium mengelola data peralatan dalam tiga bentuk khusus: tambah, ubah, dan hapus data peralatan. |
| LAB-R09 | Petugas laboratorium dapat mencatat pengembalian peralatan untuk peminjaman yang berstatus Dipinjam. |
| LAB-R10 | Sistem memeriksa dan mencatat kondisi peralatan sebagai bagian dari pencatatan pengembalian. |
| LAB-R11 | Model menunjukkan collaboration yang merealisasikan Ajukan Peminjaman dan Catat Pengembalian Peralatan. |

## Batas Sistem dan Aturan
- Sistem mencatat dan menyediakan informasi; perpindahan fisik alat tidak terjadi di dalam perangkat lunak (tetap dari Pertemuan 3).
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran (tetap dari Pertemuan 3).
- Pengembalian hanya dapat dicatat untuk peminjaman berstatus Dipinjam. Peminjaman yang masih Menunggu Keputusan atau Ditolak tidak dapat dicatat pengembaliannya.
- Kondisi peralatan pada pengembalian dicatat dengan salah satu nilai: Baik, Rusak Ringan, atau Rusak Berat.
- Hapus Data Peralatan hanya untuk peralatan yang tidak sedang dipinjam dan tidak memiliki pengajuan aktif.

## Pertanyaan Terbuka
- Bagaimana aturan pencatatan dan penanganan apabila terjadi keterlambatan pengembalian alat? 
- Apakah ada sistem denda untuk keterlambatan atau kerusakan alat, dan bagaimana perhitungannya? (Keterlambatan dan denda belum dimodelkan pada pertemuan ini).