# Tugas Akhir Praktikum Pemrograman Web - Judul 2: Git & Version Control
Repository ini dibuat untuk Tugas Akhir Mata Kuliah Praktikum Pemrograman Web, Judul 2. Repository ini mendemonstrasikan penggunaan Git secara lengkap untuk proyek website portfolio Talitha.

## Deskripsi Proyek

Proyek ini adalah implementasi website portfolio statis yang dibuat untuk Tugas Akhir Percobaan 1. Tujuan utama repository ini adalah mendemonstrasikan workflow Git secara lengkap, mulai dari:

* Inisialisasi repository
* Commit bertahap
* Pembuatan branch dan merge
* Resolusi konflik menggunakan rebase
* Sinkronisasi dengan GitHub


## Instalasi dan Penggunaan

Website ini bersifat statis (HTML/CSS) dan tidak memerlukan instalasi khusus.

1. **Clone repository:**

   ```bash
   git clone https://github.com/talithadifa/TA-PPW-Judul-2.git
   ```
2. **Masuk ke folder proyek:**

   ```bash
   cd TA-PPW-Judul-2
   ```
3. **Buka file:**
   Buka `index.html` di browser untuk melihat tampilan website.


## Workflow Git yang Dilakukan

### 1. Inisialisasi dan Commit Awal

* `git init` untuk membuat repository Git lokal.
* Commit pertama hanya untuk `index.html`.
* Commit kedua untuk seluruh file aset dan CSS.

### 2. Remote Repository (GitHub)

* `git remote add origin ...` untuk menghubungkan repository lokal dengan GitHub.
* `git push -u origin main` untuk mengunggah commit awal.

### 3. Branching dan Merging

* `git checkout -b section-hobi` membuat branch baru untuk fitur tambahan.
* Commit "Menambahkan section Hobi" di branch tersebut.
* `git merge section-hobi` untuk menggabungkan perubahan ke branch main.
* `git branch -d section-hobi` untuk menghapus branch setelah merge selesai.

### 4. Resolusi Konflik (Rebase)

* Push ditolak karena history lokal dan remote telah bercabang (non-fast-forward).
* `git pull --rebase` digunakan untuk menyatukan history.
* Konflik terjadi karena commit lokal dan remote mengubah baris kode yang sama.
* Konflik diselesaikan manual di VS Code, file di-stage (`git add`) dan commit diperbaiki menggunakan `git commit --amend`.
* `git rebase --continue` dijalankan hingga rebase selesai.
* `git push --force` digunakan untuk memaksa GitHub menerima history baru yang bersih.


## Hasil `git log --graph --oneline`

Berikut adalah tampilan history commit linear setelah proses rebase selesai:
<img width="729" height="171" alt="Screenshot 2025-11-05 015412" src="https://github.com/user-attachments/assets/f976bda1-6c78-42e0-90cf-955cbb399825" />



