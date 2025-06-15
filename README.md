# 📷 Sistem QR Absensi Seminar & Pengiriman QR WhatsApp

Proyek ini mencakup sistem otomatis **pembuatan dan pengiriman QR Code ke peserta melalui WhatsApp**, serta **pencatatan kehadiran (Check-in & Check-out)** melalui pemindaian QR Code saat hari-H acara.

---

## 📌 Fitur Utama

### 🧾 kirim_wa_qr.py
- Ambil data peserta dari Google Spreadsheet (hasil Google Form)
- Buat QR Code untuk setiap peserta berdasarkan NPM, Nama, dan Jurusan
- Simpan QR ke folder `qr_peserta/`
- Kirim QR via WhatsApp Web ke peserta secara otomatis

### 🟩 scan_absensi.py
- Scan QR Code peserta melalui kamera laptop
- Tersedia mode Check-in & Check-out
- Data kehadiran langsung dicatat ke Google Spreadsheet
- Tampilkan log pemindaian secara real-time
- Bisa **export ke Excel**
- GUI sederhana untuk kemudahan penggunaan

---

## 📁 Struktur Folder
qr-absensi-seminar/
├── kirim_wa_qr.py
├── scan_absensi.py
├── config.json
├── credentials.json
├── .gitignore
├── README.md
├── qr_peserta/

📄 Format Spreadsheet
Agar program bisa berjalan, spreadsheet kamu wajib memiliki kolom berikut:
NPM | NAMA | JURUSAN | NOMOR HP | Check-in | Check-out
-Beri akses ke spreadsheet kamu ke service account:
-seminar-bot@nodal-keep-462715-i2.iam.gserviceaccount.com

🖥️ Menjalankan Program
Syarat:
-WhatsApp Web harus aktif di browser default
-Jangan tutup tab browser sebelum semua QR dikirim
-Nomor HP di spreadsheet harus valid (format: 08xxxx / 62xxxx)

📌 Untuk absensi (Scan QR):
-Jalankan program
-Klik Mulai Kamera
-Klik Ubah Mode (Check-in ↔ Check-out)
-Arahkan QR peserta ke kamera
-Klik Export ke Excel jika ingin menyimpan salinan lokal


🧑‍💻 Developer
Ahmad Fajar Permadi
Juni 2025
GitHub Portofolio



