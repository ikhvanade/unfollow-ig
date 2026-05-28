## 📖 Panduan Ekspor Data Instagram (JSON Format)

Aplikasi ini membutuhkan file data resmi dari Instagram dalam format **JSON** untuk membandingkan daftar pengikut. Ikuti langkah-langkah di bawah ini untuk mendapatkan file yang tepat:

### ⚠️ PENTING: Menghindari Masalah Data Kosong / Hilang
> **Catatan Teknis:** Jika Anda mengekspor data menggunakan filter waktu tertentu (misalnya *6 Bulan Terakhir*), server Meta hanya akan mengekspor akun yang baru berinteraksi dalam rentang waktu tersebut. Akun lama yang sudah mem-follow Anda sejak bertahun-tahun lalu **tidak akan masuk** ke dalam file `followers_1.json`. 
> 
> **Solusi Terbaik:** Sangat disarankan untuk mendownload data **Secara Terpisah** menggunakan metode di bawah ini.

---

### 🛠️ Langkah-Langkah Request Data di Meta

1. **Masuk ke Pusat Akun (Account Center)**
   * Buka aplikasi Instagram Anda, pergi ke **Profil** → **Pengaturan dan Privasi**.
   * Klik menu **Pusat Akun (Account Center)** di bagian paling atas.

2. **Pilih Menu Unduh Informasi**
   * Gulir ke bawah dan pilih **Informasi dan Izin Anda (Your Information and Permissions)**.
   * Klik pada opsi **Unduh Informasi Anda (Download Your Information)**, lalu klik **Unduh atau Transfer Informasi**.

3. **Pilih Jenis Informasi Spesifik (PENTING)**
   * Pilih akun Instagram Anda yang ingin dicek.
   * Pada pilihan jenis informasi, pilih **Informasi Spesifik (Specific Information)**.
   * Centang opsi **Pengikut dan Mengikuti (Followers and Following)**. Klik *Berikutnya*.

4. **Atur Metode dan Format File (Wajib JSON)**
   * Pilih **Unduh ke Perangkat (Download to Device)**.
   * **Format:** Ubah dari *HTML* menjadi **JSON** (Aplikasi ini tidak mendukung format HTML).
   * **Kualitas Media:** Bebas (bisa pilih *Rendah* agar proses kompresi lebih cepat).

5. **Pengaturan Rentang Waktu (Kombinasi Terbaik)**
   * **Request Pertama (Untuk Followers):** Set Rentang Tanggal ke **Semua Waktu (All Time)**. Langkah ini wajib agar seluruh daftar orang yang mem-follow Anda dari dulu tidak hilang. Klik *Buat File*.
   * **Request Kedua (Untuk Following - Opsional jika ingin filter):** Anda bisa membuat *request* baru lagi khusus untuk data *Following* dengan Rentang Tanggal **6 Bulan Terakhir** jika hanya ingin menganalisis interaksi terbaru.

6. **Unduh dan Ekstrak File**
   * Tunggu hingga proses notifikasi dari Instagram selesai (biasanya memakan waktu beberapa menit hingga email masuk).
   * Unduh file `.zip` yang diberikan oleh Instagram, lalu ekstrak di komputer atau HP Anda.

---

### 📂 File yang Dimasukkan ke Aplikasi

Setelah diestrak, cari folder bernama `connections/followers_and_following/` di dalam folder hasil ekstrak tersebut. Ambil file berikut dan masukkan ke halaman **Checker Engine**:

* **`followers_1.json`** (Berisi daftar orang yang mem-follow Anda)
* **`following.json`** (Berisi daftar orang yang Anda follow)

*Anda bisa langsung memilih atau melakukan drag & drop kedua file tersebut secara bersamaan ke dalam aplikasi.*
