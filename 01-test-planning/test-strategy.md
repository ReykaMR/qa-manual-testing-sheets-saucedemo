# Test Strategy - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-29                 |
| **Status**           | Final                      |

---

## 1. Tujuan Dokumen

Dokumen ini mendefinisikan **pendekatan strategis** pengujian aplikasi
SauceDemo secara manual. Strategi ini menjadi dasar penyusunan
[Test Plan](./test-plan.md) dan seluruh aktivitas testing berikutnya.

---

## 2. Ruang Lingkup Strategi

Strategi ini mencakup:

- Jenis testing yang akan dilakukan.
- Level testing yang diterapkan.
- Pendekatan desain test case.
- Kriteria masuk dan keluar testing.

**Di luar cakupan:** performance testing, security testing, dan
API testing (dijelaskan di bagian _Out of Scope_ pada Test Plan).

---

## 3. Jenis Testing (Test Types)

| Jenis Testing           | Diterapkan? | Alasan                                          |
| ----------------------- | ----------- | ----------------------------------------------- |
| **Functional Testing**  | ✅ Ya       | Memverifikasi fitur berjalan sesuai requirement |
| **UI/Visual Testing**   | ✅ Ya       | Memeriksa tampilan & layout antar user type     |
| **Regression Testing**  | ✅ Ya       | Memastikan perubahan tidak merusak fitur lama   |
| **Exploratory Testing** | ✅ Ya       | Menemukan bug yang tidak tercakup test case     |
| **Smoke Testing**       | ✅ Ya       | Verifikasi cepat build sebelum testing penuh    |
| **Sanity Testing**      | ✅ Ya       | Verifikasi perbaikan bug spesifik               |
| **Performance Testing** | ❌ Tidak    | Di luar scope (aplikasi demo)                   |
| **Security Testing**    | ❌ Tidak    | Di luar scope                                   |
| **API Testing**         | ❌ Tidak    | Tidak ada akses API publik                      |
| **Automation Testing**  | ❌ Tidak    | Fokus manual testing                            |

---

## 4. Level Testing (Test Levels)

Karena SauceDemo adalah aplikasi eksternal tanpa akses source code,
hanya **System Testing** yang diterapkan.

| Level                             | Diterapkan? | Catatan                    |
| --------------------------------- | ----------- | -------------------------- |
| Unit Testing                      | ❌          | Tidak ada akses kode       |
| Integration Testing               | ❌          | Tidak ada akses internal   |
| **System Testing**                | ✅          | Level utama pengujian      |
| **User Acceptance Testing (UAT)** | ⚠️ Parsial  | Simulasi skenario end-user |

---

## 5. Pendekatan Testing

### 5.1 Risk-Based Testing

Prioritas testing difokuskan pada fitur dengan **risiko tertinggi**:

1. **Login** - pintu masuk semua fitur (Critical).
2. **Checkout** - melibatkan transaksi & perhitungan harga (High).
3. **Cart** - berkaitan langsung dengan checkout (High).
4. **Inventory** - fitur utama setelah login (Medium).
5. **Logout** - fitur sederhana (Low).

### 5.2 Time-Boxed Exploratory Testing

Sesi exploratory testing dibatasi waktu (misal 30 menit per modul)
untuk menjaga fokus dan mendokumentasikan temuan.

### 5.3 Multi-User Perspective

Karena SauceDemo memiliki 6 tipe user dengan karakteristik berbeda,
testing dilakukan dengan **mempertimbangkan setiap user type** untuk
menemukan anomali yang spesifik.

---

## 6. Kriteria Kualitas

| Kriteria                | Target               |
| ----------------------- | -------------------- |
| Test Case Coverage      | 100% fitur utama     |
| Pass Rate               | ≥ 90%                |
| High Severity Bug       | Semua terdokumentasi |
| Bug Report Completeness | 100% dengan evidence |

---

## 7. Deliverables

- Test Plan
- Test Scenarios & Test Cases
- Execution Log & Evidence
- Bug Reports
- Test Summary Report

---

## 8. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-29 | ✅           |

---

_Terakhir diperbarui: 2026-09-29_
