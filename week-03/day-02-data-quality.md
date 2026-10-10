# Week 3 — Day 2
## Anatomi Dataset Lanjutan (Data Quality Awal)

**Status:** PASS  
**Score:** 92/100  
**Rubrik:** Anatomi 14/15 · Identifikasi masalah 27/30 · Treatment/validasi 23/25 · Dampak bisnis 14/15 · Aturan validasi 14/15

> **Source note:** The original Notion lesson page was blank when inspected. The lesson, synthetic dataset, and exercise were temporarily created by the mentor based on the Learning Tracker title. This is not presented as pre-existing official Notion material. Notion remains the source of truth.

## Dataset used
Synthetic practice data (not real transactions), 7 rows × 7 columns.

| Order_ID | Tanggal | Customer | Kota | Jumlah | Harga_Satuan | Total_Penjualan |
|---|---|---|---|---:|---:|---:|
| ORD001 | 2026-04-01 | Ani | Jakarta | 2 | 50000 | 100000 |
| ORD002 | 2026-04-02 | Budi | JAKARTA | 1 | 75000 | 75000 |
| ORD003 | 2026-04-03 | Citra | *(missing)* | 3 | 40000 | 120000 |
| ORD004 | 2026-04-04 | Dedi | Bandung | -2 | 30000 | -60000 |
| ORD005 | 2026-04-05 | Eka | Surabaya | 2 | 25000 | 100000 |
| ORD006 | 2026-04-06 | Fani | Depok | 1 | 60000 | 60000 |
| ORD006 | 2026-04-06 | Fani | Depok | 1 | 60000 | 60000 |

## Findings
1. **Inconsistent formatting:** ORD001 has `Jakarta`, ORD002 has `JAKARTA`. Normalize only after confirming they represent the same city.
2. **Missing value:** ORD003 has no city. Check source records or a legitimate relational table; do not guess.
3. **Potential invalid value / domain exception:** ORD004 has `Jumlah = -2`. Its total matches multiplication, but negative quantity needs business context (e.g. return/refund conventions) before classifying as error.
4. **Calculation mismatch:** ORD005 quantity × unit price = 2 × Rp25,000 = Rp50,000, but listed total is Rp100,000. Trace source fields and formula before choosing which value to correct.
5. **Potential exact duplicate:** ORD006 appears twice identically. Verify timestamp, payment, inventory, ingestion logs, and business key rules before deleting a record.

## Treatment and validation approach
- Missing city: cross-check the source of truth and related records; if not recoverable, preserve as unknown/missing and document impact.
- Duplicate: compare all fields and verify the transaction against operational evidence before deduplication.
- Invalid/domain values: use documented business rules and boundary checks; account for returns and cancellations.
- Inconsistent formatting: profile unique values and normalize against an approved master list.
- Calculation mismatch: isolate affected rows, recompute, inspect source components and identify the authoritative source before changing values.

## Business impact
- Missing city prevents accurate allocation of ORD003's Rp120,000 to a geographic group. It does not necessarily reduce national revenue if the row is still included in the overall sum.
- City formatting differences can split Jakarta into separate groups and distort rankings or regional decisions.
- ORD005 may overstate Surabaya revenue by Rp50,000 if quantity and unit price are authoritative; confirm before correcting.

## Three validation rules
1. **Uniqueness:** Order_ID should be unique if the business rule defines one record per order. Check whether the dataset is order-level or order-line-level before enforcing it.
2. **Calculated field:** `Total_Penjualan = Jumlah * Harga_Satuan`, subject to documented discounts, taxes, returns, or other adjustments if applicable.
3. **Domain and completeness:** quantity must follow documented transaction rules; a positive-only rule needs a return/refund exception. City completeness should be enforced if required by the business process, otherwise unknown values should be flagged.

## Review feedback
**Score: 92/100 — PASS** (target ≥80).

Strengths: strong validation-first approach, thoughtful investigation of ORD006 through timestamps/payment/inventory, clear business impacts, and useful validation rules.

Corrections to remember:
- Name at least two variables when asked for examples.
- Negative quantity is not automatically an error; it depends on transaction semantics.
- A missing city can break geographic attribution without necessarily changing national revenue totals.
- A repeated ID is a duplicate candidate, not proof by itself.

## Gate
Day 2 is completed with PASS 92/100. Next tracker item: **Week 3 Day 3 — Struktur Folder Awal Repo Portfolio di GitHub**.
