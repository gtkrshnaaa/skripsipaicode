The entire project is written in Indonesian.

# Skripsi – Paicode: Agentic AI berbasis CLI untuk Bantu Proses Coding

Repo ini memuat dua hal utama:

- Objek penelitian: aplikasi CLI agentic AI bernama `Pai Code` (direktori `paicode/`).
- Naskah skripsi LaTeX lengkap beserta Makefile (direktori `skripsi_latex/`).

Tujuan repo: menyediakan satu tempat terpadu untuk kode sumber dan naskah skripsi sehingga pengembangan, dokumentasi, dan kompilasi PDF berjalan end-to-end di Ubuntu.

## Struktur Repo

* `paicode/` → source code project (objek penelitian `Pai Code`).
* `skripsi_latex/` → seluruh berkas LaTeX skripsi dan Makefile.
  * `skripsi_latex/dist/` → artefak kompilasi (aux, log, bbl, dll.).
  * `skripsi_latex/skripsipdf/` → PDF akhir (mis. `skripsigtkrshnaaa.pdf`).
* `reference/` → referensi ilmiah (PDF jurnal, buku, artikel) untuk sitasi.
* `skripsiguide.md` → panduan penyusunan skripsi.

## Prasyarat (Ubuntu)

Pastikan paket LaTeX tersedia:

```bash
sudo apt update
sudo apt install -y \
  texlive-latex-recommended \
  texlive-latex-extra \
  texlive-fonts-recommended \
  texlive-lang-other \
  texlive-bibtex-extra \
  texlive-science \
  latexmk \
  make
```

## Aturan Penulisan Skripsi

* Bahasa: **Indonesia baku formal akademik**.
* Format: **LaTeX** dengan struktur bab standar kampus Indonesia.
* Hindari kata ganti orang pertama. Gunakan bentuk pasif bila memungkinkan.
* Referensi harus berasal dari folder `reference/` atau sumber akademik lain (Google Scholar, IEEE, dll).
* Sitasi wajib pakai **BibTeX** (`daftar_pustaka.bib`).

## Struktur Skripsi

### Bab I – Pendahuluan

* **Latar belakang** → alasan dibuatnya paicode, permasalahan coding manual, relevansi dengan AI agent dan CLI, serta penegasan bahwa Paicode melakukan **operasi berkas tingkat-aplikasi di workspace proyek** dan integrasi **LLM via API** (dengan guardrail \_path security_ dan perubahan berbasis \_diff_).
* **Rumusan masalah** → contoh: bagaimana merancang dan mengimplementasikan agentic AI berbasis CLI yang dapat membantu proses coding secara interaktif.
* **Batasan masalah** → contoh: hanya mendukung Python/Unix environment, bergantung pada LLM eksternal, belum support multi-user.
* **Tujuan penelitian**.
* **Manfaat penelitian** (akademis & praktis).

### Bab II – Tinjauan Pustaka

* **Teori dasar**: Command Line Interface, AI Agent, LLM, \_path security\_, perubahan berbasis \_diff\_, Poetry.
* **Penelitian terkait**: ringkasan jurnal/skripsi tentang AI coding assistant atau agentic AI.
* **Posisi penelitian**: bandingkan paicode dengan penelitian/alat yang sudah ada.

### Bab III – Metodologi Penelitian

* **Metode pengembangan sistem** → tentukan model (prototyping, waterfall, agile, research & development).
* **Arsitektur paicode** → jelaskan modul `agent.py`, `llm.py`, `fs.py`, `cli.py`. Bisa gunakan diagram alur atau class diagram.
* **Tools yang digunakan** → Python, Poetry, Git, LLM API.

### Bab IV – Implementasi dan Hasil

* **Implementasi paicode** → step instalasi, konfigurasi API key, alur interaksi CLI.
* **Contoh sesi interaktif** → sertakan screenshot atau listing dari README.
* **Evaluasi** → uji coba dengan skenario coding tertentu, bandingkan dengan manual atau tools lain.

### Bab V – Kesimpulan dan Saran

* **Kesimpulan** → apakah paicode berhasil membantu coding dengan AI agent di CLI.
* **Saran** → pengembangan lanjut seperti multi-LLM support, integrasi editor, dsb.

## Integrasi Project Paicode

* Source code paicode di folder `paicode/` menjadi objek utama penelitian.
* Potongan kode penting disisipkan dalam skripsi menggunakan LaTeX `lstlisting`.
* Struktur project bisa ditampilkan dengan `verbatim` atau `tree`.

## Quickstart Paicode (Singkat)

Untuk penggunaan aplikasi Paicode, lihat panduan lengkap di `paicode/README.md`. Ringkasan langkah:

```bash
# Instal dependensi (dari root repo)
cd paicode
poetry install

# Set API key Gemini (sekali saja)
poetry run pai config --set YOUR_API_KEY

# Mulai sesi interaktif agen
poetry run pai
```

Catatan penting:

- Paicode menjalankan **operasi berkas tingkat-aplikasi di workspace proyek**, bukan pengelola file system OS.
- Inferensi dilakukan oleh **LLM eksternal via API**; patuhi kebijakan privasi penyedia.
- Diterapkan **path security** (blokir path sensitif) dan **perubahan berbasis diff** untuk mengurangi risiko penimpaan besar yang tidak diinginkan.

## Alur Kerja Pembuatan Skripsi

1. Baca file ini (`skripsiguide.md`) sebelum menulis.
2. Tulis tiap bab ke file `.tex` terpisah di `skripsi_latex/`.
3. Update `main.tex` agar semua bab masuk.
4. Gunakan referensi dari folder `reference/` untuk sitasi.
5. Update `daftar_pustaka.bib` bila ada sumber baru.
6. Kompilasi LaTeX jadi PDF (`skripsi.pdf`).

## Gaya Penulisan

* Konsisten formal akademik.
* Hindari bahasa sehari-hari.
* Hindari kata ganti pribadi.

## Kompilasi

Kompilasi skripsi dilakukan dari direktori `skripsi_latex/` menggunakan Makefile. Pastikan dependensi LaTeX di Ubuntu telah terpasang:

```bash
sudo apt update
sudo apt install -y \
  texlive-latex-recommended \
  texlive-latex-extra \
  texlive-fonts-recommended \
  texlive-lang-other \
  texlive-bibtex-extra \
  texlive-science \
  latexmk \
  make
```

Build dan hasil keluaran:

```bash
cd skripsi_latex

# build PDF (artefak ke dist/, PDF final ke skripsipdf/skripsigtkrshnaaa.pdf)
make pdf

# bersihkan file bantu (dist/ tetap ada, PDF aman)
make clean

# hapus folder build (dist/) saja
make distclean

# hapus dist/ dan folder PDF (gunakan hati-hati)
make clobber
```

Lokasi hasil:

- PDF final: `skripsi_latex/skripsipdf/skripsigtkrshnaaa.pdf`
- Artefak build: `skripsi_latex/dist/`

Jika ada error, cek `main.log`.

---