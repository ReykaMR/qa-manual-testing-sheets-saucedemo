# Requirement Traceability Matrix (RTM) - SauceDemo

| Field                | Value                                               |
| -------------------- | --------------------------------------------------- |
| **Project**          | Manual Testing - SauceDemo                          |
| **Document Version** | 1.0 (Initial)                                       |
| **Author**           | Reyka Mochammad Raihan                              |
| **Date**             | 2026-09-30                                          |
| **Status**           | 🟡 In Progress - Test Case ID akan diisi di Tahap 3 |

---

## 1. Tujuan

Requirement Traceability Matrix (RTM) adalah matriks yang **memetakan**
setiap requirement/fitur ke test scenario dan test case yang
memverifikasinya. Tujuan RTM:

1. Memastikan **semua requirement tercakup** oleh test case.
2. Memastikan **tidak ada test case yang tidak perlu** (orphan).
3. Memudahkan **impact analysis** saat ada perubahan.
4. Menjadi **bukti dokumentasi** cakupan testing.

---

## 2. Konvensi

| Kode     | Arti                            |
| -------- | ------------------------------- |
| `REQ-XX` | Requirement ID                  |
| `TS-XXX` | Test Scenario ID                |
| `TC-XXX` | Test Case ID (diisi di Tahap 3) |
| ✅       | Covered                         |
| ⬜       | Pending                         |

---

## 3. Matriks Traceability

| REQ ID | Requirement                                               | Sumber    | Test Scenario                          | Test Case | Status |
| ------ | --------------------------------------------------------- | --------- | -------------------------------------- | --------- | ------ |
| REQ-01 | Sistem harus mengautentikasi user dengan kredensial valid | SauceDemo | TS-001, TS-008, TS-009, TS-010         | ⬜        | 🟡     |
| REQ-02 | Sistem harus menolak kredensial invalid                   | SauceDemo | TS-002, TS-003, TS-004, TS-005, TS-006 | ⬜        | 🟡     |
| REQ-03 | Sistem harus memblokir akun locked_out_user               | SauceDemo | TS-007                                 | ⬜        | 🟡     |
| REQ-04 | User dapat logout dari aplikasi                           | SauceDemo | TS-011, TS-012                         | ⬜        | 🟡     |
| REQ-05 | Sistem harus menolak akses setelah logout                 | SauceDemo | TS-013                                 | ⬜        | 🟡     |
| REQ-06 | Sistem menampilkan daftar produk di halaman inventory     | SauceDemo | TS-014                                 | ⬜        | 🟡     |
| REQ-07 | User dapat sorting produk berdasarkan nama                | SauceDemo | TS-015, TS-016                         | ⬜        | 🟡     |
| REQ-08 | User dapat sorting produk berdasarkan harga               | SauceDemo | TS-017, TS-018, TS-019                 | ⬜        | 🟡     |
| REQ-09 | Sistem menampilkan gambar produk yang benar               | SauceDemo | TS-020                                 | ⬜        | 🟡     |
| REQ-10 | User dapat membuka halaman detail produk                  | SauceDemo | TS-021, TS-023                         | ⬜        | 🟡     |
| REQ-11 | User dapat menambahkan produk ke cart                     | SauceDemo | TS-024, TS-027, TS-028, TS-034         | ⬜        | 🟡     |
| REQ-12 | Sistem menampilkan badge jumlah item di cart              | SauceDemo | TS-022, TS-029                         | ⬜        | 🟡     |
| REQ-13 | User dapat menghapus produk dari cart                     | SauceDemo | TS-030, TS-031                         | ⬜        | 🟡     |
| REQ-14 | Cart menampilkan produk yang dipilih dengan benar         | SauceDemo | TS-033                                 | ⬜        | 🟡     |
| REQ-15 | User dapat melanjutkan belanja dari cart                  | SauceDemo | TS-032                                 | ⬜        | 🟡     |
| REQ-16 | User dapat memulai proses checkout                        | SauceDemo | TS-035                                 | ⬜        | 🟡     |
| REQ-17 | Sistem memvalidasi field First Name saat checkout         | SauceDemo | TS-036, TS-039                         | ⬜        | 🟡     |
| REQ-18 | Sistem memvalidasi field Last Name saat checkout          | SauceDemo | TS-037, TS-039                         | ⬜        | 🟡     |
| REQ-19 | Sistem memvalidasi field Postal Code saat checkout        | SauceDemo | TS-038, TS-039                         | ⬜        | 🟡     |
| REQ-20 | User dapat cancel checkout                                | SauceDemo | TS-040, TS-041                         | ⬜        | 🟡     |
| REQ-21 | Sistem menampilkan ringkasan pesanan dengan benar         | SauceDemo | TS-042                                 | ⬜        | 🟡     |
| REQ-22 | Sistem menghitung total = subtotal + tax                  | SauceDemo | TS-043                                 | ⬜        | 🟡     |
| REQ-23 | User dapat menyelesaikan checkout                         | SauceDemo | TS-044                                 | ⬜        | 🟡     |
| REQ-24 | Cart dikosongkan setelah checkout sukses                  | SauceDemo | TS-045                                 | ⬜        | 🟡     |
| REQ-25 | Alur end-to-end berjalan tanpa bug blocker                | SauceDemo | TS-EX-01, TS-EX-02, TS-EX-03           | ⬜        | 🟡     |

---

## 4. Coverage Summary

| Metrik                | Nilai          |
| --------------------- | -------------- |
| Total Requirement     | 25             |
| Total Test Scenario   | 48             |
| Requirement Covered   | 25 / 25 (100%) |
| Test Case ID Assigned | 0 / 48 (0%)    |

> **Status 🟡 In Progress:** Kolom Test Case akan diisi di Tahap 3
> setelah test case detail dibuat.

---

## 5. Catatan

- **Requirement** di sini bersumber dari observasi fitur SauceDemo
  (tidak ada dokumen SRS resmi dari vendor).
- **Exploratory testing** (TS-EX) tidak dipetakan ke requirement
  spesifik karena sifatnya eksploratif.
- RTM akan di-review ulang di akhir Tahap 3 untuk memastikan
  semua requirement sudah memiliki test case.

---

## 6. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-30 | ✅           |

---

_Terakhir diperbarui: 2026-09-30_
