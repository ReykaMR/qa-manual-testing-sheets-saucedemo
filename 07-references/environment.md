# Test Environment

Dokumen ini mencatat detail environment yang digunakan selama pengujian
aplikasi SauceDemo. Informasi ini penting untuk mereproduksi bug dan
memastikan konsistensi hasil testing.

---

## Application Under Test (AUT)

| Item              | Detail                            |
| ----------------- | --------------------------------- |
| **Nama Aplikasi** | SauceDemo                         |
| **URL**           | https://www.saucedemo.com         |
| **Versi**         | Demo (tidak ada versioning resmi) |
| **Tipe**          | Web Application                   |
| **Vendor**        | Sauce Labs                        |

---

## Test Environment (Local Machine)

| Komponen              | Spesifikasi                                        |
| --------------------- | -------------------------------------------------- |
| **Operating System**  | Windows 10 Pro (22H2)                              |
| **RAM**               | 16 GB                                              |
| **Storage**           | 512 GB SSD                                         |
| **Processor**         | Intel(R) Core(TM) i7-6700HQ CPU @ 2.60GHz 2.59 GHz |
| **Screen Resolution** | 1920 x 1080                                        |
| **Network**           | Wi-Fi, 25 Mbps (stable)                            |

---

## Browser yang Digunakan

| Browser         | Versi                                                    | Digunakan? | Catatan                   |
| --------------- | -------------------------------------------------------- | ---------- | ------------------------- |
| Google Chrome   | 153.0.8010.48 (Official Build) (64-bit) (cohort: Stable) | Ya         | Browser utama             |
| Mozilla Firefox | 152.0.5                                                  | Opsional   | Cross-browser testing     |
| Microsoft Edge  | 154.0.4258.37 (Official build) (64-bit)                  | Opsional   | Cross-browser testing     |
| Safari          | Latest stable                                            | Tidak      | Tidak tersedia di Windows |

**Browser default untuk testing**: **Google Chrome (latest stable)**.

> **Tips:** Cek versi browser lewat `chrome://version` (Chrome), `about:support` (Firefox), atau `edge://version` (Edge).

---

## Test Data

| User Type               | Username                  | Password       | Expected Behavior                |
| ----------------------- | ------------------------- | -------------- | -------------------------------- |
| Standard User           | `standard_user`           | `secret_sauce` | Login sukses, semua fitur normal |
| Locked Out User         | `locked_out_user`         | `secret_sauce` | Login gagal, pesan "locked out"  |
| Problem User            | `problem_user`            | `secret_sauce` | Login sukses tapi UI bermasalah  |
| Performance Glitch User | `performance_glitch_user` | `secret_sauce` | Login lambat (>5 detik)          |
| Error User              | `error_user`              | `secret_sauce` | Beberapa aksi memicu error       |
| Visual User             | `visual_user`             | `secret_sauce` | Beberapa elemen tampil salah     |

---

## Tools yang Digunakan

| Tool                                | Fungsi                                |
| ----------------------------------- | ------------------------------------- |
| **Google Chrome DevTools**          | Inspeksi elemen, cek console, network |
| **Markdown Editor** (VS Code)       | Menulis dokumentasi                   |
| **Screenshot Tool** (Snipping Tool) | Mengambil bukti bug                   |
| **Google Sheets**                   | (Opsional) cross-check test case      |
| **Git & GitHub**                    | Version control & publikasi           |

---

## Periode Testing

| Item                | Detail                               |
| ------------------- | ------------------------------------ |
| **Tanggal Mulai**   | 2026-09-29                           |
| **Tanggal Selesai** | (akan diisi setelah testing selesai) |
| **Total Sesi**      | (akan diisi)                         |

---

## Catatan Penting

- SauceDemo adalah aplikasi **demo**, jadi beberapa anomali mungkin **sengaja** dibuat oleh vendor untuk latihan.
- Bug yang ditemukan di user `problem_user`, `error_user`, dan `visual_user` **sering dianggap sebagai intended behavior** - perlu validasi sebelum dilaporkan sebagai bug.
- Password semua user sama: `secret_sauce`.
- Data user tidak persist antar sesi (reset saat refresh/logout).

---

## Referensi

- SauceDemo: https://www.saucedemo.com
- Sauce Labs Documentation: https://docs.saucelabs.com

---

_Terakhir diperbarui: 2026-09-29_
