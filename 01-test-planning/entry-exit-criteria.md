# Entry & Exit Criteria - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-29                 |
| **Status**           | Final                      |

---

## 1. Tujuan

Dokumen ini mendefinisikan **kriteria masuk (entry)** dan
**kriteria keluar (exit)** untuk setiap fase testing. Kriteria ini
memastikan testing dimulai dan diakhiri secara objektif, bukan
berdasarkan asumsi.

---

## 2. Entry Criteria (Kriteria Masuk)

Testing **tidak boleh dimulai** sebelum semua kriteria berikut terpenuhi.

### 2.1 Fase Test Design

| No  | Kriteria                                   | Status |
| --- | ------------------------------------------ | ------ |
| 1   | Test Plan telah disetujui                  | ✅     |
| 2   | Test Strategy telah disetujui              | ✅     |
| 3   | Requirement/fitur SauceDemo telah dipahami | ✅     |

### 2.2 Fase Test Execution

| No  | Kriteria                            | Status |
| --- | ----------------------------------- | ------ |
| 1   | Test case telah dibuat & direview   | ✅     |
| 2   | Test data siap (6 user type)        | ✅     |
| 3   | Environment siap (browser, koneksi) | ✅     |
| 4   | Aplikasi dapat diakses (Smoke Pass) | ✅     |

### 2.3 Fase Regression

| No  | Kriteria                                | Status |
| --- | --------------------------------------- | ------ |
| 1   | Bug telah diperbaiki (secara hipotetis) | ✅     |
| 2   | Build/versi baru tersedia               | ✅     |

---

## 3. Exit Criteria (Kriteria Keluar)

Testing **dianggap selesai** jika semua kriteria berikut terpenuhi.

### 3.1 Fase Test Execution

| No  | Kriteria                               | Target |
| --- | -------------------------------------- | ------ |
| 1   | Test case dieksekusi                   | 100%   |
| 2   | Pass rate                              | ≥ 90%  |
| 3   | Semua High severity bug terdokumentasi | 100%   |
| 4   | Execution log & evidence lengkap       | 100%   |

### 3.2 Fase Defect Management

| No  | Kriteria                                  | Target |
| --- | ----------------------------------------- | ------ |
| 1   | Semua bug memiliki bug report lengkap     | 100%   |
| 2   | Bug telah di-triage (severity & priority) | 100%   |
| 3   | Bug summary dibuat                        | ✅     |

### 3.3 Fase Test Closure

| No  | Kriteria                         | Target |
| --- | -------------------------------- | ------ |
| 1   | Test Summary Report dibuat       | ✅     |
| 2   | Test Metrics dihitung            | ✅     |
| 3   | Lessons Learned didokumentasikan | ✅     |
| 4   | Sign-off dari QA Engineer        | ✅     |

---

## 4. Suspension & Resumption Criteria

### 4.1 Suspension (Penghentian Sementara)

Testing **dihentikan sementara** jika:

- Aplikasi tidak dapat diakses (server down).
- Ditemukan bug **blocker** yang menghalangi alur utama.
- Environment bermasalah (browser crash berulang).

### 4.2 Resumption (Lanjut Kembali)

Testing **dilanjutkan** jika:

- Aplikasi dapat diakses kembali.
- Blocker bug telah di-_workaround_ atau diperbaiki.
- Environment stabil.

---

## 5. Definition of Done (DoD)

Sebuah test case dianggap **selesai** jika:

- ✅ Telah dieksekusi minimal 1 kali.
- ✅ Hasil (Pass/Fail/Blocked) tercatat di execution log.
- ✅ Jika Fail → bug report telah dibuat dengan evidence.
- ✅ Status di test case diperbarui.

---

## 6. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-29 | ✅           |

---

_Terakhir diperbarui: 2026-09-29_
