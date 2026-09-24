# Day 04 — Data Quality & Missing Values

> **Learning Portfolio — Foundation**  
> Status: ✅ Completed — Lulus  
> Score: **9,5/10**  
> Study Time: **2 jam**

## Portfolio Summary

Analisis yang baik membutuhkan data yang layak dipercaya. Hari ini fokus pada menemukan masalah kualitas data dan menentukan tindakan yang tepat tanpa cleaning secara sembarangan.

## Data Quality Framework

| Masalah | Contoh | Tindakan awal |
|---|---|---|
| Missing | Usia kosong | Cek sumber & konteks |
| Duplicate | ID tercatat dua kali | Verifikasi sebelum menghapus |
| Invalid | Usia = -5 | Validasi terhadap aturan/sumber |
| Inconsistent | Jakarta / JAKARTA | Normalisasi jika maknanya sama |

## Business Case

Temuan pada dataset transaksi:
- **Missing:** Jumlah kosong.
- **Invalid:** Jumlah = -2.
- **Inconsistent:** JAKARTA vs Jakarta.
- **Duplicate:** ID 004 muncul dua kali.

### Treatment Logic

- Missing → periksa sumber data dan tentukan metode penanganan.
- Invalid → validasi nilai sebenarnya; jangan menebak.
- Inconsistent → normalisasi jika konteks menunjukkan makna yang sama.
- Duplicate → hapus hanya setelah dipastikan merupakan duplikasi.

> **Prinsip:** jangan menebak nilai missing/invalid dan jangan menghapus record sebelum alasan perubahan tervalidasi.

## Analytical Insight

Data cleaning bukan sekadar membuat tabel terlihat rapi. Tujuannya meningkatkan kelayakan data agar analisis berikutnya dapat dipercaya.

## Skills Demonstrated

- Data Quality Assessment
- Data Cleaning Logic
- Validation Thinking
- Anomaly Identification
- Data Integrity Awareness

## Assessment

- Level 1: **8,5/10**
- Level 2: **10/10**
- Level 3: **10/10**
- Final: **9,5/10**

## Learning Checkpoint

> Data yang bersih belum tentu menghasilkan analisis yang berguna jika pertanyaan bisnisnya salah.
