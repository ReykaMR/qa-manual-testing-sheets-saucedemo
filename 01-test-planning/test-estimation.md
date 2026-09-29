# Test Estimation - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-29                 |
| **Status**           | Final                      |

---

## 1. Tujuan

Dokumen ini berisi estimasi effort (waktu) yang dibutuhkan untuk
menguji setiap modul SauceDemo. Estimasi digunakan sebagai acuan
penjadwalan dan pengukuran produktivitas.

---

## 2. Metode Estimasi

Metode yang digunakan: **Expert Judgment** dengan pendekatan
**Three-Point Estimation**.

**Rumus:** E = (O + 4M + P) / 6

- **O** = Optimistic (waktu tercepat)
- **M** = Most Likely (waktu paling mungkin)
- **P** = Pessimistic (waktu terlama)
- **E** = Expected (estimasi akhir)

---

## 3. Estimasi per Modul

| Modul                      | Optimistic (jam) | Most Likely (jam) | Pessimistic (jam) | Estimasi (jam) |
| -------------------------- | ---------------- | ----------------- | ----------------- | -------------- |
| Login                      | 1.5              | 3                 | 4                 | 2.9            |
| Logout                     | 0.5              | 1                 | 1.5               | 1.0            |
| Inventory                  | 2                | 4                 | 6                 | 4.0            |
| Product Detail             | 1                | 2                 | 3                 | 2.0            |
| Cart                       | 2                | 4                 | 6                 | 4.0            |
| Checkout                   | 4                | 6                 | 9                 | 6.2            |
| Exploratory (lintas modul) | 2                | 3                 | 5                 | 3.2            |
| Regression                 | 1                | 2                 | 4                 | 2.2            |
| **Total**                  | **14**           | **25**            | **38.5**          | **25.5**       |

---

## 4. Breakdown Aktivitas per Modul

### 4.1 Login (2.9 jam)

- Design test case: 1 jam
- Eksekusi (6 user type): 1 jam
- Dokumentasi bug: 0.5 jam
- Review & evidence: 0.4 jam

### 4.2 Checkout (6.2 jam)

- Design test case: 2 jam
- Eksekusi (alur sukses + validasi form): 2.5 jam
- Dokumentasi bug: 1 jam
- Review & evidence: 0.7 jam

### 4.3 Modul lainnya

Mengikuti pola serupa: **design → execution → defect → review**.

---

## 5. Estimasi Total Proyek

| Fase                          | Estimasi (jam) |
| ----------------------------- | -------------- |
| Test Planning                 | 4              |
| Test Design (Scenario + Case) | 8              |
| Test Execution                | 6              |
| Defect Management             | 4              |
| Test Closure                  | 2              |
| Buffer (10%)                  | 2.5            |
| **Total**                     | **26.5 jam**   |

---

## 6. Asumsi

1. QA bekerja sendiri tanpa gangguan signifikan.
2. Environment sudah siap (tidak ada waktu setup besar).
3. Tidak ada perubahan scope selama testing.
4. Aplikasi dapat diakses 24/7 (SauceDemo demo).

---

## 7. Catatan

- Estimasi ini **tidak termasuk** waktu belajar tools baru.
- Jika ditemukan bug kompleks, waktu bisa bertambah 10-20%.

---

_Terakhir diperbarui: 2026-09-29_
