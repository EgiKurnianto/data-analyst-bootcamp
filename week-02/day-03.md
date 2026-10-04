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

Mini analysis menggunakan data penjualan dengan **20 transaksi**, **25 unit**, dan total revenue **Rp48.800.000**.

Contoh query yang dipraktikkan:

```sql
SELECT produk, SUM(total_penjualan) AS total_revenue
FROM penjualan
GROUP BY produk
ORDER BY total_revenue DESC;
```

## Business Findings

- Laptop menghasilkan revenue terbesar: **Rp14.100.000** pada mini challenge Februari 2026.
- Mouse memiliki volume unit tinggi, tetapi revenue tidak otomatis menjadi yang terbesar.
- Kategori Elektronik menjadi kontributor revenue terbesar pada dataset latihan.

## Key Insight

**Volume penjualan tinggi tidak selalu berarti revenue tinggi.**

Nilai transaksi per unit harus dipertimbangkan ketika membaca performa produk.

## Analytical Standard

Query yang benar belum cukup. Hasil query harus diterjemahkan ke konteks bisnis dan tidak boleh menghasilkan causal claim yang belum didukung data.

## Result

- Exercise 13–20 selesai.
- Review konsep: **5/5 benar**.
- Mini challenge selesai sampai menghasilkan insight.
