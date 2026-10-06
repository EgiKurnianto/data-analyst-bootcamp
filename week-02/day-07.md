# Week 02 Day 07 — Ujian Mini Week 2

**Status:** 🏆 Completed — LULUS  
**Final Assessment:** **98,1/100**  
**Study Time:** **2 jam**

## Tujuan

Menguji kemampuan Week 2 Day 1–6 dalam SQL, KPI & funnel analysis, business questions, insight, dan recommendation.

## Bagian A — SQL Fundamentals

- Filter Laptop dengan WHERE: **10/10**
- Total revenue per produk dengan SUM + GROUP BY + ORDER BY: **10/10**
- Revenue Februari > Rp2.000.000 dengan WHERE + GROUP BY + HAVING: **10/10**
- Analisis Laptop vs Mouse: **10/10**

**Subtotal: 40/40**

Temuan: Laptop menghasilkan revenue Rp14.100.000 pada Februari, sedangkan Mouse Rp900.000. Keduanya memiliki 2 transaksi, sehingga perbedaan revenue tidak cukup dijelaskan oleh jumlah transaksi saja.

## Bagian B — KPI & Funnel Analysis

### Perubahan KPI

| KPI | Maret | April | Perubahan |
|---|---:|---:|---:|
| Visitors | 20.000 | 24.000 | +20% |
| Product Views | 15.000 | 18.000 | +20% |
| Add to Cart | 6.000 | 5.400 | -10% |
| Transactions | 4.000 | 3.200 | -20% |
| Revenue | Rp400 juta | Rp288 juta | -28% |

**Nilai: 10/10**

### Conversion Funnel

| Tahap | Maret | April | Perubahan |
|---|---:|---:|---:|
| Visitors → Product Views | 75% | 75% | 0 pp |
| Product Views → Add to Cart | 40% | 30% | -10 pp |
| Add to Cart → Transactions | 66,67% | 59,26% | -7,41 pp |

Titik penurunan terbesar: **Product Views → Add to Cart**, turun 10 percentage points.

**Nilai: 10/10**

**Subtotal: 20/20**

## Bagian C — Business Question & Insight

### Insight utama

1. Visitors dan Product Views naik 20%, tetapi Add to Cart turun 10%.
2. Conversion Product Views → Add to Cart turun 40% → 30%.
3. Revenue turun 28%, sejalan dengan Transactions turun 20% dan AOV turun Rp100.000 → Rp90.000.
4. Retention turun 70% → 55%.

### Fakta vs Hipotesis

**Fakta:** traffic naik, Product Views naik, conversion PDP → ATC turun, transactions turun, revenue turun, AOV turun, retention turun.

**Hipotesis:** kualitas traffic berubah, UX/PDP bermasalah, harga atau informasi produk berubah, atau program retensi kurang efektif.

Prioritas investigasi: **Traffic Source** dan **Product Detail Page**.

> Retention tidak disebut sebagai root cause tanpa customer-level evidence.

**Nilai: 9/10**

## Bagian D — Recommendation

### 1. Product Views → Add to Cart
Audit UX/UI PDP, harga, review, informasi produk, stok, CTA, serta targeting/sumber traffic.

### 2. Transactions & AOV
Uji product bundling dan free-shipping threshold; validasi threshold dengan margin dan data transaksi.

### 3. Retention
Jalankan win-back campaign untuk pelanggan yang belum repeat order, dengan segmentasi berbasis perilaku aktual.

**Nilai: 9,5/10**

## Hasil Akhir

| Bagian | Nilai |
|---|---:|
| SQL Fundamentals | 40/40 |
| KPI & Funnel Analysis | 20/20 |
| Business Question & Insight | 9/10 |
| Recommendation | 9,5/10 |
| **Total** | **78,5/80** |
| **Final Assessment** | **98,1/100** |

## Kompetensi yang Diuji

- SQL fundamentals: SELECT, WHERE, GROUP BY, HAVING, ORDER BY, SUM, COUNT, AVG, MIN, MAX.
- KPI dan funnel analysis.
- Conversion Rate, Retention Rate, AOV, Revenue, Transactions.
- Menemukan funnel drop-off.
- Membedakan fakta dan hipotesis.
- Menyusun business insight.
- Membuat recommendation berbasis data.
- Menentukan prioritas investigasi.

## Key Lesson

**Data menunjukkan apa yang terjadi; analisis lanjutan diperlukan untuk membuktikan mengapa hal tersebut terjadi.**

**Week 2 selesai — LULUS 98,1/100.**

Next: **Week 3 — Data Cleaning & Data Validation di Spreadsheet.**
