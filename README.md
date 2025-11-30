# Travel Booking System

Sebuah proyek sistem pemesanan travel berbasis terminal yang dikembangkan sebagai bagian dari mata kuliah COSC6047 – Introduction to Programming for Business. Sistem ini memungkinkan pengguna untuk mencari, memesan, dan membatalkan penerbangan serta hotel.

## Fitur Utama

Sistem ini menyediakan menu utama dengan fungsionalitas berikut:

1. **Cari Penerbangan**
2. **Cari Hotel**
3. **Pesan Penerbangan**
4. **Pesan Hotel**
5. **Batalkan Reservasi**
6. **Lihat Semua Reservasi**
7. **Keluar**

---

## Contoh Penggunaan dan Skenario Uji

Berikut adalah ringkasan dari berbagai skenario uji (test cases) yang telah dijalankan pada sistem:

### 1. Pencarian (Cari)

| Skenario | Input | Hasil | Status |
| :--- | :--- | :--- | :--- |
| **Cari Penerbangan (Valid)** | Jakarta $\to$ Bali, 2025-01-15, 2 Penumpang | Ditemukan 2 penerbangan (Flight 101, Flight 105) | ✅ Berhasil |
| **Cari Penerbangan (Tidak Ada Hasil)** | Surabaya $\to$ Bali, 2025-01-15, 1 Penumpang | Tidak ada penerbangan tersedia. | ✅ Berhasil |
| **Cari Hotel (Valid)** | Surabaya, Check-in: 2025-01-15, Check-out: 2025-01-16, 2 Tamu | Ditemukan 2 hotel (ID 202, ID 205) | ✅ Berhasil |
| **Cari Hotel (Tidak Ada Hasil)** | Bandung, Check-in: 2025-01-15, Check-out: 2025-01-17, 2 Tamu | Tidak ada hotel tersedia di lokasi tersebut. | ✅ Berhasil |

### 2. Pemesanan (Pesan)

| Skenario | Input (ID/Nomor) | Detail Hasil | Status |
| :--- | :--- | :--- | :--- |
| **Pesan Penerbangan (Berhasil)** | No. Penerbangan: 102 | Reservasi berhasil. Diberikan **Nomor Konfirmasi: 422970**. | ✅ Berhasil |
| **Pesan Penerbangan (Gagal - Kursi)** | No. Penerbangan: 105, Jumlah: 999 | Kursi tidak mencukupi. Tersedia: 45. | ❌ Gagal |
| **Pesan Penerbangan (Gagal - ID)** | No. Penerbangan: 999 | Penerbangan dengan nomor 999 tidak ditemukan. | ❌ Gagal |
| **Pesan Hotel (Berhasil)** | ID Hotel: 202 | Reservasi berhasil. Diberikan **Nomor Konfirmasi: 196232**. | ✅ Berhasil |
| **Pesan Hotel (Gagal - ID)** | ID Hotel: 999 | Hotel dengan ID 999 tidak ditemukan. | ❌ Gagal |

### 3. Pembatalan (Batalkan Reservasi)

| Skenario | Input (Nomor Konfirmasi) | Detail Hasil | Status |
| :--- | :--- | :--- | :--- |
| **Pembatalan Reservasi (Berhasil)** | 196232 | Reservasi hotel dengan nomor konfirmasi 196232 berhasil dibatalkan. | ✅ Berhasil |
| **Pembatalan Reservasi (Gagal - ID)** | 196233 | Reservasi dengan nomor konfirmasi 196233 tidak ditemukan. | ❌ Gagal |

---

## Cara Menjalankan Program

1.  **Prasyarat:** Pastikan Anda memiliki **Java Development Kit (JDK)** terinstal.
2.  **Unduh Kode Sumber:**
    Dapatkan file proyek (misalnya, file ZIP) dari sumber yang tersedia dan ekstrak ke folder di komputer Anda (misal: `travel-booking-system`).
3.  **Akses Terminal:**
    Buka Terminal/Command Prompt dan navigasikan ke direktori utama proyek tersebut.
    ```bash
    cd [PATH_MENUJU_FOLDER_PROYEK]
    ```
4.  **Kompilasi dan Jalankan:**
    ```bash
    # Proses kompilasi (jika menggunakan Java)
    javac Main.java 
    
    # Menjalankan program
    java Main
    ```
Program akan menampilkan pesan selamat datang dan **MENU UTAMA**.

## Struktur Data (Contoh)

Data penerbangan, hotel, dan reservasi dikelola dalam struktur data yang memungkinkan pencarian dan manipulasi yang cepat.

* **Penerbangan:** 
    * Flight 101: Garuda Indonesia, Jakarta $\to$ Bali, 10:00 - 11:00, Rp 1500000.00
    * Flight 105: AirAsia, Jakarta $\to$ Bali, 14:00 - 17:00, Rp 1200000.00 (Sisa kursi: 45)
* **Hotel:** (Contoh data dari gambar)
    * Hotel ID 202: Hotel Majapahit, Surabaya, 4 bintang, Rp 1200000.00/malam
    * Hotel ID 205: Pop Hotel, Surabaya, 3 bintang, Rp 500000.00/malam

## Kontributor

Proyek ini dikerjakan oleh:

* Dewa Ayu Adellya Cahyaluna - 2802537382 
* Amira Naila Aqilah Herlambang - 2802544495
* Tegar Saksi Ilalang - 2802516434
* Tiara Rizkia Putri - 2802557844 
* Kharina Putri Amalia - 2802537281
