# Week 02 Day 06 — Mini Data Analysis #2

**Status:** 🟡 Materi siap, belum dikerjakan  
**Planned Study Time:** 2 jam

> Halaman Notion secara eksplisit mencatat Day 6 sebagai **belum dikerjakan**. Dokumentasi ini menyimpan case yang sudah disiapkan tanpa mengklaim analysis sebagai hasil pengerjaan.

## Objective

Melakukan mini data analysis menggunakan dataset yang lebih kompleks dengan alur:

**Business Problem → Business Question → Data → Analysis → Insight → Recommendation**

## Case

Sebuah toko online mengalami penurunan revenue pada April.

| Metric | Maret | April |
|---|---:|---:|
| Visitors | 20.000 | 24.000 |
| Product Views | 15.000 | 18.000 |
| Add to Cart | 6.000 | 5.400 |
| Transactions | 4.000 | 3.200 |
| Revenue | Rp400.000.000 | Rp288.000.000 |
| AOV | Rp100.000 | Rp90.000 |
| Retention Rate | 70% | 55% |

## Analysis Tasks

### 1. Business Questions

- Mengapa Visitors dan Product Views meningkat tetapi Add to Cart dan Transactions menurun?
- Apa yang menyebabkan Retention Rate dan AOV turun bersamaan?

### 2. KPI Analysis

Target perhitungan:
- Revenue change
- Transaction change
- AOV change
- Retention change

### 3. Funnel Analysis

Prioritas:

**Product Views → Add to Cart**

Maret:

`6.000 ÷ 15.000 = 40%`

April:

`5.400 ÷ 18.000 = 30%`

Penurunan conversion rate: **10 percentage points**.

### 4. Insight Framework

**Fakta:** Visitors dan Product Views naik, tetapi Add to Cart turun.

**Hipotesis:** kualitas traffic, product detail page, harga, stok, UX, atau kendala teknis mungkin berkontribusi.

Hipotesis tersebut **belum dapat dianggap sebagai penyebab pasti** tanpa data tambahan.

### 5. Recommendation Framework

- Audit Product Detail Page & Marketing Channel.
- Evaluasi harga, informasi produk, stok, UX, dan kualitas traffic.
- Lakukan win-back pelanggan lama.
- Uji bundling/minimum purchase threshold untuk meningkatkan AOV.

## Learning Standard

Jangan hanya melihat revenue. Breakdown revenue menjadi **Transactions + AOV**, lalu gunakan funnel dan retention untuk mencari area yang perlu diperiksa.

**Next:** kerjakan analysis secara bertahap dan dokumentasikan hasil perhitungan serta insight setelah pengerjaan selesai.
