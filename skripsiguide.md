** penting: file ini tidak boleh di modifikasi, hanya untuk dibaca dan di pahami **


# skripsiguide.md

## Tujuan

Panduan ini digunakan untuk menulis dan menyusun skripsi berbasis LaTeX di direktori `skripsi_latex/`. Objek penelitian adalah project **paicode** yang disertakan di repo ini.

## Struktur Repo

* `paicode/` → source code project (objek penelitian).
* `skripsi_latex/` → semua file LaTeX skripsi.
* `reference/` → berisi referensi ilmiah (PDF jurnal, buku, artikel). Gunakan untuk sitasi.
* `skripsiguide.md` → file panduan (dokumen ini).

## Aturan Penulisan Skripsi

* Bahasa: **Indonesia baku formal akademik**.
* Format: **LaTeX** dengan struktur bab standar kampus Indonesia.
* Hindari kata ganti orang pertama. Gunakan bentuk pasif bila memungkinkan.
* Referensi harus berasal dari folder `reference/` atau sumber akademik lain (Google Scholar, IEEE, dll).
* Sitasi wajib pakai **BibTeX** (`daftar_pustaka.bib`).

## Struktur Skripsi

### Bab I – Pendahuluan

* **Latar belakang** → alasan dibuatnya paicode, permasalahan coding manual, relevansi dengan AI agent, CLI, dan konsep local-first coding assistant.
* **Rumusan masalah** → contoh: bagaimana merancang dan mengimplementasikan agentic AI berbasis CLI yang dapat membantu proses coding secara interaktif.
* **Batasan masalah** → contoh: hanya mendukung Python/Unix environment, bergantung pada LLM eksternal, belum support multi-user.
* **Tujuan penelitian**.
* **Manfaat penelitian** (akademis & praktis).

### Bab II – Tinjauan Pustaka

* **Teori dasar**: Command Line Interface, AI Agent, LLM, local-first software, Poetry.
* **Penelitian terkait**: ringkasan jurnal/skripsi tentang AI coding assistant atau agentic AI.
* **Posisi penelitian**: bandingkan paicode dengan penelitian/alat yang sudah ada.

### Bab III – Metodologi Penelitian

* **Metode pengembangan sistem** → tentukan model (prototyping, waterfall, agile, research & development).
* **Arsitektur paicode** → jelaskan modul `agent.py`, `llm.py`, `workspace.py`, `cli.py`. Bisa gunakan diagram alur atau class diagram.
* **Tools yang digunakan** → Python, Poetry, Git, LLM API.

### Bab IV – Implementasi dan Hasil

* **Implementasi paicode** → step instalasi, konfigurasi API key, alur interaksi CLI.
* **Contoh sesi interaktif** → sertakan screenshot atau listing dari README.
* **Evaluasi** → uji coba dengan skenario coding tertentu, bandingkan dengan manual atau tools lain.

### Bab V – Kesimpulan dan Saran

* **Kesimpulan** → apakah paicode berhasil membantu coding dengan AI agent di CLI.
* **Saran** → pengembangan lanjut seperti multi-LLM support, integrasi editor, dsb.

### Daftar Pustaka

* Gunakan file `daftar_pustaka.bib` dan sitasi dengan `\cite{}`.

### Lampiran

* Masukkan potongan kode paicode, hasil uji coba, dan detail teknis.

## Integrasi Project Paicode

* Source code paicode di folder `paicode/` menjadi objek utama penelitian.
* Potongan kode penting disisipkan dalam skripsi menggunakan LaTeX `lstlisting`.
* Struktur project bisa ditampilkan dengan `verbatim` atau `tree`.

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

## Catatan Penting
karena tidak akan menggunakan gambar sama sekali di skripsi ini, maka untuk semua ilustrasi akan diisi/dibuat dengan tools yang disediakan oleh latex, baik itu untuk diagram, tabel, dan grafik atau apapun, intinya untuk ilustrasi tidak akan menggunakan cara lain selain dengan latex, kemudian untuk testing atau preview paicode (yang mana ini adalah CLI app) akan dilakukan dengan cara copas hasil interaksi langsung dari terminal, jadi tidak menggunakan gambar sama sekali.

---
