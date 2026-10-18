# Belajar Tajwid

Aplikasi web ringan untuk belajar hukum tajwid Al-Quran dalam bahasa Indonesia. Terdiri dari materi ringkas yang disertai contoh teks Arab, dan latihan pilihan ganda untuk menguji pemahaman. Berjalan langsung di browser tanpa instalasi, tanpa backend, dan tanpa dependensi.

## Fitur

- **Materi per bab**: Nun Sukun & Tanwin, Mim Sukun, Mad, serta Qalqalah, Ghunnah & Lam Jalalah.
- **Contoh bacaan** berharakat dengan keterangan hukum yang berlaku.
- **Latihan 10 soal** pilihan ganda dengan penjelasan jawaban.
- **Progres belajar** (bab selesai dan skor terbaik) tersimpan otomatis di browser lewat `localStorage`.
- **Responsif** untuk ponsel dan desktop, mendukung mode terang dan gelap.

## Cara Menjalankan

1. Clone repositori ini.
2. Buka `belajar-tajwid.html` langsung di browser, atau sajikan lewat server statis apa pun.

```bash
git clone https://github.com/aalfath7/belajar-tajwid.git
cd belajar-tajwid
# buka belajar-tajwid.html di browser
```

Koneksi internet hanya dibutuhkan untuk memuat font Arab **Amiri** dari Google Fonts. Tanpa koneksi, teks Arab tetap tampil memakai font bawaan sistem.

## Struktur

```
.
├── belajar-tajwid.html   # seluruh aplikasi (HTML, CSS, JS)
└── README.md
```

Materi dan soal latihan disimpan sebagai data di dalam berkas HTML (konstanta `T` untuk materi dan `Q` untuk soal), sehingga mudah ditambah atau diubah.

## Menambah Materi atau Soal

- **Materi baru**: tambahkan objek pada array `T` dengan format `{id, title, intro, rules:[{n, l, d, ar, e}]}`.
- **Soal baru**: tambahkan pada array `Q` dengan format `[pertanyaan, [pilihan], indeksJawabanBenar, penjelasan]`.

## Catatan Penting

Aplikasi ini hanyalah alat bantu belajar. Tajwid tidak bisa dipelajari hanya dari layar: pelajari dengan **talaqqi** (membaca langsung di hadapan guru yang sanadnya jelas). Penentuan panjang mad, khususnya Mad Jaiz Munfasil, mengikuti bacaan yang diajarkan gurumu. Jika menemukan kekeliruan materi, silakan buka _issue_ atau _pull request_.

## Rencana Pengembangan

- [ ] Materi tambahan: hukum Ra, Alif Lam (Qamariyah/Syamsiyah), waqaf dan ibtida’
- [ ] Mode hafalan huruf makhraj dan sifat huruf
- [ ] Audio contoh bacaan
- [ ] Kumpulan soal yang lebih banyak dan acak

## Kontribusi

Kontribusi sangat diterima, terutama koreksi materi dari guru atau pengajar Al-Quran. Silakan _fork_, buat cabang baru, lalu ajukan _pull request_.

## Lisensi

Tentukan lisensi sesuai kebutuhanmu (misalnya MIT) dan tambahkan berkas `LICENSE`.
