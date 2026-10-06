# Week 02 Day 03 — SQL Query Fundamentals & Analysis

**Status:** 🟢 Completed  
**Study Time:** 2 jam  
**Review:** 5/5  
**Mini Challenge:** Completed

## Objective

Menggunakan SQL untuk menjawab business question melalui agregasi, filtering, grouping, sorting, dan interpretasi hasil.

## SQL Concepts

- `COUNT()`
- `SUM()`
- `AVG()`
- `MIN()`
- `MAX()`
- `WHERE`
- `GROUP BY`
- `HAVING`
- `ORDER BY`

## Learning Workflow

```text
Business Question
      ↓
Data Preparation
      ↓
Write SQL Query
      ↓
Execute & Get Result
      ↓
Analyze & Find Insight
      ↓
Recommendation
      ↓
Next Action
```

## Dataset

Tabel: `penjualan`

Kolom utama:
- `transaction_id`
- `tanggal`
- `produk`
- `jumlah`
- `total_penjualan`

**Periode latihan utama:** Februari 2026.

> **Catatan penting:** Day 3 menggunakan subset transaksi Februari 2026. Jangan mencampurkan angka subset ini dengan total dataset utama Day 1.

## Mini Challenge

Business Question:

> Manager ingin mengetahui performa penjualan setiap produk selama Februari 2026.

Query menggunakan `COUNT(transaction_id)`, `SUM(jumlah)`, `SUM(total_penjualan)`, filter Februari 2026, `GROUP BY produk`, dan `ORDER BY total_revenue DESC`.

### Hasil Mini Challenge

| Produk | Total Transaksi | Total Unit | Total Revenue |
|---|---:|---:|---:|
| Laptop | 2 | 2 | Rp14.100.000 |
| Monitor | 2 | 2 | Rp5.000.000 |
| Headset | 2 | 5 | Rp1.250.000 |
| Mouse | 2 | 6 | Rp900.000 |
| Keyboard | 2 | 3 | Rp900.000 |

## Business Findings

- Laptop memiliki revenue terbesar: **Rp14.100.000**, dengan 2 transaksi dan 2 unit.
- Mouse memiliki unit terjual terbanyak: **6 unit**, tetapi revenue **Rp900.000**.
- Semua produk memiliki **2 transaksi** pada subset Februari ini.
- Perbedaan revenue perlu dibaca bersama unit dan nilai transaksi.

## Key Insight

**Volume penjualan tinggi tidak selalu berarti revenue tinggi.**

Untuk menjelaskan penyebab perbedaan revenue secara lebih lengkap, masih diperlukan data seperti harga, diskon, promosi, margin, atau karakteristik pelanggan.

## Analytical Standard

Query yang benar belum cukup. Hasil query harus diterjemahkan ke konteks bisnis dan tidak boleh menghasilkan causal claim yang belum didukung data.

## Result

- Exercise 13–20 selesai.
- Review konsep: **5/5 benar**.
- Mini challenge selesai sampai menghasilkan insight.
