# Week 02 Day 01 — Tools Setup & SQL Basic Analysis

**Status:** 🟢 Completed  
**Study Time:** 2 jam  
**Tools:** MySQL, MySQL Workbench, Excel, Power BI

## Objective

Memulai praktik analisis database menggunakan SQL dan mengubah hasil query menjadi business insight.

## Dataset

Tabel: `penjualan`

Kolom utama:
- `transaction_id`
- `tanggal`
- `customer`
- `kota`
- `produk`
- `kategori`
- `jumlah`
- `harga`
- `total_penjualan`

## SQL Concepts

- `SELECT`
- `SUM()`
- `GROUP BY`
- `ORDER BY`
- `DESC`
- `WHERE`
- Alias dengan `AS`
- Subquery sederhana

## Analysis Results

**Total revenue:** Rp48.800.000

| Produk | Unit | Revenue | Rata-rata/Unit |
|---|---:|---:|---:|
| Mouse | 11 | Rp1.650.000 | Rp150.000 |
| Headset | 7 | Rp1.750.000 | Rp250.000 |
| Keyboard | 6 | Rp1.800.000 | Rp300.000 |
| Laptop | 5 | Rp36.100.000 | Rp7.220.000 |
| Monitor | 3 | Rp7.500.000 | Rp2.500.000 |

Kategori:

| Kategori | Unit | Revenue |
|---|---:|---:|
| Elektronik | 9 | Rp43.600.000 |
| Aksesoris | 24 | Rp5.200.000 |

Laptop menyumbang sekitar **70,37%** total revenue. Kategori Elektronik menyumbang sekitar **89,3%** total revenue.

## Business Insights

1. Mouse memiliki volume unit tertinggi, tetapi Laptop menghasilkan revenue terbesar.
2. Aksesoris terjual lebih banyak unit, tetapi revenue jauh lebih rendah dibanding Elektronik.
3. Revenue perlu dibaca bersama volume dan nilai per unit; unit tinggi tidak otomatis berarti revenue tinggi.

## Analytical Limitation

Data belum cukup untuk menyimpulkan:
- produk paling menguntungkan;
- produk paling diminati;
- strategi prioritas bisnis.

Data tambahan seperti margin, biaya, stok, tren waktu, dan promosi masih diperlukan.

## Reflection

SQL bukan hanya syntax. Nilai SQL muncul ketika query digunakan untuk menjawab **Business Question** dan hasilnya diterjemahkan menjadi insight yang sesuai evidence.
