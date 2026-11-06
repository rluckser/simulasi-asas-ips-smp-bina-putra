# Simulasi ASAS IPS SMP Bina Putra

Website tes soal prediksi ASAS — IPS Kelas VIII, ASAS Ganjil 2026/2027,
berdasarkan kisi-kisi MGMP IPS SMP Kabupaten Lampung Tengah.

**Dibuat oleh Jelly Dharmawan S.Pd.**

- **45 soal per sesi**, waktu **120 menit** (timer hitung mundur, otomatis mengumpulkan saat habis)
- **Bank soal 90 soal**: 2 varian (A/B) untuk tiap indikator 1–45. Tiap sesi diambil 1 varian acak per indikator, lalu urutan soal diacak di dalam tiap jenis soal dan pilihan jawaban PG diacak.
- Urutan soal mengikuti kisi-kisi: Pilihan Jamak (1–25), Benar-Salah (26–30), Menjodohkan (31–35), Isian Singkat (36–40), Uraian (41–45).
- **Skor otomatis** dari 35 soal: Pilihan Jamak (25), Benar-Salah (5), Menjodohkan (5). Nilai 0–100.
- **Cek mandiri** untuk 10 soal: Isian Singkat (5) dan Uraian (5) — tampil kunci jawaban dan pembahasan, tidak masuk skor otomatis. Isian Singkat dijawab dengan satu kata atau frasa pendek.
- Menjodohkan: tiap soal menampilkan 5 pilihan, yaitu jawaban dari kelima soal Menjodohkan pada sesi itu.
- 2 soal bergambar (indikator 41 × 2 varian, diagram siklus ekonomi 4 sektor) dengan ilustrasi SVG di `assets/img/`.
- Riwayat skor tersimpan di `localStorage` perangkat siswa.

## Distribusi materi

| Materi | Soal |
|---|---|
| Kegiatan ekonomi, produksi/distribusi/konsumsi, pelaku ekonomi | 16 |
| Harga | 2 |
| Pasar | 10 |
| Lembaga keuangan | 8 |
| Perdagangan internasional | 7 |
| Transformasi ekonomi digital | 2 |

## Struktur file

```
index.html                  Halaman utama (beranda, tes, hasil)
assets/css/style.css        Gaya tampilan (tema oranye terakota-biru)
assets/js/main.js           Logika: pengacakan, timer, penilaian, riwayat
assets/data/questions.json  Bank soal gabungan (90 soal)
assets/img/ips-41-*.svg     Diagram siklus ekonomi 4 sektor (2 file)
bank/                       Bank soal per bentuk soal (sumber, sebelum digabung)
```

## Menjalankan lokal

Dari folder ini, jalankan server statis (jangan buka `index.html` langsung dari file,
karena bank soal dimuat lewat `fetch`):

```bash
python3 -m http.server 8000
```

Lalu buka http://localhost:8000 di browser.

## Publish ke GitHub Pages

1. Buat repository baru bernama `simulasi-asas-ips-smp-bina-putra`.
2. Unggah semua file di folder ini ke branch `main`, di root repository.
3. Di repository, buka **Settings → Pages**, pilih **Deploy from a branch**,
   branch `main`, folder `/ (root)`, lalu simpan.
4. Situs akan live di `https://<username>.github.io/simulasi-asas-ips-smp-bina-putra/`.
