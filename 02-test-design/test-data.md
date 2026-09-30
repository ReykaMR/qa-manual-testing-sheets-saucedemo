# Test Data - SauceDemo

| Field                | Value                      |
| -------------------- | -------------------------- |
| **Project**          | Manual Testing - SauceDemo |
| **Document Version** | 1.0                        |
| **Author**           | Reyka Mochammad Raihan     |
| **Date**             | 2026-09-30                 |
| **Status**           | Final                      |

---

## 1. Tujuan

Dokumen ini mencatat **seluruh data uji** yang digunakan selama pengujian
SauceDemo. Data uji yang terdokumentasi memastikan testing dapat
direproduksi dan konsisten.

---

## 2. Data User (Credentials)

SauceDemo menyediakan 6 tipe user dengan karakteristik berbeda.
Semua user memiliki password yang sama: `secret_sauce`.

| No  | User Type               | Username                  | Password       | Expected Behavior                          |
| --- | ----------------------- | ------------------------- | -------------- | ------------------------------------------ |
| 1   | Standard User           | `standard_user`           | `secret_sauce` | Login sukses, semua fitur normal           |
| 2   | Locked Out User         | `locked_out_user`         | `secret_sauce` | Login gagal, pesan "locked out"            |
| 3   | Problem User            | `problem_user`            | `secret_sauce` | Login sukses, beberapa UI bermasalah       |
| 4   | Performance Glitch User | `performance_glitch_user` | `secret_sauce` | Login sukses tapi lambat (>5 detik)        |
| 5   | Error User              | `error_user`              | `secret_sauce` | Login sukses, beberapa aksi memicu error   |
| 6   | Visual User             | `visual_user`             | `secret_sauce` | Login sukses, beberapa elemen tampil salah |

### 2.1 Data Invalid (untuk Negative Testing)

| No  | Username        | Password         | Expected Result                            |
| --- | --------------- | ---------------- | ------------------------------------------ |
| 1   | `standard_user` | `wrong_password` | Error "Username and password do not match" |
| 2   | `wrong_user`    | `secret_sauce`   | Error "Username and password do not match" |
| 3   | `wrong_user`    | `wrong_password` | Error "Username and password do not match" |
| 4   | (kosong)        | (kosong)         | Error "Username is required"               |
| 5   | `standard_user` | (kosong)         | Error "Password is required"               |
| 6   | (kosong)        | `secret_sauce`   | Error "Username is required"               |

---

## 3. Data Produk

SauceDemo memiliki 6 produk. Data berikut menjadi acuan pengujian
inventory, cart, dan checkout.

| No  | Product Name                      | Price (USD) |
| --- | --------------------------------- | ----------- |
| 1   | Sauce Labs Backpack               | $29.99      |
| 2   | Sauce Labs Bike Light             | $9.99       |
| 3   | Sauce Labs Bolt T-Shirt           | $15.99      |
| 4   | Sauce Labs Fleece Jacket          | $49.99      |
| 5   | Sauce Labs Onesie                 | $7.99       |
| 6   | Test.allTheThings() T-Shirt (Red) | $15.99      |

**Total jika semua produk dibeli:** $129.94

---

## 4. Data Checkout

| Field       | Nilai Valid | Nilai Invalid           |
| ----------- | ----------- | ----------------------- |
| First Name  | `Reyka`     | (kosong)                |
| Last Name   | `Raihan`    | (kosong)                |
| Postal Code | `12345`     | (kosong), `ABC`, `!@#$` |

### 4.1 Skenario Perhitungan Harga

**Contoh:** Beli 1 produk (Backpack $29.99)

| Komponen  | Nilai      |
| --------- | ---------- |
| Subtotal  | $29.99     |
| Tax (8%)  | $2.40      |
| **Total** | **$32.39** |

> **Catatan:** Tarif pajak mungkin berbeda tiap region. Dokumentasikan
> nilai aktual saat eksekusi jika berbeda.

---

## 5. Data Sorting

| Opsi Sorting        | Expected Order                                                                                                                     |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| Name (A to Z)       | Backpack, Bike Light, Bolt T-Shirt, Fleece Jacket, Onesie, Test.allTheThings() T-Shirt                                             |
| Name (Z to A)       | Test.allTheThings() T-Shirt, Onesie, Fleece Jacket, Bolt T-Shirt, Bike Light, Backpack                                             |
| Price (low to high) | Onesie ($7.99), Bike Light ($9.99), Bolt T-Shirt ($15.99), Test.allTheThings() ($15.99), Backpack ($29.99), Fleece Jacket ($49.99) |
| Price (high to low) | Fleece Jacket ($49.99), Backpack ($29.99), Bolt T-Shirt ($15.99), Test.allTheThings() ($15.99), Bike Light ($9.99), Onesie ($7.99) |

> **Catatan:** Untuk dua produk dengan harga sama ($15.99),
> urutan bisa bervariasi - catat sebagai _tie_.

---

## 6. Data Environment

Detail environment lengkap tersedia di
[`../07-references/environment.md`](../07-references/environment.md).

| Item          | Nilai                         |
| ------------- | ----------------------------- |
| Browser Utama | Google Chrome (latest stable) |
| Resolusi      | 1920 x 1080                   |
| URL           | https://www.saucedemo.com     |

---

## 7. Aturan Penggunaan Data

1. **Jangan menggunakan data user real** - hanya data dari SauceDemo.
2. **Reset sesi** (logout + clear cache) sebelum mengganti user type.
3. **Catat data aktual** jika berbeda dari yang terdokumentasi.
4. **Update dokumen ini** jika menemukan data baru selama testing.

---

## 8. Approval

| Nama                   | Peran       | Tanggal    | Tanda Tangan |
| ---------------------- | ----------- | ---------- | ------------ |
| Reyka Mochammad Raihan | QA Engineer | 2026-09-30 | ✅           |

---

_Terakhir diperbarui: 2026-09-30_
