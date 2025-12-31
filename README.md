# 📊 Sistem Bendahara Desktop

Sistem Bendahara Desktop adalah aplikasi berbasis **VB.NET** dengan database **SQLite (ODBC)** yang digunakan untuk mengelola data keuangan bendahara secara **offline**, termasuk penyimpanan bukti transaksi berupa foto dan ekspor data ke Excel.

Aplikasi ini dirancang untuk penggunaan internal (ORGANISASI) dan **tidak memerlukan koneksi internet**.

---

## 🚀 Fitur Utama
- Input, edit, dan hapus data keuangan
- Upload & simpan foto bukti transaksi (nota)
- Database SQLite (ringan & portable)
- Export laporan ke Excel
- Berjalan secara offline
- Struktur folder sederhana & mudah di-backup

---

## 🖥️ Spesifikasi & Kebutuhan Sistem
- Windows 10 / Windows 11
- Arsitektur aplikasi: **32-bit (x86)**
- SQLite ODBC Driver **32-bit**
- Tidak memerlukan Microsoft Access / SQL Server

---

## 🔧 Panduan Instalasi (WAJIB)

### 1️⃣ Install SQLite ODBC Driver 32-bit
Aplikasi ini menggunakan **SQLite melalui ODBC**, sehingga driver **WAJIB di-install**.

Install driver di folder "Requirement Here !"
Pilih salah satu file berikut:
- `sqliteodbc_w32.exe`
- `sqliteodbc_w32.exe`

⚠️ Pastikan **32-bit (x86)**  
⚠️ Jangan install versi `w64`

---

### 2️⃣ Verifikasi Driver SQLite ODBC
Setelah instalasi, lakukan pengecekan:

1. Tekan **Win + R**
2. Jalankan: C:\Windows\SysWOW64\odbcad32.exe
3. Masuk ke tab **Drivers**
4. Pastikan terdapat salah satu driver berikut:
   - `SQLite3 ODBC Driver`
   - atau `SQLite ODBC Driver`

Jika driver tidak muncul, berarti instalasi belum benar.

---

### 3️⃣ Menjalankan Aplikasi
Jalankan aplikasi dengan cara:
- Double-click `Aplikasi Bendahara HMTRPL.exe`

⚠️ Jangan memindahkan file `.exe` tanpa database dan folder `nota`.

---

## 📁 Struktur File & Folder
| File / Folder | Fungsi |
|--------------|--------|
| `Aplikasi Bendahara HMTRPL.exe` | File utama aplikasi |
| `bendahara.db` | Database SQLite |
| `nota/` | Penyimpanan foto bukti transaksi |

---

## 🛡️ Tentang Deteksi Antivirus (IMPORTANT)
Beberapa antivirus **dapat mendeteksi aplikasi ini sebagai suspicious**.  
Hal ini **BUKAN virus** dan merupakan **false positive**.

### Penyebab umum:
- Aplikasi memiliki akses **Read / Write / Execute (RWX)**
- Aplikasi menyimpan file gambar ke folder lokal
- Database bersifat writable
- Aplikasi tidak menggunakan digital signature

Perilaku tersebut umum pada aplikasi desktop internal dan sering disalahartikan oleh antivirus.

---

### ✅ Solusi yang Disarankan
- Tambahkan folder aplikasi ke **Antivirus Exclusion**
- Gunakan installer resmi (Inno Setup)
- Jalankan aplikasi dari folder yang tidak dibatasi permission

Aplikasi ini **TIDAK mengandung malware, trojan, spyware, ataupun backdoor**.

---

## ⚙️ Informasi Teknis (Developer)
- Bahasa: VB.NET
- Database: SQLite (ODBC, DSN-less)
- Build Mode: `Release | x86`
- Path database menggunakan: Application.StartupPath

---

## 📦 Catatan Distribusi
- Gunakan installer untuk deployment ke PC lain
- Pastikan SQLite ODBC Driver 32-bit sudah terinstall di PC target
- Lakukan backup rutin terhadap file `bendahara.db`
- Jangan rename atau memindahkan folder `nota`

---

## 🧪 Troubleshooting Singkat
**Error IM002 (ODBC Driver Not Found):**
- Pastikan SQLite ODBC Driver **32-bit** terinstall
- Pastikan nama driver di code sesuai dengan yang ada di ODBC Manager
- Pastikan aplikasi dibuild dalam mode **x86**

---

## ✨ Penutup
Sistem Bendahara Desktop dibuat untuk membantu pencatatan keuangan secara sederhana, cepat, dan offline.  
Pastikan instalasi dilakukan sesuai panduan agar aplikasi berjalan stabil di semua PC.

Happy managing 💸📈
