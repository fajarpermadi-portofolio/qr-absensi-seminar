📄 README - SISTEM ABSENSI QR & DISTRIBUSI QR KE WHATSAPP

📌 DESKRIPSI PROGRAM

Sistem ini terdiri dari dua bagian utama:

1. kirim_wa_qr.exe — Untuk membuat QR Code berdasarkan data dari Google Spreadsheet dan mengirimkannya otomatis ke nomor WhatsApp peserta.
2. scan_absensi.exe — Untuk mencatat kehadiran peserta (Check-in dan Check-out) menggunakan QR Code.

Semua program ini dapat dijalankan langsung di Windows tanpa perlu menginstal Python, asalkan semua file pendukung tetap di folder yang sama.

---

✅ FITUR UTAMA

📌 kirim_wa_qr.exe
- Mengambil data peserta dari Google Spreadsheet (hasil Google Form)
- Membuat QR Code berdasarkan NPM, Nama, dan Jurusan
- Menyimpan QR di folder qr_peserta/
- Mengirim QR dan pesan otomatis ke WhatsApp peserta via browser
- Format nomor otomatis diperbaiki (08xxx → +628xxx)

📌 scan_absensi.exe
- Scan QR Code dari kamera laptop
- Mode Check-in dan Check-out bisa diganti manual
- Data absensi langsung tersimpan ke Google Spreadsheet
- Tampil log kehadiran, waktu scan, dan detail peserta
- Fitur ekspor ke Excel dan lihat daftar langsung di aplikasi

---

🖥 CARA MENJALANKAN PROGRAM

📍 Untuk kirim_wa_qr.exe:
1. Pastikan file credentials.json dan koneksi internet tersedia
2. Login ke WhatsApp Web di browser default
3. Jalankan kirim_wa_qr.exe
4. Program akan:
   - Membuat QR setiap peserta
   - Membuka WhatsApp Web secara otomatis
   - Mengirim pesan + QR 

📍 Untuk scan_absensi.exe:
1. Pastikan koneksi internet aktif
2. Buka folder program
3. Jalankan scan_absensi.exe
4. Tekan tombol:
   - Mulai Kamera → buka kamera laptop
   - Ubah Mode → Check-in ↔ Check-out
   - Export ke Excel → simpan kehadiran lokal
5. Arahkan QR peserta ke kamera → data akan otomatis tercatat

---

📂 KONFIGURASI SPREADSHEET & AKSES GOOGLE

Agar program dapat berjalan dengan spreadsheet buatan sendiri, ikuti langkah berikut:

1. Buat spreadsheet Google dengan kolom:
   - NPM
   - NAMA
   - JURUSAN
   - NOMOR HP
   - Check-in
   - Check-out
BESAR DAN KECIL HURUF HARUS SAMA PERSIS !!!

2. Klik tombol **Bagikan** di spreadsheet
3. Masukkan email berikut sebagai Editor:
   **seminar-bot@nodal-keep-462715-i2.iam.gserviceaccount.com**
4. Simpan file `credentials.json` yang diberikan (isi API key/akun layanan)
5. Letakkan file `credentials.json` di folder yang sama dengan program .exe
6. Samakan nama spreadsheet yang ada di config.json (contoh di config.json bawaan adalah "tes") menjadi nama spreadsheet yang kamu buat dengan tetap memakai tanda petik " "

Program akan otomatis terhubung ke spreadsheet yang kamu buat sendiri selama:
- Nama spreadsheet dan index worksheet benar (diatur di config.json)
- Akses diberikan ke service account di atas

---

⚠️ CATATAN PENTING

- File credentials.json harus berada di folder yang sama dengan .exe
- Jangan ubah nama file .exe atau file .dll yang disertakan
- Pastikan webcam aktif dan tidak digunakan oleh aplikasi lain
- Nomor WhatsApp peserta harus valid dan tanpa spasi, diawali dengan 08 atau 62
- WhatsApp Web harus tetap terbuka saat kirim QR (tidak boleh disentuh sama sekali)

---


🧑‍💻 DIBUAT OLEH:  
Ahmad Fajar Permadi  
Juni 2025
