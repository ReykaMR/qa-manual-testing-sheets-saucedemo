# Test Plan - SauceDemo

| Field                | Value                               |
| -------------------- | ----------------------------------- |
| **Project**          | Manual Testing - SauceDemo          |
| **Document Version** | 1.0                                 |
| **Author**           | Reyka Mochammad Raihan              |
| **Date**             | 2026-09-29                          |
| **Status**           | Final                               |
| **Reference**        | [Test Strategy](./test-strategy.md) |

---

## 1. Introduction

Dokumen ini merupakan **Test Plan** untuk pengujian manual aplikasi
[SauceDemo](https://www.saucedemo.com). Test Plan ini menjelaskan
ruang lingkup, pendekatan, jadwal, sumber daya, dan kriteria
keberhasilan pengujian.

---

## 2. Test Objective

Tujuan pengujian ini adalah:

1. Memverifikasi bahwa fitur utama SauceDemo berjalan sesuai ekspektasi.
2. Mengidentifikasi bug pada alur login, inventory, cart, checkout, dan logout.
3. Memvalidasi perilaku setiap tipe user (standard, locked, problem, dll).
4. Mendokumentasikan hasil testing secara sistematis.

---

## 3. Scope

### 3.1 In Scope ✅

| Fitur / Modul      | Deskripsi                             |
| ------------------ | ------------------------------------- |
| **Login**          | Autentikasi dengan 6 tipe user        |
| **Logout**         | Keluar dari sesi                      |
| **Inventory**      | Daftar produk, sorting, filter        |
| **Product Detail** | Halaman detail produk                 |
| **Cart**           | Tambah, hapus, lihat isi cart         |
| **Checkout**       | Form informasi, ringkasan, konfirmasi |

### 3.2 Out of Scope ❌

- Performance & load testing.
- Security & penetration testing.
- API testing.
- Accessibility testing (WCAG).
- Mobile responsiveness (fokus: desktop).
- Automation testing.

---

## 4. Test Approach

Pendekatan testing mengacu pada [Test Strategy](./test-strategy.md):

- **Risk-Based Testing** - fokus pada fitur berisiko tinggi.
- **Exploratory Testing** - sesi time-boxed per modul.
- **Multi-User Testing** - setiap user type diuji.
- **Manual Execution** - semua test case dieksekusi manual.

---

## 5. Test Deliverables

| No  | Deliverable         | Lokasi                                   |
| --- | ------------------- | ---------------------------------------- |
| 1   | Test Scenarios      | `02-test-design/test-scenarios.md`       |
| 2   | Test Cases          | `02-test-design/test-cases/`             |
| 3   | RTM                 | `02-test-design/rtm.md`                  |
| 4   | Execution Log       | `03-test-execution/execution-log.md`     |
| 5   | Bug Reports         | `04-defect-management/bug-reports/`      |
| 6   | Test Summary Report | `05-test-closure/test-summary-report.md` |

---

## 6. Test Schedule

| Fase      | Aktivitas                   | Estimasi   | Target Selesai |
| --------- | --------------------------- | ---------- | -------------- |
| 1         | Test Planning               | 4 jam      | Hari 1         |
| 2         | Test Scenario & Case Design | 8 jam      | Hari 2-3       |
| 3         | Environment Setup           | 1 jam      | Hari 3         |
| 4         | Test Execution              | 6 jam      | Hari 4-5       |
| 5         | Defect Management           | 4 jam      | Hari 5-6       |
| 6         | Test Closure                | 2 jam      | Hari 7         |
| **Total** |                             | **25 jam** | **7 hari**     |

---

## 7. Resource & Roles

| Peran       | Nama                   | Tanggung Jawab            |
| ----------- | ---------------------- | ------------------------- |
| QA Engineer | Reyka Mochammad Raihan | Seluruh aktivitas testing |

> **Catatan:** Proyek ini dikerjakan secara individu.
> [RACI Matrix](./raci-matrix.md) tetap disusun untuk menunjukkan pemahaman konsep.

---

## 8. Test Environment

Detail lengkap tersedia di [`../07-references/environment.md`](../07-references/environment.md).

| Komponen              | Detail                                  |
| --------------------- | --------------------------------------- |
| **OS**                | Windows 10 Pro                          |
| **Browser Utama**     | Google Chrome (latest stable)           |
| **Screen Resolution** | 1920 x 1080                             |
| **Tools**             | Chrome DevTools, VS Code, Snipping Tool |
| **AUT URL**           | https://www.saucedemo.com               |

---

## 9. Entry & Exit Criteria

Detail lengkap di [`entry-exit-criteria.md`](./entry-exit-criteria.md).

- **Entry:** Aplikasi dapat diakses, test case siap, environment siap.
- **Exit:** 100% test case dieksekusi, semua High bug terdokumentasi.

---

## 10. Risk & Mitigation

Daftar lengkap di [`risk-register.md`](./risk-register.md).

Risiko utama:

- Beberapa bug di SauceDemo adalah _intended_ (sengaja dibuat).
- Waktu testing terbatas.

---

## 11. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-29 | ✅           |

---

_Terakhir diperbarui: 2026-09-29_
