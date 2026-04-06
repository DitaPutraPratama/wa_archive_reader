# WA Archive Reader

**100% Made with AI**

Akses langsung: https://ditaputrapratama.github.io/wa_archive_reader/

Aplikasi berbasis browser untuk menampilkan riwayat percakapan WhatsApp dari file export ZIP, lengkap dengan tampilan foto, video, dan voice note, tanpa instalasi dan tanpa server.

---

## Deskripsi

Chat Viewer adalah satu file HTML yang dapat dibuka langsung di browser. File ini membaca arsip ZIP export WhatsApp, mengekstrak isi chat dan semua media di dalamnya ke dalam memori, lalu menampilkannya dalam antarmuka percakapan dua sisi — satu pengirim di kiri, satu pengirim di kanan.

Semua proses terjadi sepenuhnya di dalam browser. Tidak ada data yang dikirim ke server manapun.

---

## Cara Export Chat dari WhatsApp

Sebelum menggunakan aplikasi ini, lakukan export dari WhatsApp terlebih dahulu.

1. Buka percakapan yang ingin diekspor di WhatsApp
2. Ketuk ikon tiga titik di pojok kanan atas
3. Pilih **Lainnya**, lalu pilih **Ekspor obrolan**
4. Pilih **Sertakan media** agar foto, video, dan voice note ikut tersimpan
5. Simpan atau kirim file ZIP yang dihasilkan ke perangkat yang akan digunakan untuk membuka Chat Viewer

---

## Cara Menggunakan

1. Buka file `chat-viewer.html` menggunakan browser Chrome atau Edge
2. Klik area pilih file atau seret file ZIP ke dalamnya
3. Tunggu proses pembacaan selesai, ditandai dengan progress bar
4. Percakapan akan langsung tampil

Tidak perlu mengekstrak file ZIP. Cukup satu file ZIP langsung dari WhatsApp.

---

## Fitur

### Tampilan Percakapan

Dua pengirim ditampilkan di sisi berlawanan. Pengirim pertama yang terdeteksi sebagai bukan pengguna utama ditempatkan di kiri, dan pengirim lainnya di kanan. Warna bubble kiri dan kanan dibedakan agar mudah dibaca.

### Media

Foto ditampilkan langsung di dalam bubble. Video dapat diputar langsung tanpa membuka aplikasi lain. Voice note ditampilkan dengan visualisasi waveform dan tombol putar. Jika file media tidak ditemukan di dalam ZIP, akan muncul keterangan nama file sebagai pengganti.

### Lightbox Foto

Mengklik foto akan membuka tampilan layar penuh. Di dalam lightbox tersedia tombol navigasi untuk berpindah ke foto sebelumnya atau berikutnya tanpa harus menutup dan membuka ulang. Navigasi juga dapat dilakukan menggunakan tombol panah kiri dan kanan pada keyboard. Saat lightbox ditutup, halaman akan otomatis kembali ke posisi foto yang sedang ditampilkan.

### Tanggal Berjalan

Label tanggal ditampilkan secara permanen di bawah header dan berubah secara otomatis mengikuti tanggal pesan yang sedang terlihat di layar saat menggulir halaman.

### Pencarian Teks

Klik ikon kaca pembesar di header untuk membuka panel pencarian. Ketik kata yang ingin dicari dan semua kemunculannya akan langsung disorot. Tombol panah atas dan bawah di panel pencarian digunakan untuk berpindah antar hasil. Posisi saat ini ditampilkan sebagai angka, misalnya 3 dari 12. Pencarian juga dapat dioperasikan menggunakan tombol Enter untuk maju dan Shift+Enter untuk mundur.

### Loncat ke Tanggal

Klik ikon kalender di header untuk membuka panel loncat tanggal. Pilih tanggal dari daftar dropdown lalu klik tombol Pergi. Halaman akan langsung bergulir ke awal tanggal tersebut.

### Mode Gelap dan Terang

Klik ikon bulan di header untuk beralih ke mode gelap. Klik ikon matahari untuk kembali ke mode terang. Semua elemen tampilan menyesuaikan warna secara otomatis.

---

## Persyaratan

-   Browser: Google Chrome atau Microsoft Edge versi terbaru
-   File: ZIP hasil export WhatsApp yang berisi `_chat.txt` dan file media
-   Tidak memerlukan koneksi internet setelah file HTML dibuka
-   Tidak memerlukan instalasi aplikasi tambahan

---

## Catatan Teknis

File chat yang dibaca adalah `_chat.txt` di dalam ZIP. Format yang didukung adalah format export WhatsApp standar dengan pola waktu `[DD/MM/YY, HH.MM.SS] Nama: Pesan`. Media yang didukung mencakup gambar dalam format JPG, JPEG, PNG, GIF, dan WebP; video dalam format MP4, MOV, AVI, 3GP, dan MKV; serta audio dalam format OPUS, OGG, M4A, AAC, MP3, dan WAV.

File media di dalam ZIP dibaca ke dalam memori sebagai blob URL sehingga dapat diputar dan ditampilkan langsung tanpa menulis file ke disk.

---

## Struktur File

```
chat-viewer.html    -- Satu-satunya file yang diperlukan
README.md           -- Dokumen ini
```

Untuk menggunakan aplikasi, cukup simpan `chat-viewer.html` di sembarang lokasi dan buka dengan browser. Tidak ada dependensi eksternal yang perlu diinstal secara lokal karena library JSZip dimuat langsung dari CDN saat pertama kali digunakan.

---

_100% Made with AI_
