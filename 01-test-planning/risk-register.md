# Risk Register - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-29                 |
| **Status**           | Final                      |

---

## 1. Tujuan

Dokumen ini mengidentifikasi **risiko** yang mungkin muncul selama
proses testing, beserta **dampak** dan **strategi mitigasi**-nya.

---

## 2. Skala Penilaian

### 2.1 Probability (Kemungkinan)

| Level  | Nilai | Deskripsi                 |
| ------ | ----- | ------------------------- |
| Low    | 1     | Kemungkinan kecil terjadi |
| Medium | 2     | Mungkin terjadi           |
| High   | 3     | Sangat mungkin terjadi    |

### 2.2 Impact (Dampak)

| Level  | Nilai | Deskripsi                   |
| ------ | ----- | --------------------------- |
| Low    | 1     | Dampak kecil, mudah diatasi |
| Medium | 2     | Mengganggu progres testing  |
| High   | 3     | Menghentikan testing        |

### 2.3 Risk Score

Risk Score = Probability × Impact

| Skor | Level     | Aksi                      |
| ---- | --------- | ------------------------- |
| 1-2  | 🟢 Low    | Monitor                   |
| 3-4  | 🟡 Medium | Mitigasi                  |
| 6-9  | 🔴 High   | Mitigasi ketat + eskalasi |

---

## 3. Daftar Risiko

| ID   | Risiko                                                                  | Prob | Impact | Skor | Level     | Mitigasi                                                                 |
| ---- | ----------------------------------------------------------------------- | ---- | ------ | ---- | --------- | ------------------------------------------------------------------------ |
| R-01 | Beberapa anomali di SauceDemo adalah _intended_ (sengaja dibuat vendor) | 3    | 2      | 6    | 🔴 High   | Validasi dengan dokumentasi Sauce Labs; bedakan _intended_ vs _real bug_ |
| R-02 | Waktu testing terbatas                                                  | 2    | 3      | 6    | 🔴 High   | Gunakan risk-based testing; prioritaskan modul High                      |
| R-03 | Aplikasi SauceDemo tidak dapat diakses (server down)                    | 1    | 3      | 3    | 🟡 Medium | Coba beberapa kali; catat sebagai blocked; lanjut ke modul lain          |
| R-04 | Browser crash / hang saat testing                                       | 2    | 2      | 4    | 🟡 Medium | Restart browser; simpan bukti sebelum crash                              |
| R-05 | Data test (user) tidak konsisten antar sesi                             | 2    | 2      | 4    | 🟡 Medium | Logout & clear cache setiap ganti user                                   |
| R-06 | Bug sulit direproduksi (intermittent)                                   | 2    | 2      | 4    | 🟡 Medium | Catat step-by-step; rekam video; coba minimal 3x                         |
| R-07 | Test case tidak mencakup edge case                                      | 2    | 2      | 4    | 🟡 Medium | Review test case; tambahkan exploratory testing                          |
| R-08 | Kehilangan progress karena tidak commit Git                             | 1    | 3      | 3    | 🟡 Medium | Commit setiap selesai 1 file/dokumen                                     |

---

## 4. Risk Heatmap

| Impact \ Probability | 1          | 2                      | 3    |
| -------------------- | ---------- | ---------------------- | ---- |
| **3 - High**         | R-03, R-08 | R-02                   | -    |
| **2 - Medium**       | -          | R-04, R-05, R-06, R-07 | R-01 |
| **1 - Low**          | -          | -                      | -    |

**High-risk items:** R-01 dan R-02 (Risk Score = 6).

**Catatan:** R-01 memiliki Probability 3 × Impact 2, sedangkan R-02 memiliki Probability 2 × Impact 3.

---

## 5. Risk Response Plan

### R-01 - Anomali Intended vs Real Bug

- **Strategi:** Mitigate
- **Aksi:**
  - Cek dokumentasi Sauce Labs.
  - Bandingkan perilaku antar user type.
  - Jika ragu, tandai sebagai "**potential bug**" dan jelaskan asumsi.

### R-02 - Waktu Terbatas

- **Strategi:** Mitigate
- **Aksi:**
  - Fokus pada modul dengan risiko tertinggi (Login, Checkout).
  - Gunakan time-box 30 menit per sesi exploratory.
  - Jangan kejar jumlah test case, kejar kualitas.

---

## 6. Review & Update

Risk register ini akan di-review:

- **Setiap akhir fase** testing.
- **Ketika ada risiko baru** yang muncul.

---

## 7. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-29 | ✅           |

---

_Terakhir diperbarui: 2026-09-29_
