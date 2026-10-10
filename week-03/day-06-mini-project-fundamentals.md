# Week 03 Day 06 — Mini Project Fundamental (End-to-End Sederhana)

**Hasil review: PASS — 91/100** (target kelulusan ≥80/100).

> **Catatan sumber:** Halaman materi Day 6 di Notion sebelumnya kosong saat diperiksa. Materi dan dataset kedai kopi ini adalah latihan sementara dari mentor; dataset bersifat sintetis dan bukan data perusahaan nyata.

## Rubrik Penilaian

| Komponen | Skor |
|---|---:|
| Problem definition & business questions | 14/15 |
| Data quality & cleaning rules | 22/25 |
| Ketepatan perhitungan pada dataset Day 6 | 24/25 |
| Insight vs. hypothesis | 18/20 |
| Rekomendasi & ringkasan manajer | 13/15 |
| **Total** | **91/100** |

## Hal yang Dikerjakan dengan Baik

- Mengembalikan analisis ke dataset yang benar, T001–T013, setelah percobaan pertama memakai metrik dari latihan lain.
- Menghitung Net Sales per baris dengan rumus `jumlah × harga_satuan × (1 − diskon_pct)`.
- Menghitung ringkasan Januari dan Februari serta penjualan per kategori secara konsisten pada skenario sementara yang dipilih.
- Mengidentifikasi channel kosong pada T009, kandidat duplikat T011, kuantitas negatif T012, dan diskon 1.20 pada T013.
- Memisahkan temuan deskriptif dari hipotesis, lalu mengusulkan validasi POS, audit alasan retur/stok, dan aturan validasi diskon.
- Secara eksplisit memilih untuk tidak menetapkan koreksi T013 tanpa bukti, serta mengusulkan pelaporan skenario untuk data yang belum terverifikasi.

## Hasil Perhitungan — Skenario Sementara

Asumsi kerja untuk tabel ini: satu baris T011 dikeluarkan **jika** duplikasi terkonfirmasi; T012 diperlakukan sebagai retur **jika** didukung bukti; T013 diasumsikan 20% hanya untuk skenario sementara; channel T009 diberi label `Unassigned`.

| Metrik | Januari | Februari (sementara) |
|---|---:|---:|
| Total Net Sales | Rp1.669.800 | Rp1.172.400 |
| Unit bersih | 102 | 80 |
| Transaksi penjualan yang dihitung | 6 | 6 |
| AOV | Rp278.300 | Rp195.400 |
| Perubahan Net Sales | — | -29,79% |
| Perubahan unit bersih | — | -21,57% |

| Kategori | Januari | Februari (sementara) | Perubahan |
|---|---:|---:|---:|
| Minuman | Rp1.221.000 | Rp1.066.800 | -12,63% |
| Makanan | Rp448.800 | Rp105.600 | -76,47% |
| **Total** | **Rp1.669.800** | **Rp1.172.400** | **-29,79%** |

Angka Februari di atas bukan angka final terverifikasi. Dua isu utama dapat mengubah hasil:
- Jika T013 memakai nilai asli 1.20 secara aritmetika, Net Sales baris itu menjadi -Rp36.000 dan total Februari menjadi Rp992.400. Nilai ini adalah skenario sensitivitas, bukan nilai penjualan yang boleh dianggap valid tanpa pemeriksaan sumber.
- Jika T012 tidak dimasukkan sebagai retur sebelum ada bukti, total Februari pada skenario T013 = 20% menjadi Rp1.216.400 dan unit menjadi 82, sebelum penyesuaian lain yang terverifikasi.

## Koreksi & Batasan Penting

1. **T013 — diskon 1.20:** jangan otomatis mengubahnya menjadi 0.20. Simpan nilai asli, tandai `Needs Verification`, periksa log POS/master promo, dan tampilkan skenario koreksi terpisah jika berguna. Hasil Rp144.000 hanya berlaku pada skenario asumsi diskon 20%.
2. **T012 — jumlah -2:** perlakukan sebagai retur hanya setelah nota/log mendukung. Sampai saat itu, laporkan angka sebelum dan sesudah penyesuaian dengan catatan bahwa hasil masih provisional.
3. **T011 — kandidat duplikat:** baris identik bukan bukti final double-entry. Konfirmasi melalui timestamp dan bukti transaksi sebelum menghapus satu baris.
4. **T009 — channel kosong:** `Unassigned` adalah label analitis, bukan nilai channel asli. Transaksi dapat tetap masuk ke total penjualan jika nilai penjualannya valid.
5. **Kategori Makanan turun 76,47%** dalam skenario sementara, tetapi penyebab seperti kualitas pastry, stok kosong, atau minat pelanggan yang turun belum terbukti. Kuantitas negatif T012 turut memengaruhi hasil sementara.
6. **Efektivitas diskon belum dapat disimpulkan.** Perlu perbandingan transaksi dengan/tanpa diskon, mempertimbangkan produk, unit, periode, dan konteks promo. Dataset kecil ini mendukung eksplorasi awal, bukan klaim kausal.

## Insight, Hipotesis, dan Rekomendasi

### Insight deskriptif
- Dalam skenario sementara, Net Sales Februari turun 29,79% walaupun transaksi penjualan yang dihitung sama-sama enam. AOV turun dari Rp278.300 menjadi Rp195.400.
- Kategori Makanan menunjukkan penurunan persentase terbesar (-76,47%), sedangkan Minuman turun 12,63% pada skenario yang sama.

### Hipotesis yang belum terbukti
- Penurunan Pastry mungkin berkaitan dengan kualitas produk, ketersediaan stok, atau perubahan permintaan.
- Diskon Februari mungkin belum meningkatkan unit per transaksi atau justru menekan pendapatan per unit; perlu analisis lebih lanjut untuk mengujinya.

### Rekomendasi
1. Verifikasi log POS/master promo T013, bukti retur T012, dan timestamp/bukti transaksi T011 sebelum menetapkan angka final.
2. Audit stok dan alasan retur Pastry; untuk menguji promosi, bandingkan unit per transaksi, Net Sales per transaksi, dan hasil per produk pada transaksi diskon vs. non-diskon. Catat bahwa data biaya dibutuhkan jika keputusan harus berbasis profit/margin.

## Ringkasan Manajer

Pada skenario sementara, Net Sales Februari tercatat Rp1.172.400, turun 29,79% dari Januari, sementara jumlah transaksi penjualan yang dihitung tetap enam. AOV turun dari Rp278.300 menjadi Rp195.400. Kategori Makanan menunjukkan penurunan persentase terbesar, tetapi penyebab operasionalnya belum diketahui. Angka Februari bergantung pada verifikasi diskon T013, status retur T012, dan kandidat duplikat T011. Langkah berikutnya adalah memeriksa bukti POS/retur dan stok, lalu memperbarui ringkasan sebelum keputusan bisnis dibuat.

## Status

- **Week 3 Day 6: Completed — PASS 91/100.**
- Materi dan dataset sintetis sementara mentor karena halaman materi awal Notion kosong.
- **Next step:** Week 3 Day 7 — Ujian Fundamental Gabungan.
