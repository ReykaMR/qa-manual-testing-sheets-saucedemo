# 02 - Test Design

Folder ini berisi seluruh dokumen **desain pengujian** untuk aplikasi
[SauceDemo](https://www.saucedemo.com), mencakup test scenario, test data,
dan Requirement Traceability Matrix (RTM).

Dokumen di folder ini menjadi **jembatan** antara Test Planning
dan Test Execution.

---

## Daftar Dokumen

| File                                       | Deskripsi                                    | Status                    |
| ------------------------------------------ | -------------------------------------------- | ------------------------- |
| [`test-scenarios.md`](./test-scenarios.md) | Skenario pengujian tingkat tinggi per modul  | ✅ Final                  |
| [`test-data.md`](./test-data.md)           | Data uji yang digunakan (user, produk, dll)  | ✅ Final                  |
| [`rtm.md`](./rtm.md)                       | Requirement Traceability Matrix (versi awal) | 🟡 In Progress            |
| [`test-cases/`](./test-cases/)             | Test case detail per modul                   | ⬜ Belum dibuat (Tahap 3) |

---

## Alur Desain

```text
Test Plan (Tahap 1)
        ↓
Test Scenario (Tahap 2)
        ↓
Test Case Detail (Tahap 3)
        ↓
Test Execution (Tahap 5)
```

---

## Referensi Terkait

- **Test Planning** → [`../01-test-planning/`](../01-test-planning/)
- **Test Execution** → [`../03-test-execution/`](../03-test-execution/)
- **Environment** → [`../07-references/environment.md`](../07-references/environment.md)

---

_Terakhir diperbarui: 2026-09-30_
