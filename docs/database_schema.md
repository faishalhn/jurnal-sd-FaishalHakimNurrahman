# Database Schema AVOLICIUS

## Tabel Users

Menyimpan data pengguna sistem, baik pelanggan maupun admin.

Kolom:

- id (Primary Key)
- nama
- email
- password
- role
- created_at

## Tabel Produk

Menyimpan informasi produk makanan dan minuman berbasis alpukat.

Kolom:

- id (Primary Key)
- nama_produk
- deskripsi
- harga
- stok
- gambar
- created_at

## Tabel Pesanan

Menyimpan data transaksi pemesanan yang dilakukan pelanggan.

Kolom:

- id (Primary Key)
- user_id (Foreign Key ke Users)
- tanggal_pesanan
- total_harga
- status_pesanan

## Tabel Detail_Pesanan

Menyimpan rincian produk yang dipesan pada setiap transaksi.

Kolom:

- id (Primary Key)
- pesanan_id (Foreign Key ke Pesanan)
- produk_id (Foreign Key ke Produk)
- jumlah
- harga_satuan
- subtotal

## Tabel Laporan_Penjualan

Menyimpan ringkasan data penjualan untuk kebutuhan pelaporan.

Kolom:

- id (Primary Key)
- tanggal
- total_transaksi
- total_pendapatan
