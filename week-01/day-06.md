# Day 06 — Mini Data Analysis

> **Dokumentasi Perjalanan — Foundation**  
> Status: ✅ Completed — Lulus  
> Score: **9,5/10**  
> Study Time: **2 jam**

## Tujuan

Menerapkan alur berpikir Data Analyst secara end-to-end:

**Business Question → Data → Analysis → Information → Insight → Business Meaning**

## Business Case

| Bulan | Pengunjung | Transaksi | Revenue |
|---|---:|---:|---:|
| Januari | 10.000 | 1.000 | Rp100 juta |
| Februari | 10.000 | 900 | Rp92 juta |
| Maret | 10.000 | 750 | Rp78 juta |
| April | 10.000 | 600 | Rp65 juta |

## Level 1 — Membaca Data

Transaksi:
`(600 - 1.000) / 1.000 × 100% = -40%`

➡️ Transaksi turun **40%**.

Revenue:
`(65 - 100) / 100 × 100% = -35%`

➡️ Revenue turun **35%**.

## Level 2 — Information

Fakta yang terlihat:
1. Pengunjung tetap 10.000/bulan.
2. Transaksi menurun setiap bulan.
3. Revenue menurun setiap bulan.

Information menjawab **“Apa yang terjadi?”**

## Level 3 — Insight

### Insight 1
Pengunjung tetap 10.000, tetapi transaksi turun 1.000 → 600.

**Makna:** performa konversi pengunjung menjadi transaksi menurun.

### Insight 2
Revenue turun 35% bersamaan dengan transaksi turun 40%.

**Makna:** penurunan performa terlihat pada volume transaksi dan revenue.

### Insight 3
Dataset belum memiliki variabel yang cukup untuk menentukan penyebab pasti.

**Makna:** analisis lanjutan diperlukan sebelum menentukan tindakan.

## Mini Challenge — Conversion Rate

**Conversion Rate = Transaksi / Pengunjung × 100%**

- Januari: 1.000 / 10.000 = **10%**
- April: 600 / 10.000 = **6%**

Penurunan absolut = **4 percentage points**.  
Penurunan relatif = **40%**.

> Jangan menyebut 10% → 6% sebagai “turun 4%”. Yang tepat adalah **turun 4 percentage points**, atau **40% secara relatif**.

## So What?

Jumlah pengunjung tidak berubah, tetapi proporsi pengunjung yang melakukan transaksi menurun. Karena itu, analisis berikutnya perlu melihat proses setelah pengunjung datang hingga melakukan transaksi.

Hipotesis yang dapat diuji:
- perubahan harga;
- perubahan produk;
- perubahan promosi;
- perbedaan conversion berdasarkan produk/kategori;
- perubahan perilaku customer.

Semua poin tersebut adalah **hipotesis**, bukan penyebab yang sudah terbukti.

## Analytical Discipline

| Level | Contoh |
|---|---|
| Observation | Transaksi turun 40% |
| Insight | Conversion rate ikut turun |
| Causal Claim | “Promo berhenti menyebabkan penurunan” |

Level ketiga membutuhkan evidence tambahan.

## Assessment

- Level 1: **10/10**
- Level 2: **10/10**
- Level 3: **9,5/10**
- Mini Challenge: **9,5/10**
- Final: **9,5/10**

## Skills

- Quantitative Analysis
- Insight Generation
- Business Thinking
- Analytical Rigor
