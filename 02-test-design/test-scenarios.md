# Test Scenarios - SauceDemo

| Field                | Value                                         |
| -------------------- | --------------------------------------------- |
| **Project**          | Manual Testing - SauceDemo                    |
| **Document Version** | 1.0                                           |
| **Author**           | Reyka Mochammad Raihan                        |
| **Date**             | 2026-09-30                                    |
| **Status**           | Final                                         |
| **Reference**        | [Test Plan](../01-test-planning/test-plan.md) |

---

## 1. Tujuan

Dokumen ini berisi **daftar skenario pengujian** (test scenarios) untuk
aplikasi SauceDemo. Setiap skenario menggambarkan **apa yang akan diuji**
pada tingkat tinggi, tanpa langkah detail (yang akan dijelaskan di
[test case](../02-test-design/test-cases/)).

---

## 2. Konvensi Penomoran

| Format       | Contoh   | Keterangan       |
| ------------ | -------- | ---------------- |
| `TS-<nomor>` | `TS-001` | Test Scenario ID |

**Modul & rentang nomor:**

| Modul          | Rentang         | Jumlah |
| -------------- | --------------- | ------ |
| Login          | TS-001 – TS-010 | 10     |
| Logout         | TS-011 – TS-013 | 3      |
| Inventory      | TS-014 – TS-022 | 9      |
| Product Detail | TS-023 – TS-026 | 4      |
| Cart           | TS-027 – TS-034 | 8      |
| Checkout       | TS-035 – TS-045 | 11     |
| **Total**      |                 | **45** |

---

## 3. Modul: Login

**Tujuan:** memverifikasi proses autentikasi pengguna dengan berbagai
kondisi input dan tipe user.

**User type terkait:** `standard_user`, `locked_out_user`, `problem_user`,
`performance_glitch_user`, `error_user`, `visual_user`.

| ID     | Scenario                                      | Priority | User Type               |
| ------ | --------------------------------------------- | -------- | ----------------------- |
| TS-001 | Login dengan kredensial valid (standard user) | High     | standard_user           |
| TS-002 | Login dengan password salah                   | High     | standard_user           |
| TS-003 | Login dengan username salah                   | High     | –                       |
| TS-004 | Login dengan username & password kosong       | Medium   | –                       |
| TS-005 | Login hanya mengisi username                  | Medium   | standard_user           |
| TS-006 | Login hanya mengisi password                  | Medium   | –                       |
| TS-007 | Login dengan locked_out_user                  | High     | locked_out_user         |
| TS-008 | Login dengan problem_user                     | High     | problem_user            |
| TS-009 | Login dengan performance_glitch_user          | Medium   | performance_glitch_user |
| TS-010 | Login dengan error_user & visual_user         | Medium   | error_user, visual_user |

---

## 4. Modul: Logout

**Tujuan:** memverifikasi proses keluar dari sesi aplikasi.

| ID     | Scenario                                            | Priority | User Type     |
| ------ | --------------------------------------------------- | -------- | ------------- |
| TS-011 | Logout dari halaman inventory                       | High     | standard_user |
| TS-012 | Verifikasi redirect setelah logout                  | High     | standard_user |
| TS-013 | Akses halaman inventory setelah logout (direct URL) | High     | standard_user |

---

## 5. Modul: Inventory

**Tujuan:** memverifikasi tampilan daftar produk, sorting, dan filter.

| ID     | Scenario                                      | Priority | User Type     |
| ------ | --------------------------------------------- | -------- | ------------- |
| TS-014 | Menampilkan semua produk di halaman inventory | High     | standard_user |
| TS-015 | Sorting produk: Name (A to Z)                 | Medium   | standard_user |
| TS-016 | Sorting produk: Name (Z to A)                 | Medium   | standard_user |
| TS-017 | Sorting produk: Price (low to high)           | High     | standard_user |
| TS-018 | Sorting produk: Price (high to low)           | High     | standard_user |
| TS-019 | Verifikasi sorting pada problem_user          | High     | problem_user  |
| TS-020 | Verifikasi gambar produk pada visual_user     | Medium   | visual_user   |
| TS-021 | Klik produk untuk membuka detail              | Medium   | standard_user |
| TS-022 | Verifikasi badge cart saat kosong             | Low      | standard_user |

---

## 6. Modul: Product Detail

**Tujuan:** memverifikasi halaman detail produk.

| ID     | Scenario                                            | Priority | User Type     |
| ------ | --------------------------------------------------- | -------- | ------------- |
| TS-023 | Menampilkan informasi lengkap produk                | Medium   | standard_user |
| TS-024 | Tambah produk ke cart dari halaman detail           | High     | standard_user |
| TS-025 | Kembali ke inventory dari halaman detail            | Medium   | standard_user |
| TS-026 | Verifikasi konsistensi harga di detail vs inventory | Medium   | standard_user |

---

## 7. Modul: Cart

**Tujuan:** memverifikasi pengelolaan keranjang belanja.

| ID     | Scenario                                                 | Priority | User Type     |
| ------ | -------------------------------------------------------- | -------- | ------------- |
| TS-027 | Menambahkan 1 produk ke cart                             | High     | standard_user |
| TS-028 | Menambahkan beberapa produk ke cart                      | High     | standard_user |
| TS-029 | Verifikasi badge cart bertambah                          | Medium   | standard_user |
| TS-030 | Menghapus produk dari cart                               | High     | standard_user |
| TS-031 | Menghapus semua produk dari cart                         | Medium   | standard_user |
| TS-032 | Melanjutkan belanja dari cart                            | Medium   | standard_user |
| TS-033 | Verifikasi isi cart konsisten dengan produk yang dipilih | High     | standard_user |
| TS-034 | Verifikasi penambahan produk pada problem_user           | High     | problem_user  |

---

## 8. Modul: Checkout

**Tujuan:** memverifikasi alur checkout dari form hingga konfirmasi.

| ID     | Scenario                                            | Priority | User Type     |
| ------ | --------------------------------------------------- | -------- | ------------- |
| TS-035 | Checkout dengan data valid                          | High     | standard_user |
| TS-036 | Checkout dengan First Name kosong                   | High     | standard_user |
| TS-037 | Checkout dengan Last Name kosong                    | High     | standard_user |
| TS-038 | Checkout dengan Postal Code kosong                  | High     | standard_user |
| TS-039 | Checkout dengan semua field kosong                  | High     | standard_user |
| TS-040 | Cancel checkout dari halaman form                   | Medium   | standard_user |
| TS-041 | Cancel checkout dari halaman overview               | Medium   | standard_user |
| TS-042 | Verifikasi ringkasan pesanan (produk, harga, pajak) | High     | standard_user |
| TS-043 | Verifikasi perhitungan total = subtotal + tax       | High     | standard_user |
| TS-044 | Selesaikan checkout hingga halaman konfirmasi       | High     | standard_user |
| TS-045 | Verifikasi cart kosong setelah checkout sukses      | High     | standard_user |

---

## 9. Skenario Lintas Modul (Exploratory)

**Tujuan:** menemukan bug di luar test case formal.

| ID       | Scenario                                                   | Priority |
| -------- | ---------------------------------------------------------- | -------- |
| TS-EX-01 | Alur end-to-end: login → tambah produk → checkout → logout | High     |
| TS-EX-02 | Refresh halaman di tengah alur checkout                    | Medium   |
| TS-EX-03 | Buka beberapa tab dengan sesi berbeda                      | Low      |

> **Catatan:** Skenario eksploratori tidak memiliki test case formal,
> tetapi hasilnya didokumentasikan di
> [`../03-test-execution/execution-log.md`](../03-test-execution/execution-log.md).

---

## 10. Ringkasan

| Modul          | Jumlah Scenario | High   | Medium | Low   |
| -------------- | --------------- | ------ | ------ | ----- |
| Login          | 10              | 6      | 4      | 0     |
| Logout         | 3               | 3      | 0      | 0     |
| Inventory      | 9               | 4      | 4      | 1     |
| Product Detail | 4               | 1      | 3      | 0     |
| Cart           | 8               | 4      | 3      | 0     |
| Checkout       | 11              | 8      | 3      | 0     |
| Exploratory    | 3               | 1      | 1      | 1     |
| **Total**      | **48**          | **27** | **18** | **2** |

---

## 11. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-30 | ✅           |

---

_Terakhir diperbarui: 2026-09-30_
