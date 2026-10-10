# Week 03 Day 05 — Business Questions → Rencana Analisis

**Hasil review: PASS — 91/100** (target kelulusan ≥80/100).

> **Catatan sumber:** Halaman materi Day 5 di Notion sebelumnya kosong saat diperiksa. Materi dan dataset kedai kopi adalah materi sementara mentor; data kasus bersifat sintetis, bukan data perusahaan nyata.

## Rubrik Penilaian

| Komponen | Skor |
|---|---:|
| Kualitas dan keterukuran business questions | 23/25 |
| Kesesuaian KPI dan data yang dibutuhkan | 23/25 |
| Urutan metode analisis | 18/20 |
| Data gap dan pemisahan fakta vs. hipotesis | 19/20 |
| Prioritas dan kejelasan komunikasi | 8/10 |
| **Total** | **91/100** |

## Hal yang Dikerjakan dengan Baik

- Menyusun empat business questions yang mengarah ke kanal marketing, performa menu/diskon, segmentasi pelanggan, dan perbandingan antar-cabang.
- Memetakan tiga pertanyaan ke KPI, sumber data, langkah analisis, output, dan keputusan yang dapat didukung.
- Mengusulkan data tambahan yang relevan: POS item-level, atribusi kanal marketing, CRM/riwayat pelanggan, dan log stok habis.
- Memisahkan hipotesis dari fakta dan memilih investigasi yang dapat dilakukan sebelum membuat rekomendasi final.
- Perhitungan perubahan utama benar: revenue turun 15%; transaksi turun 10%; visitors naik 8%; belanja marketing naik 25%; AOV turun sekitar 5,56%; jumlah pelanggan yang kembali pada tabel turun 21,25%.

## Koreksi Penting

1. **Jangan menganggap penyebab AOV turun sudah diketahui.** Data menunjukkan AOV turun dari Rp20.000 ke sekitar Rp18.889. Diskon agresif atau perubahan product mix merupakan hipotesis. Gunakan frasa “apakah perubahan diskon/harga/product mix berkaitan dengan penurunan AOV?” sebelum ada bukti yang mendukung hubungan sebab-akibat.
2. **Definisi CAC harus konsisten.** Marketing spend dibagi jumlah transaksi adalah marketing cost per transaction, bukan CAC. CAC membutuhkan jumlah pelanggan baru yang diperoleh dan atribusi kanal yang jelas.
3. **ROAS memerlukan atribusi revenue ke iklan.** Revenue agregat kedai dibagi belanja marketing agregat tidak membuktikan paid-media ROAS. Definisi spend dan periode atribusi juga harus konsisten.
4. **Retention rate tidak dapat dihitung hanya dari dua angka pelanggan kembali.** Perlu definisi cohort, pelanggan yang memenuhi syarat untuk kembali, identitas pelanggan, dan periode observasi. Perbedaan 2.400 ke 1.890 adalah penurunan jumlah yang tercatat sebesar 510 (21,25%), tetapi tidak membuktikan bahwa tepat 510 orang yang sama berhenti kembali.
5. **Data POS yang siap tersedia belum terverifikasi.** POS line-item log memang berguna, tetapi ketersediaan, kelengkapan kolom, dan kualitasnya perlu dikonfirmasi terlebih dahulu.
6. **Hindari menyebut item-level analysis sebagai intervensi langsung pada penyebab.** Analisis menu/diskon adalah cara menguji beberapa penjelasan yang mungkin, bukan bukti bahwa menu atau diskon adalah akar masalah.
7. **Conversion pengunjung ke transaksi dapat diturunkan secara awal dari tabel:** Januari 6.000/10.000 = 60%; Februari 5.400/10.800 = 50%. Ini turun 10 percentage points (atau sekitar 16,67% secara relatif), jika definisi pengunjung dan transaksi konsisten serta periode pencatatannya sebanding.
8. **Istilah “margin diskon” perlu diperjelas.** Ukur discount rate/discount amount sebagai proporsi penjualan sebelum diskon jika data mendukung. Untuk menghitung margin kontribusi/profit, diperlukan data biaya produk dan biaya terkait.
9. **Peningkatan spend dan visitors bersamaan dengan penurunan transaksi adalah pola, bukan bukti bahwa marketing menyebabkan transaksi turun.** Periksa channel mix, atribusi, kualitas trafik, operasional, stok, dan faktor lain sebelum menyimpulkan penyebab.

## Kesimpulan

Jawaban sudah memenuhi gate. Langkah awal yang masuk akal adalah membuat baseline KPI, memvalidasi definisi dan kualitas data, lalu memecah performa menurut menu, kanal, dan pelanggan. Prioritas menu/diskon bisa diterima sebagai pilihan investigasi, tetapi belum terbukti lebih penting daripada kanal, retensi, atau operasional sampai dampak dan kelengkapan data dibandingkan.

## Status

- **Day 5: Completed — PASS 91/100.**
- Materi dan dataset sintetis sementara mentor karena halaman materi awal Notion kosong.
- **Next step:** Week 3 Day 6 — Mini Project Fundamental (End-to-End Sederhana).
