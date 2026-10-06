# Week 2 — Day 2

## Instalasi & Dasar Git/GitHub



### Tujuan Pembelajaran



- Memahami perbedaan Git dan GitHub.

- Memahami Repository, Working Directory, Staging Area, Commit, Branch, dan Remote.

- Memahami workflow dasar Git.

- Menggunakan Git untuk mendokumentasikan project Data Analyst.



---



## 1. Git vs GitHub



### Git

Git adalah version control yang berjalan di komputer lokal untuk mencatat dan melacak perubahan pada project.



### GitHub

GitHub adalah platform online untuk menyimpan dan membagikan repository Git.



Analogi:



- Git = buku catatan versi di laptop.

- GitHub = tempat menyimpan dan membagikan buku tersebut secara online.



---



## 2. Git Workflow



Workflow dasar Git:



Working Directory

→ git add

→ Staging Area

→ git commit

→ Local Repository

→ git push

→ GitHub



Urutan kerja:



Edit file

→ Check status

→ Stage perubahan

→ Commit

→ Push

→ Verify di GitHub



---



## 3. Perintah Git yang Dipelajari



### Mengecek versi Git

```powershell
git --version
```

### Mengecek status repository

```powershell
git status
```

### Stage perubahan

```powershell
git add .
```

### Commit perubahan

```powershell
git commit -m "docs: add Week 2 Day 2 Git fundamentals"
```

### Push ke GitHub

```powershell
git push origin main
```

### Memastikan remote repository

```powershell
git remote -v
```

---

## 4. Praktik yang Dilakukan

Repository:

```text
EgiKurnianto/data-analyst-bootcamp
```

Environment: **Windows PowerShell**

Workflow:

Edit → git status → git add → git commit → git push → Verify on GitHub

Git terverifikasi dengan:

```text
git version 2.43.0.windows.1
```

Repository berhasil digunakan untuk menyimpan dokumentasi bootcamp dan perubahan berhasil diverifikasi di branch main.

## 5. Repository Relevance

GitHub digunakan untuk menyimpan SQL queries, dataset/data dictionary, dokumentasi cleaning, analysis notebook, dashboard documentation, README, insight/recommendation, dan changelog.

Tujuannya agar portfolio menunjukkan **proses yang reproducible**, bukan hanya hasil akhir.

## 6. Professional Habit

**Document → Track → Review → Improve**

Setiap perubahan sebaiknya dapat dijelaskan: apa yang berubah, mengapa berubah, kapan berubah, dan apa dampaknya.

## 7. Key Learning

Version control bukan hanya skill coding. Untuk Data Analyst, Git membantu membangun kebiasaan dokumentasi, reproducibility, dan pengelolaan portfolio yang lebih profesional.

**Status:** 🟢 Completed

**Next:** Week 2 Day 3 — SQL Query Fundamentals & Analysis
