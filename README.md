# UAS_MOBILE-2
# 🏋️ Aplikasi Jadwal Olahraga

Aplikasi Jadwal Olahraga adalah aplikasi sederhana berbasis PHP yang membantu pengguna mengatur dan memantau aktivitas olahraga. Setiap halaman saling terhubung untuk membentuk alur penggunaan yang sederhana.

---

# Struktur File

```
├── index.php
├── home.php
├── reminder.php
├── progres.php
├── settings.php
├── selesai.php
└── style.css
```

---

## 1. index.php

### Fungsi
File utama yang dijalankan pertama kali ketika aplikasi dibuka.

### Penjelasan
- Melakukan redirect (pengalihan) secara otomatis ke halaman `home.php`.
- Tidak memiliki tampilan antarmuka.

### Alur
```
index.php
    ↓
home.php
```

---

## 2. home.php

### Fungsi
Sebagai halaman beranda (Home) aplikasi.

### Penjelasan
- Menampilkan ucapan selamat datang.
- Menjadi titik awal navigasi pengguna.
- Menyediakan tombol menuju halaman Reminder.

### Output
```
HOME

Selamat datang di Aplikasi Jadwal Olahraga

[Masuk Reminder]
```

### Alur
```
home.php
    ↓
reminder.php
```

---

## 3. reminder.php

### Fungsi
Mengingatkan pengguna mengenai jadwal olahraga.

### Penjelasan
- Menanyakan apakah pengguna sudah mengatur jadwal olahraga.
- Menyediakan dua pilihan:

#### YA
Pengguna sudah mengatur jadwal olahraga.

```
reminder.php
      ↓
progres.php
```

#### TIDAK
Pengguna belum mengatur jadwal olahraga.

```
reminder.php
      ↓
settings.php
```

### Output
```
REMINDER

Apakah kamu sudah mengatur jadwal olahraga?

[YA]
[TIDAK]
```

---

## 4. progres.php

### Fungsi
Menampilkan perkembangan olahraga pengguna.

### Penjelasan
Menampilkan data olahraga mingguan, misalnya:

- Senin : 30 menit
- Rabu : 45 menit
- Jumat : 30 menit

### Output
```
PROGRES

Progres olahraga kamu minggu ini:

- Senin : 30 menit
- Rabu : 45 menit
- Jumat : 30 menit
```

### Navigasi
Halaman ini menyediakan tombol menuju:

```
summary.php
```

> Catatan:
> File `summary.php` belum tersedia sehingga perlu dibuat agar tombol tersebut dapat digunakan.

---

## 5. settings.php

### Fungsi
Mengatur atau mengubah jadwal olahraga.

### Penjelasan
Menanyakan apakah pengguna ingin mengubah jadwal olahraga.

### Pilihan

#### YA
Kembali ke halaman Reminder.

```
settings.php
      ↓
reminder.php
```

#### TIDAK
Mengakhiri penggunaan aplikasi.

```
settings.php
      ↓
selesai.php
```

### Output
```
SETTINGS

Apakah ingin mengubah jadwal olahraga?

[YA]
[TIDAK]
```

---

## 6. selesai.php

### Fungsi
Halaman akhir aplikasi.

### Penjelasan
- Menampilkan ucapan terima kasih.
- Menyediakan tombol untuk kembali ke Home.

### Output
```
SELESAI

Terima kasih telah menggunakan Aplikasi Jadwal Olahraga

[Kembali ke Home]
```

### Alur
```
selesai.php
      ↓
home.php
```

---

## 7. style.css

### Fungsi
Mengatur tampilan seluruh halaman aplikasi.

### Pengaturan yang digunakan

### Body
- Font : Arial
- Background : abu-abu muda
- Posisi teks : tengah
- Jarak atas : 50 px

### Tombol Link (`a`)
- Warna biru
- Tulisan putih
- Sudut membulat
- Efek hover berwarna biru lebih gelap

### Fungsi Utama
Memberikan tampilan yang lebih rapi dan konsisten pada seluruh halaman.

---

# Alur Keseluruhan Sistem

```
index.php
    ↓
home.php
    ↓
reminder.php
   ├── YA ────> progres.php ────> summary.php
   │
   └── TIDAK ──> settings.php
                     │
                 YA ─┘
                     │
                 TIDAK
                     ↓
                selesai.php
                     ↓
                home.php
```

---

# Teknologi yang Digunakan

- HTML
- CSS
- PHP

---

# Author

Muhamad Valentino Ramzi

Program Studi Teknik Informatika
Universitas Pelita Bangsa
