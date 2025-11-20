# 🎓 Presentasi Sidang Skripsi Paicode

Presentasi lengkap untuk sidang skripsi dengan **16 slide profesional** yang mencakup semua aspek penelitian.

## 📋 Struktur Slide Lengkap

| No | File | Judul | Kategori | Keterangan |
|----|------|-------|----------|------------|
| 1 | `slide01_cover.html` | Cover | Opening | Judul & identitas |
| 2 | `slide02_agenda.html` | Agenda Presentasi | Opening | Struktur presentasi (8 bagian) |
| 3 | `slide03_latar_belakang.html` | Latar Belakang | Pendahuluan | Motivasi & konteks penelitian |
| 4 | `slide04_rumusan_masalah.html` | Rumusan Masalah | Pendahuluan | 4 rumusan masalah utama |
| 5 | `slide05_tujuan.html` | Tujuan Penelitian | Pendahuluan | 4 tujuan penelitian |
| 6 | `slide06_tinjauan_pustaka.html` | Tinjauan Pustaka | Teori | Teori dasar & posisi penelitian |
| 7 | `slide07_arsitektur_single_shot.html` | **Arsitektur Single‑Shot Intelligence** ⭐ | Metodologi | **KUNCI: Kontribusi utama** |
| 8 | `slide08_komponen_sistem.html` | Komponen Sistem | Metodologi | 6 modul utama & alur data |
| 9 | `slide09_fitur_utama.html` | **Fitur Utama** ⭐ | Fitur | **KUNCI: 6 fitur unggulan** |
| 10 | `slide10_path_security.html` | Path Security & Diff-Aware | Keamanan | Deny-list & threshold 500 baris |
| 11 | `slide11_implementasi.html` | Implementasi | Teknis | Teknologi, instalasi, konfigurasi |
| 12 | `slide12_demo.html` | Demo & Skenario | Demo | 5 skenario pengujian |
| 13 | `slide13_hasil_evaluasi.html` | **Hasil Evaluasi** ⭐ | Hasil | **KUNCI: Ringkasan metrik evaluasi (netral)** |
| 14 | `slide14_kesimpulan.html` | Kesimpulan | Penutup | 7 poin kesimpulan |
| 15 | `slide15_saran.html` | Saran Pengembangan | Penutup | 10 saran pengembangan lanjutan |
| 16 | `slide16_penutup.html` | Terima Kasih & Q&A | Closing | Ringkasan & sesi tanya jawab |

## 🚀 Cara Menggunakan

### Opsi 1: Mulai dari Index
```bash
# Buka di browser
open index.html
# atau
firefox index.html
```

### Opsi 2: Langsung ke Slide Pertama
```bash
open slide01_cover.html
```

### Navigasi
- **Keyboard**: Tekan `←` untuk kembali, `→` untuk lanjut
- **Mouse**: Klik tombol navigasi di setiap slide
- **Quick Jump**: Gunakan `index.html` untuk melompat ke slide tertentu

## ✨ Fitur Presentasi

### Desain & UI
- ✅ **Responsive design** - Tampil sempurna di layar apapun
- ✅ **Modern UI** dengan Tailwind CSS & gradient backgrounds
- ✅ **Smooth animations** & transitions
- ✅ **Custom color scheme**: Primary (#2C32C5), Accent (#E9C537)
- ✅ **Typography**: Unbounded (display) + Inter (body)

### Interaktivitas
- ✅ **Keyboard navigation** (arrow keys)
- ✅ **Progress indicator** di setiap slide (X/16)
- ✅ **Visual hierarchy** dengan warna & ukuran
- ✅ **Hover effects** pada elemen interaktif

### Konten
- ✅ Selaras dengan skripsi terbaru: arsitektur **Single‑Shot Intelligence**
- ✅ **3 slide kunci** ditandai dengan ⭐
- ✅ **Visualisasi** dengan grid, tabel, dan card layout

## 🎯 Tips Presentasi Sidang

### Alokasi Waktu (~20-25 menit)
| Bagian | Slide | Waktu | Catatan |
|--------|-------|-------|---------|
| Opening | 1-2 | 1 menit | Singkat, langsung ke inti |
| Pendahuluan | 3-5 | 3 menit | Fokus pada rumusan masalah |
| Tinjauan Pustaka | 6 | 2 menit | Highlight posisi penelitian |
| **Metodologi** | **7-8** | **5 menit** | **PENTING: Jelaskan arsitektur Single‑Shot (intent → acknowledgment → planning JSON → adaptive execution → logging)** |
| **Fitur** | **9-10** | **4 menit** | **PENTING: Demo fitur-fitur unggulan** |
| Implementasi | 11 | 2 menit | Teknis singkat |
| Demo | 12 | 2 menit | Contoh interaksi |
| **Hasil** | **13** | **3 menit** | **PENTING: Ringkas metrik evaluasi secara netral** |
| Penutup | 14-16 | 3 menit | Kesimpulan & Q&A |

### Fokus Utama (Slide Kunci ⭐)
1. **Slide 7**: Arsitektur Single‑Shot Intelligence
   - Intent classification → Dynamic acknowledgment → Planning JSON → Adaptive execution (1–3 subfase) → Finalization & logging (.pai_history)
   - Penekanan: path security dan batasan diff saat eksekusi.

2. **Slide 9**: Fitur Utama
   - Single API key management (secure file, 0o600)
   - Path security (deny‑list direktori sensitif)
   - Diff‑aware `MODIFY` (threshold 500 baris, ratio 50%)
   - Session logging ke `.pai_history`
   - Interrupt handling (Ctrl+C)

3. **Slide 13**: Hasil Evaluasi
   - Ringkas metrik yang tersedia pada naskah (tanpa klaim angka lama).

### Persiapan Demo (Slide 12)
Siapkan terminal dengan:
```bash
# Jalankan Paicode
pai

# Contoh perintah untuk demo (format user):
user> buatkan program BMI Calculator dengan python
user> tampilkan struktur
user> tampilkan isi kode sumber
```

### Antisipasi Pertanyaan
1. **Bagaimana arsitektur Single‑Shot bekerja?** → Intent → acknowledgment → planning JSON → adaptive execution → logging
2. **Kenapa 500 baris threshold?** → Balance antara fokus & fleksibilitas, dapat dikonfigurasi
3. **Bagaimana dengan privasi?** → Lokal: path security, API: bergantung penyedia
4. **Perbandingan dengan Copilot/Cursor?** → CLI-based, stateful, surgical approach
5. **Bagaimana evaluasi dilakukan?** → Skenario pengujian representatif; metrik: waktu, langkah, keberhasilan build/run, kepatuhan path security, ukuran diff

## 📊 Highlight Kontribusi

### Akademis
- Arsitektur rujukan untuk agen AI berbasis CLI (Single‑Shot Intelligence)
- Metrik evaluasi sesuai naskah

### Praktis
- Alat bantu yang privacy‑aware
- Mudah diintegrasikan dengan berbagai IDE
- Open source & dapat dikembangkan

## 🎨 Customisasi

### Mengubah Warna
Edit di setiap file HTML bagian `tailwind.config`:
```javascript
colors: {
  bgdom: '#E4E5FE',    // Background
  primary: '#2C32C5',  // Warna utama
  accent2: '#E9C537',  // Warna aksen
  ink: '#252525'       // Teks
}
```

### Menambah Slide
1. Copy template dari slide yang ada
2. Update nomor slide (X/16 → X/17)
3. Update navigasi prev/next
4. Tambahkan di `index.html`

## 📁 File Lama (Diabaikan)
File-file berikut adalah versi lama dan tidak digunakan:
- `slide1.html` (diganti dengan `slide01_cover.html`)
- `slide2.html` (diganti dengan `slide02_agenda.html`)
- `slide3.html` (diganti dengan `slide03_latar_belakang.html`)

## 🔗 Navigasi Cepat

- **Mulai Presentasi**: [slide01_cover.html](slide01_cover.html)
- **Index Semua Slide**: [index.html](index.html)
- **Slide Kunci**:
  - [Slide 7: Arsitektur Single‑Shot Intelligence](slide07_arsitektur_single_shot.html)
  - [Slide 9: Fitur Utama](slide09_fitur_utama.html)
  - [Slide 13: Hasil Evaluasi](slide13_hasil_evaluasi.html)

## 📝 Checklist Sebelum Sidang

- [ ] Test semua slide di browser yang akan digunakan
- [ ] Pastikan navigasi keyboard berfungsi
- [ ] Siapkan demo live Paicode
- [ ] Hafalkan skenario & metrik yang digunakan (waktu, langkah, build/run, path security, diff)
- [ ] Siapkan jawaban untuk pertanyaan umum
- [ ] Backup: export PDF atau screenshot semua slide
- [ ] Test koneksi internet (jika ada video/demo online)

---

**Dibuat untuk**: Sidang Skripsi Paicode  
**Mahasiswa**: gtkrshnaaa  
**Program Studi**: Teknik Informatika  
**Universitas**: Universitas Teknologi Digital Indonesia  
**Tahun**: 2025

🎉 **Semoga sukses sidangnya!**
