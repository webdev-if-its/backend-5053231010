# backend-nrp

Repo tugas mata kuliah **Pengembangan Backend Dasar**, dibuat dari template [`webdev-if-its/backend-template`](https://github.com/webdev-if-its/backend-template). Ganti judul di atas jadi nama repo kalian sendiri (`backend-nrp`, contoh: `backend-5025201012`).

## Aturan Umum

- Tugas tiap pertemuan disimpan di folder `pertemuan-XX/` pada repo ini.
- Commit message wajib menyebut level yang dicapai: `pertemuan-XX: level N selesai`.
- Deadline push: sebelum pertemuan berikutnya dimulai.
- Semua level dicek otomatis lewat `go test` — baca `pertemuan-XX/SOAL.md` tiap minggu untuk detail levelnya.

## Mengambil Pertemuan Baru Tiap Minggu

Repo ini **tidak otomatis sinkron** dengan template dosen. Begitu ada pertemuan baru, jalankan (ganti `pertemuan-02` sesuai minggu berjalan):

```bash
git fetch https://github.com/webdev-if-its/backend-template.git main
git checkout FETCH_HEAD -- pertemuan-02
```

Perintah ini **aman dijalankan kapan pun** — tidak akan menimpa folder pertemuan lain yang sudah kalian kerjakan, karena hanya mengambil folder yang disebutkan. Setelah itu, commit folder barunya seperti biasa.

Kalau dosen memperbaiki sesuatu di pertemuan yang sudah dirilis (mis. ada bug di test), biasanya cukup ambil ulang file yang diperbaiki saja, bukan seluruh folder — akan diumumkan file mana yang berubah.

---

Bagian di bawah ini **isi bertahap** sesuai level yang sedang kalian kerjakan (lihat `pertemuan-01/SOAL.md`) — heading-nya dicek otomatis, jangan diganti namanya.

## Identitas
- Nama: Aisyahra Alhanni Satria
- NRP: 5053231010
- Kelas: M

## Commit vs Push
Commit adalah command disaat kita benar-benar sudah percaya kalau kerjaan kita sudah selesai dan kita berani komit untuk dimasukkan ke repo dan tercatat di riwayat. Push adalah command untuk mendorong kerjaan kita masuk kedalam repo setelah kita commit. Jika seseorang sudah commit tapi belum push, maka kerjaan mereka tidak akan masuk ke dalam repo main.

## Reproducibility
Reproducibility artinya program dapat dijalankan oleh anggota tim lain dengan hasil yang konsisten. Perbedaan versi Go dapan menyebabkan hasil runtime yang berbeda. Namun, pada program sederhana seperti ini, perbedaan versi biasanya tidak menjadi masalah selama kode tetap kompatibel.

## Catatan Merge Conflict
ada konflik dimana saat merubah branch, kode yang sudah tertulis hilang dan harus start dari awal lagi. Jujur bingung, tapi berakhiran berhasil. Pada bagian CetakInfo, aku membuat dua jenis fungsi yang bentuknya berbeda. Jadi saat merge, aku memilih yang lebih mudah dan compact ketimbang menggunakan lebih banyak baris untuk fungsi yang tidak membutuhkan banyak baris.

## Kenapa .gitignore Penting
.gitignore penting untuk mencegah file yang tidak diperlukan, seperti hasil build dan konfigurasi IDE, ikut ter-commit ke repository. Contohnya, jika salah satu anggota tim tidak menggunakan .gitignore dan meng-commit folder .idea/ atau file hasil build, file tersebut dapat ikut terbawa saat anggota lain melakukan git pull dan menyebabkan konfigurasi IDE atau file yang tidak diperlukan menjadi berbeda dan mengganggu proses kolaborasi.

## Refleksi
Bagian yang paling membingungkan bagi saya adalah proses merge conflict karena saya harus memahami perubahan dari branch main dan branch fitur-sapaan sebelum menentukan kode mana yang harus dipertahankan. Setelah mencoba menyelesaikannya secara manual, saya akhirnya memahami bahwa merge conflict terjadi ketika Git tidak dapat menentukan perubahan mana yang harus dipilih, sehingga kita harus menggabungkan perubahan tersebut sendiri.
