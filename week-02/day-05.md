# Week 02 Day 05 — Studi Kasus Business Questions Lanjutan

**Documentation Result:** 🟢 Completed  
**Assessment:** **95/100 — LULUS**  
**Study Time:** 2 jam  
**Tracker Note:** property Status di Notion masih tercatat “Not Started”, tetapi isi halaman memuat assessment selesai dan status Completed.

## Objective

Mengubah business problem menjadi business question yang spesifik, terukur, relevan, dan dapat dijawab menggunakan data.

## Analysis Framework

**Business Problem → Business Question → Data yang Dibutuhkan → Metric → Analysis → Insight → Recommendation**

## Example Business Problem

> Revenue toko online turun pada April.

Business questions yang dibangun:
1. Mengapa Visitors/Product Views meningkat tetapi Add to Cart dan Transactions menurun?
2. Apa yang menyebabkan Retention Rate dan AOV turun bersamaan?

## Data Requirements

Untuk membandingkan revenue antarperiode:
- `transaction_date`
- `product_id/product_name`
- `category`
- `quantity`
- `revenue/total_price`

Untuk menjelaskan revenue:
- Total Revenue
- Total Transactions
- Average Order Value (AOV)

## Mini Case

| Metric | Maret | April |
|---|---:|---:|
| Visitors | 20.000 | 24.000 |
| Product Views | 15.000 | 18.000 |
| Add to Cart | 6.000 | 5.400 |
| Transactions | 4.000 | 3.200 |
| Revenue | Rp400 jt | Rp288 jt |
| AOV | Rp100.000 | Rp90.000 |
| Retention | 70% | 55% |

Findings:
- Revenue **-28%**
- Transactions **-20%**
- AOV **-10%**
- Retention **70% → 55%**, turun **15 percentage points**
- Product Views → Add to Cart: **40% → 30%**

## Insight

Traffic meningkat, tetapi conversion pada tahap Product Views → Add to Cart menurun.

Fakta data dipisahkan dari hipotesis:
- **Fakta:** traffic dan product views naik; add-to-cart, transactions, AOV, dan retention turun.
- **Hipotesis:** kualitas traffic, product detail page, UX, harga, stok, atau perubahan perilaku pelanggan.

## Recommendation

1. Audit Product Detail Page & marketing channel.
2. Evaluasi harga, informasi produk, stok, UX, dan kualitas traffic.
3. Jalankan win-back/re-engagement.
4. Uji bundling atau minimum purchase threshold untuk pemulihan AOV.

## Assessment

**95/100 — LULUS**

Kekuatan:
- Business problem terhubung dengan KPI.
- Metric dihitung dengan benar.
- Funnel dibaca dengan tepat.
- Fakta dan hipotesis dibedakan.
- Recommendation terhubung dengan insight.

