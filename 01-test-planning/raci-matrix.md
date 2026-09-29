# RACI Matrix - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-29                 |
| **Status**           | Final                      |

---

## 1. Pengertian RACI

| Huruf | Peran       | Arti                                    |
| ----- | ----------- | --------------------------------------- |
| **R** | Responsible | Yang mengerjakan                        |
| **A** | Accountable | Yang bertanggung jawab akhir (approver) |
| **C** | Consulted   | Yang dimintai pendapat                  |
| **I** | Informed    | Yang diberi informasi                   |

---

## 2. Struktur Tim

Karena proyek ini dikerjakan secara **individu**,
RACI disusun untuk menunjukkan pemahaman konsep dan kesiapan
berkolaborasi di tim nyata.

| Peran             | Deskripsi                                    |
| ----------------- | -------------------------------------------- |
| **QA Engineer**   | Pelaksana utama testing                      |
| **Project Owner** | (Simulasi) Stakeholder yang menyetujui hasil |
| **Developer**     | (Simulasi) Pihak yang memperbaiki bug        |

---

## 3. RACI Matrix

| Aktivitas                    | QA Engineer | Project Owner | Developer |
| ---------------------------- | ----------- | ------------- | --------- |
| Menyusun Test Strategy       | **R/A**     | I             | –         |
| Menyusun Test Plan           | **R/A**     | I             | –         |
| Membuat Test Scenario        | **R/A**     | –             | –         |
| Membuat Test Case            | **R/A**     | I             | –         |
| Review Test Case             | **R**       | **A**         | C         |
| Setup Environment            | **R/A**     | –             | C         |
| Eksekusi Test Case           | **R/A**     | I             | –         |
| Melaporkan Bug               | **R/A**     | I             | **I**     |
| Triase Bug                   | **R**       | **A**         | C         |
| Verifikasi Perbaikan Bug     | **R/A**     | I             | **I**     |
| Regression Testing           | **R/A**     | I             | –         |
| Menyusun Test Summary Report | **R/A**     | I             | –         |
| Sign-off Testing             | **R**       | **A**         | I         |

**Keterangan:**

- **Bold** = peran utama.
- `–` = tidak terlibat.

---

## 4. Catatan

- Dalam proyek nyata, **Developer** dan **Project Owner** adalah
  orang berbeda. Di sini hanya simulasi.
- RACI membantu menghindari ambiguitas: "siapa yang approve?"
  dan "siapa yang harus diberi tahu?".

---

## 5. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-29 | ✅           |

---

_Terakhir diperbarui: 2026-09-29_
