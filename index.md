# Kebijakan Privasi — Absensi Tura

**Berlaku sejak:** 12 Juni 2026
**Versi:** 1.0
**Pengendali Data:** PT Tura Group Indonesia

---

## 1. Pendahuluan

Aplikasi **Absensi Tura** ("Aplikasi") adalah aplikasi internal milik PT Tura Group Indonesia ("Perusahaan", "kami") yang digunakan oleh karyawan untuk melakukan absensi masuk dan keluar.

Kebijakan ini menjelaskan data apa yang kami kumpulkan, bagaimana digunakan, dan hak Anda sebagai pengguna.

Aplikasi ini hanya diperuntukkan bagi karyawan PT Tura Group yang sudah terdaftar di sistem HCIS internal. Bukan untuk publik umum.

---

## 2. Data yang Dikumpulkan

### 2.1 Data Identitas (dari sistem HCIS Perusahaan)
- Nama lengkap
- Nomor Registrasi Pegawai (NRP)
- Email perusahaan
- Foto profil (kalau ada)
- Jabatan, departemen, lokasi kerja

### 2.2 Data Lokasi (saat absen)
- Koordinat GPS (latitude, longitude) saat Anda menekan tombol absen
- Hanya diakses saat Anda aktif menekan tombol absen, **bukan tracking terus-menerus**
- Digunakan untuk verifikasi geofence (memastikan Anda berada di area kantor/site yang sah)

### 2.3 Data Kamera (foto selfie absen)
- Foto wajah Anda (selfie) saat menekan tombol absen
- Diambil dari kamera depan, **bukan dari galeri** (anti-curang)
- Disimpan di server Perusahaan sebagai bukti kehadiran

### 2.4 Data Perangkat
- Device ID (UUID acak yang dibuat saat install)
- Nama perangkat (mis. "Samsung A52")
- Versi sistem operasi
- Versi aplikasi
- Token sesi login (untuk autentikasi)

### 2.5 Data Aktivitas (log)
- Riwayat absen masuk/keluar (tanggal, waktu, lokasi, sesi)
- Log error teknis: kode HTTP, pesan error, waktu kejadian (untuk membantu tim IT debug masalah)
- **Tidak termasuk** foto, password, atau data sensitif

---

## 3. Cara Data Digunakan

| Tujuan | Data yang dipakai |
|---|---|
| Verifikasi identitas saat login | NRP/email + password |
| Validasi geofence absen | GPS koordinat + foto selfie |
| Pencatatan kehadiran | Tanggal, waktu, lokasi, foto |
| Penghitungan gaji & cuti | Riwayat absen dari HCIS |
| Debug & pelaporan teknis | Log error, info perangkat |
| Notifikasi update aplikasi | Versi aplikasi yang ter-install |

Data **TIDAK** digunakan untuk:
- Iklan
- Tracking lokasi di luar momen absen
- Dijual atau dibagikan ke pihak ketiga komersial
- Analytics behavior di luar konteks absensi

---

## 4. Pihak Ketiga

Aplikasi mengakses layanan pihak ketiga berikut:

| Layanan | Tujuan | Data yang diakses |
|---|---|---|
| **Google Play Services** | Auto-update aplikasi via Play Store, location services (GPS) | Versi aplikasi, koordinat GPS saat aktif |
| **Server internal Tura (sim.tura.group)** | Penyimpanan & sinkronisasi data absen | Semua data di atas |

**Tidak ada** layanan analytics pihak ketiga (Firebase Analytics, Google Analytics, Facebook SDK, dll).

---

## 5. Penyimpanan & Keamanan

- **Lokasi server:** server internal PT Tura Group di Indonesia
- **Enkripsi saat transit:** semua komunikasi via HTTPS (TLS 1.2+)
- **Enkripsi saat istirahat:** token login disimpan di Android Keystore / iOS Keychain (enkripsi level OS)
- **Foto absen:** disimpan di storage server perusahaan dengan akses terbatas (hanya HR & IT)
- **Periode penyimpanan:** sesuai kebijakan retensi HR PT Tura Group (umumnya 5 tahun untuk data ketenagakerjaan, sesuai regulasi pajak Indonesia)

---

## 6. Pihak yang Berhak Mengakses Data

| Pihak | Akses |
|---|---|
| **Karyawan (Anda)** | Data Anda sendiri (riwayat absen, profil) |
| **HRBP (HR Business Partner)** | Data semua karyawan untuk kepentingan administrasi gaji & kepatuhan jam kerja |
| **IT Internal** | Log teknis (tanpa foto) untuk debug & maintenance |
| **Manajemen** | Laporan agregat (tanpa data personal terkait) |
| **Pemerintah / Hukum** | Hanya jika ada permintaan resmi (panggilan pengadilan, audit pajak) |

---

## 7. Hak Anda

Sebagai pengguna Aplikasi, Anda berhak:

1. **Mengakses data:** lihat riwayat absen Anda via aplikasi atau request ke HRBP
2. **Memperbarui data:** koreksi data identitas via HRBP
3. **Menghapus data:** request hapus akun setelah Anda tidak lagi menjadi karyawan (data kehadiran tetap disimpan sesuai retensi pajak)
4. **Menarik persetujuan:** uninstall aplikasi setiap saat. Data lokal di HP akan terhapus. Data server tetap sesuai retensi HR.
5. **Mengajukan keluhan:** kontak DPO Perusahaan (lihat bagian Kontak)

---

## 8. Izin Aplikasi (Android Permissions)

| Permission | Kapan diminta | Tujuan |
|---|---|---|
| `ACCESS_FINE_LOCATION` | Saat absen | Validasi geofence kantor/site |
| `ACCESS_COARSE_LOCATION` | Saat absen | Backup kalau GPS tidak presisi |
| `CAMERA` | Saat absen | Selfie verifikasi |
| `INTERNET` | Selalu | Sinkronisasi data ke server |
| `ACCESS_NETWORK_STATE` | Selalu | Deteksi koneksi (untuk offline queue) |
| `WAKE_LOCK` | Saat sync background | Memastikan absen offline berhasil ter-upload |

Permission diminta saat fitur pertama kali digunakan, **bukan otomatis saat install**. Anda bisa menolak — namun fitur terkait tidak akan berfungsi (mis. tidak bisa absen tanpa lokasi + kamera).

---

## 9. Anak-anak

Aplikasi ini diperuntukkan bagi karyawan PT Tura Group yang berusia minimum 18 tahun. Kami tidak secara sengaja mengumpulkan data dari anak-anak di bawah 18 tahun.

---

## 10. Perubahan Kebijakan

Kami dapat memperbarui kebijakan ini sewaktu-waktu. Versi terbaru selalu tersedia di URL yang sama. Perubahan material akan dinotifikasi via aplikasi atau email perusahaan.

---

## 11. Kontak

Untuk pertanyaan, keluhan, atau permintaan terkait data pribadi Anda:

- **Email:** willie@tura.tech
- **Perusahaan:** PT Tura Teknologi Informasi
- **Alamat:**
  Gedung Menara Karya Lt. 28
  Jl. H. R. Rasuna Said Blok X-5 Kav. 1-2
  Kuningan Timur, Setiabudi
  Jakarta Selatan 12950

---

*Dokumen ini dibuat untuk memenuhi persyaratan Google Play Store dan praktik perlindungan data karyawan sesuai UU PDP No. 27 Tahun 2022.*
