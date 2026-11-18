# Sistem Monitoring Stok dan Penjualan Kantin Kampus

## 1. Identitas

| Keterangan | Isi |
|---|---|
| Nama Lengkap | Ai Nurasiah |
| NIM | C2583207035 |
| Kelas | PTI3B |
| Mata Kuliah | Algoritma dan Pemrograman Lanjutan |
| Dosen Pengampu | Taofik Muhammad, M.Kom |
| Nama Proyek | Sistem Monitoring Stok dan Penjualan Kantin Kampus |

## 2. Deskripsi Singkat

Sistem Monitoring Stok dan Penjualan Kantin Kampus adalah program berbasis bahasa C yang digunakan untuk mengelola data produk, memantau persediaan barang, melakukan transaksi penjualan, dan menampilkan laporan penjualan. Data produk disimpan menggunakan array selama program berjalan.

## 3. Daftar Fitur

1. Melihat daftar produk, harga, dan stok.
2. Menambahkan produk baru.
3. Mengubah data produk.
4. Melakukan transaksi penjualan beberapa produk.
5. Menambahkan stok produk.
6. Mencari produk berdasarkan nama.
7. Mengurutkan produk berdasarkan harga termurah atau jumlah terjual terbanyak.
8. Menampilkan laporan penjualan.
9. Mengecek produk dengan stok kurang dari 5.
0. Keluar dari program.

## 4. Penjelasan Penggunaan Array

Array digunakan untuk menyimpan data setiap produk. Setiap data produk mempunyai indeks yang saling berhubungan. Artinya, nama, harga, stok, dan jumlah terjual pada indeks yang sama merupakan data dari produk yang sama.

| Array/Variabel | Fungsi |
|---|---|
| `[NAMA_ARRAY_NAMA]` | Menyimpan nama produk. |
| `[NAMA_ARRAY_HARGA]` | Menyimpan harga produk. |
| `[NAMA_ARRAY_STOK]` | Menyimpan jumlah stok produk. |
| `[NAMA_ARRAY_TERJUAL]` | Menyimpan jumlah produk yang sudah terjual. |
| `[VARIABEL_JUMLAH_PRODUK]` | Menyimpan jumlah produk yang tercatat. |

**Catatan:** Ganti nama dalam tanda kurung siku sesuai nama variabel yang benar-benar digunakan di file `main.c`.

Pada saat produk baru ditambahkan, data produk disimpan pada indeks yang tersedia. Ketika transaksi berhasil, stok produk berkurang dan jumlah terjual bertambah. Proses pencarian dan pengurutan juga dilakukan terhadap data yang tersimpan di dalam array.

## 5. Cara Kompilasi dan Menjalankan Program

### Menggunakan Code::Blocks

1. Buka proyek atau file `main.c` di Code::Blocks.
2. Pastikan compiler GCC sudah terpasang dan terdeteksi.
3. Klik **Build and Run** atau tekan **F9**.
4. Jendela console akan muncul dan menampilkan menu program.
5. Masukkan angka menu sesuai fitur yang ingin digunakan.

### Menggunakan terminal Windows (GCC)

Pastikan terminal berada di folder tempat file `main.c` disimpan, lalu jalankan:

```bash
gcc main.c -o kantin.exe
```

Jika kompilasi berhasil, jalankan program dengan perintah:

```bash
kantin.exe
```

## 6. Pengujian Program

Screenshot disimpan di folder `screenshots`. Jalur gambar di bawah menggunakan alamat relatif agar gambar dapat tampil ketika README.md dibuka di GitHub, selama struktur folder tidak diubah.

### Skenario 1: Tambah Produk

**Langkah pengujian:**
1. Jalankan program.
2. Pilih menu `2. Tambah Produk`.
3. Masukkan nama produk `Seblak`, harga `15000`, dan stok awal `20`.
4. Pastikan program menampilkan pesan bahwa produk berhasil ditambahkan.
5. Pilih menu `1. Lihat Daftar Produk` untuk memastikan produk muncul.

**Hasil pengujian:** Produk Seblak berhasil ditambahkan dengan harga 15000 dan stok 20.

<img width="1366" height="768" alt="WhatsApp Image 2026-11-16 at 19 30 57" src="https://github.com/user-attachments/assets/5fd4ccf5-0d6e-4f94-b5c4-774f993a1ceb" />


### Skenario 2: Transaksi Penjualan

**Langkah pengujian:**
1. Pilih menu `4. Transaksi Penjualan`.
2. Pilih produk nomor `3` (Es Teh Manis), lalu masukkan jumlah beli `1`.
3. Pilih produk nomor `4` (Gorengan), lalu masukkan jumlah beli `1`.
4. Masukkan `0` untuk mengakhiri pemilihan produk.
5. Periksa rincian transaksi dan konfirmasi transaksi dengan memasukkan `y`.

**Hasil pengujian:** Es Teh Manis 1 × 4000 = 4000 dan Gorengan 1 × 2000 = 2000. Total pembayaran adalah 6000.

<img width="1366" height="768" alt="WhatsApp Image 2026-11-16 at 19 32 37" src="https://github.com/user-attachments/assets/0027c688-dc61-448d-960b-13913e9e4340" />


### Skenario 3: Pembaruan Stok

**Langkah pengujian:**
1. Sebelum transaksi, pilih menu `1. Lihat Daftar Produk` dan screenshot daftar stok.
2. Lakukan transaksi seperti pada Skenario 2.
3. Setelah transaksi berhasil, pilih menu `1` kembali.
4. Screenshot daftar stok setelah transaksi.
5. Bandingkan stok sebelum dan sesudah transaksi.

**Hasil pengujian berdasarkan transaksi Skenario 2:** Stok Es Teh Manis berkurang dari 30 menjadi 29 dan stok Gorengan berkurang dari 40 menjadi 39.

**Screenshot yang perlu dilengkapi:** Ambil dua gambar terpisah dan simpan dengan nama berikut.

<img width="1366" height="768" alt="WhatsApp Image 2026-11-16 at 19 33 17" src="https://github.com/user-attachments/assets/66dbba43-3c17-4abd-bc67-4b6f6c7e6d13" />




### Skenario 4: Stok Tidak Cukup

**Langkah pengujian:**
1. Pastikan stok Air Mineral adalah `4`.
2. Pilih menu `4. Transaksi Penjualan`.
3. Pilih produk nomor `5` (Air Mineral).
4. Masukkan jumlah beli `5`, melebihi stok yang tersedia.
5. Periksa pesan penolakan transaksi.

**Hasil pengujian:** Program menolak pembelian karena stok Air Mineral hanya 4. Transaksi tidak dilanjutkan.

<img width="1366" height="768" alt="4" src="https://github.com/user-attachments/assets/c761ff5c-0c9f-44da-aa9a-5d41b7177dc6" />


**Screenshot tambahan yang perlu dilengkapi:** Setelah transaksi ditolak, pilih menu `1` dan screenshot daftar produk untuk membuktikan stok Air Mineral tetap 4.



### Skenario 5: Laporan Penjualan

**Langkah pengujian:**
1. Pastikan transaksi pada Skenario 2 sudah berhasil.
2. Pilih menu `8. Laporan Penjualan`.
3. Periksa jumlah terjual, pendapatan setiap produk, total unit, dan produk terlaris.

**Hasil pengujian:** Total unit terjual adalah 2 dan total pendapatan adalah 6000. Es Teh Manis dan Gorengan masing-masing terjual 1 unit.

<img width="1366" height="768" alt="5" src="https://github.com/user-attachments/assets/27ac68f4-78eb-4d2b-92e4-db52f79ffeae" />


### Skenario 6: Pengurutan Produk

**Langkah pengujian berdasarkan harga:**
1. Pilih menu `7. Urutkan Produk`.
2. Pilih pilihan `1. Harga termurah`.
3. Periksa apakah produk tersusun dari harga paling murah hingga paling mahal.

<img width="1366" height="768" alt="6" src="https://github.com/user-attachments/assets/d0489f30-3f68-4c65-ab21-9fc9d8b019b5" />


**Langkah pengujian berdasarkan jumlah terjual:**
1. Pilih menu `7. Urutkan Produk` kembali.
2. Pilih pilihan `2. Jumlah terjual terbanyak`.
3. Periksa apakah produk dengan jumlah terjual terbanyak berada di urutan atas.

**Hasil pengujian:** Pengurutan harga dimulai dari Gorengan (2000) hingga Seblak (15000). Berdasarkan jumlah terjual, Es Teh Manis dan Gorengan berada di urutan teratas karena masing-masing terjual 1 unit.



### Skenario 7: Pencarian Produk dan Stok Menipis

**Langkah pengujian pencarian:**
1. Pilih menu `6. Cari Produk`.
2. Masukkan nama produk `Es Teh Manis`.
3. Periksa apakah produk ditemukan dan informasinya ditampilkan.

**Langkah pengujian stok menipis:**
1. Pilih menu `9. Cek Stok Menipis`.
2. Periksa daftar produk yang memiliki stok kurang dari 5.

**Hasil pengujian:** Produk Es Teh Manis berhasil ditemukan. Program juga menampilkan peringatan bahwa stok Air Mineral tersisa 4.

<img width="1366" height="768" alt="7" src="https://github.com/user-attachments/assets/8e17d27f-9efa-4ca6-aa3b-b1ff971d6ab8" />


## 7. Struktur Folder Proyek

```text
Proyek_Array_C_C2583207035/
├── main.c
├── README.md
└── screenshots/
    ├── 01-tambah-produk.png
    ├── 02-transaksi.png
    ├── 03a-stok-sebelum.png
    ├── 03b-stok-sesudah.png
    ├── 04a-stok-tidak-cukup.png
    ├── 04b-stok-tetap.png
    ├── 05-laporan.png
    ├── 06a-urut-harga.png
    ├── 06b-urut-terjual.png
    └── 07-pencarian-dan-stok-menipis.png
```

## 8. Penutup

Program ini dibuat sebagai penerapan materi algoritma dan pemrograman menggunakan bahasa C, khususnya penggunaan array untuk menyimpan dan mengolah data produk. Melalui program ini, pengelolaan stok dan transaksi penjualan kantin dapat dilakukan secara lebih terstruktur.
