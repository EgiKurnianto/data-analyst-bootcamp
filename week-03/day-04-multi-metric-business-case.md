# Week 03 Day 04 — Studi Kasus Bisnis Kompleks (Multi-Metric)

**Hasil review: PASS — 91/100** (target kelulusan ≥80/100).

> **Catatan sumber:** Halaman materi Day 4 di Notion sebelumnya kosong saat diperiksa. Materi dan dataset latihan disusun sementara oleh mentor berdasarkan judul tracker. Dataset bersifat sintetis, bukan data perusahaan nyata.

## Rubrik Penilaian

| Komponen | Skor |
|---|---:|
| Perhitungan dan konsistensi rumus | 29/30 |
| Information dan insight | 21/25 |
| Pemisahan hypothesis dari fakta | 18/20 |
| Prioritas dan rencana investigasi | 14/15 |
| Ringkasan untuk manajer | 9/10 |
| **Total** | **91/100** |

## Review Jawaban

### Hal yang dikerjakan dengan baik
- Menghitung perubahan KPI Januari–Februari dengan benar: Visitors +20%, Product Views +20%, Add to Cart -10%, Transactions -20%, Revenue -28%, Marketing Spend +40%.
- Menghitung funnel dengan benar: Visitors → Product Views 75% pada kedua bulan; Product Views → Add to Cart 40% → 30%; Add to Cart → Transactions sekitar 66,67% → 59,26%; overall conversion 20% → 13,33%; AOV Rp100.000 → Rp90.000.
- Mengidentifikasi Product Views → Add to Cart sebagai tahap pertama yang menunjukkan penurunan rasio.
- Mengusulkan pemeriksaan performa channel, riwayat harga/ongkir, stok, error teknis, dan pengujian A/B.
- Menyebutkan ketidakpastian dan data tambahan yang diperlukan, alih-alih menyatakan penyebab sebagai fakta.

## Koreksi Penting

1. **Biaya pemasaran per transaksi bukan otomatis CAC.** Marketing Spend / Transactions menghasilkan Rp12.500 pada Januari dan Rp21.875 pada Februari, naik 75%. Sebut sebagai *marketing cost per transaction* sampai jumlah pelanggan baru dan definisi CAC tersedia.
2. **Revenue / Marketing Spend bukan otomatis paid-media ROAS.** Angka 8,00x dan sekitar 4,11x adalah *revenue-to-marketing-spend ratio* berdasarkan angka agregat. Untuk paid-media ROAS diperlukan atribusi revenue ke iklan dan definisi spend yang konsisten.
3. **Low buying intent dan masalah halaman produk tetap hypothesis.** Data agregat menunjukkan di mana rasio funnel turun, bukan penyebabnya. Validasi dengan breakdown channel, perangkat, produk, stok, harga, ongkir, dan error log.
4. **Penurunan Add to Cart bersamaan dengan penurunan AOV tidak membuktikan product mix atau daya tarik produk berubah.** Periksa product mix, harga, diskon, margin, dan data per produk.
5. **Target eksperimen bukan jaminan.** Add to Cart Rate 40%, overall conversion ≥20%, dan revenue-to-marketing-spend ratio >6x adalah target usulan yang perlu divalidasi dengan baseline, margin, atribusi, dan desain eksperimen.

## Kesimpulan Bisnis

Pada Februari, traffic meningkat tetapi Add to Cart, transactions, revenue, dan AOV menurun; Product Views → Add to Cart turun dari 40% menjadi 30%. Tahap ini adalah prioritas investigasi yang masuk akal, namun akar penyebab belum dapat dipastikan dari data agregat. Langkah berikutnya adalah menganalisis funnel menurut sumber traffic, perangkat, produk, harga, stok, dan gangguan teknis sebelum menguji perubahan halaman produk.

## Status

- **Day 4: Completed — PASS 91/100.**
- Materi dan dataset latihan sementara mentor karena halaman materi awal Notion kosong.
- **Next step:** Week 3 Day 5 — Business Questions → Rencana Analisis.
