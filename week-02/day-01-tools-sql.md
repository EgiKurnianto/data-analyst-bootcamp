# 📔 Week 2 — Day 1: Tools Setup & SQL Basic Analysis

**Status:** 🟢 Completed  
**Focus:** Foundation Tools & SQL Practice

## 🎯 Learning Objective

Pada Day 1 Week 2 saya belajar:

- menggunakan MySQL dan MySQL Workbench sebagai lingkungan kerja SQL;
- membaca tabel penjualan menggunakan `SELECT`;
- menghitung total dengan `SUM()`;
- mengelompokkan data dengan `GROUP BY`;
- mengurutkan hasil dengan `ORDER BY` dan `DESC`;
- memfilter data menggunakan `WHERE`;
- menggunakan alias dengan `AS`;
- membuat subquery sederhana;
- menghitung kontribusi revenue;
- membandingkan volume unit terjual dengan revenue;
- mengubah hasil query menjadi business insight.

## 🛠️ Tools & Dataset

**Tools:**
- MySQL
- MySQL Workbench
- Microsoft Excel
- Power BI

**Tabel:** `penjualan`

**Kolom utama:**
`transaction_id`, `tanggal`, `customer`, `kota`, `produk`, `kategori`, `jumlah`, `harga`, `total_penjualan`

## 🧪 Latihan SQL yang Diselesaikan

### 1. Total Revenue

```sql
SELECT SUM(total_penjualan)
FROM penjualan;
```

**Hasil:** Rp48.800.000

### 2. Total Unit Berdasarkan Produk

```sql
SELECT
    produk,
    SUM(jumlah) AS total_jumlah
FROM penjualan
GROUP BY produk;
```

**Hasil:**

| Produk | Total Unit |
|---|---:|
| Mouse | 11 |
| Headset | 7 |
| Keyboard | 6 |
| Laptop | 5 |
| Monitor | 3 |

### 3. Revenue Berdasarkan Produk

```sql
SELECT
    produk,
    SUM(total_penjualan) AS total_revenue
FROM penjualan
GROUP BY produk
ORDER BY total_revenue DESC;
```

**Produk dengan revenue terbesar:** Laptop = Rp36.100.000

### 4. Revenue Berdasarkan Kategori

```sql
SELECT
    kategori,
    SUM(total_penjualan) AS total_revenue
FROM penjualan
GROUP BY kategori
ORDER BY total_revenue DESC;
```

**Hasil:**

| Kategori | Total Revenue |
|---|---:|
| Elektronik | Rp43.600.000 |
| Aksesoris | Rp5.200.000 |

### 5. Unit Berdasarkan Kategori

```sql
SELECT
    kategori,
    SUM(jumlah) AS total_jumlah
FROM penjualan
GROUP BY kategori
ORDER BY total_jumlah DESC;
```

**Hasil:**

| Kategori | Total Unit |
|---|---:|
| Aksesoris | 24 |
| Elektronik | 9 |

### 6. Membandingkan Unit dan Revenue

| Kategori | Total Unit | Total Revenue |
|---|---:|---:|
| Elektronik | 9 | Rp43.600.000 |
| Aksesoris | 24 | Rp5.200.000 |

### 7. Kontribusi Revenue Laptop

Dengan menggunakan subquery, revenue Laptop dibandingkan dengan seluruh revenue.

**Hasil:** Laptop menyumbang sekitar **70,37%** dari total revenue.

### 8. Rata-rata Nilai Penjualan per Unit

Perhitungan:

`SUM(total_penjualan) / SUM(jumlah)`

| Produk | Total Unit | Total Revenue | Rata-rata/Unit |
|---|---:|---:|---:|
| Mouse | 11 | Rp1.650.000 | Rp150.000 |
| Headset | 7 | Rp1.750.000 | Rp250.000 |
| Keyboard | 6 | Rp1.800.000 | Rp300.000 |
| Laptop | 5 | Rp36.100.000 | Rp7.220.000 |
| Monitor | 3 | Rp7.500.000 | Rp2.500.000 |

## 📊 Business Insights

### Insight 1 — Volume vs Revenue

Mouse memiliki unit terjual paling banyak, yaitu **11 unit**, sedangkan Laptop menghasilkan revenue terbesar sebesar **Rp36.100.000**.

Hal ini menunjukkan bahwa produk dengan volume penjualan tinggi belum tentu menghasilkan revenue terbesar. Perbedaan harga per unit menjadi faktor penting dalam perbedaan total revenue.

### Insight 2 — Revenue Berdasarkan Kategori

Kategori **Elektronik** menghasilkan **Rp43.600.000** dari total revenue **Rp48.800.000**, atau sekitar **89,3%**, meskipun hanya menjual **9 unit**.

Sebaliknya, Aksesoris menjual **24 unit** tetapi menghasilkan revenue **Rp5.200.000**.

### Insight 3 — Kontribusi Laptop

Laptop menyumbang sekitar **70,37%** dari seluruh revenue dengan total penjualan **5 unit**.

Ini memperlihatkan bahwa kontribusi revenue tidak dapat dinilai hanya dari jumlah unit terjual.

## 🧠 Analytical Standard

> ⚠️ **Jangan membuat kesimpulan yang melampaui evidence.**
>
> Data menunjukkan Mouse memiliki volume penjualan tertinggi dan Laptop memiliki revenue tertinggi. Namun, data ini belum cukup untuk menyatakan bahwa Mouse adalah produk yang paling diminati, produk fast-moving, atau bahwa perusahaan harus memprioritaskan Laptop.
>
> Untuk rekomendasi bisnis yang lebih kuat, masih diperlukan data seperti margin keuntungan, biaya, tren waktu, stok, dan faktor promosi.

## 🏆 Kompetensi yang Berhasil Dipraktikkan

- [x] SELECT
- [x] SUM()
- [x] GROUP BY
- [x] ORDER BY
- [x] DESC
- [x] WHERE
- [x] Alias dengan AS
- [x] Subquery sederhana
- [x] Menghitung kontribusi revenue
- [x] Menghitung rata-rata nilai per unit
- [x] Membandingkan volume penjualan dan revenue
- [x] Menulis business insight berdasarkan hasil query
- [x] Membedakan insight dengan asumsi atau causal claim

## 🔥 Refleksi Pembelajaran

Pelajaran terpenting Day 1 Week 2 adalah bahwa SQL bukan hanya tentang menulis query, tetapi menggunakan query untuk menjawab **Business Question**.

Saya mulai memahami bahwa angka harus dibaca dalam konteks. Jumlah unit yang tinggi tidak otomatis berarti revenue tinggi, dan revenue tinggi juga belum otomatis berarti produk tersebut paling menguntungkan.

Saya juga belajar untuk tidak membuat kesimpulan yang belum didukung data. Jika evidence belum cukup, saya perlu menyebutkan keterbatasannya dan mencari data tambahan.

## 🚀 Final Result

**Status:** 🟢 Completed — Day 1 Week 2

**Next Step:** Week 2 Day 2 — Instalasi & Dasar Git/GitHub
