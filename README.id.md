<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logo bestimage.ai"></a></p>

# Kumpulan Prompt Video Wan 3.0 — Panduan Bahasa Indonesia

**148 arahan produksi video dalam 14 kategori**.

[Panduan bahasa Inggris](README.md) · [Semua 15 bahasa](locales/README.md) · [Indeks seluruh adegan](prompts/README.md)

![Gambar konsep: petugas arsip membuka peta bintang di ruang peta observatorium dalam cahaya fajar](assets/wan-3-prompt-collection-hero.png)

*Ilustrasi statis ini dibuat dengan alat pembuat gambar bawaan, bukan keluaran video Wan 3.0. Lihat [prompt gambar dan asal-usulnya](assets/README.md).*

## Cakupan dan langkah awal

Tersedia panduan pengantar serta satu prompt perbandingan yang sama dalam 15 bahasa, **bukan terjemahan lengkap seluruh 148 arahan**. Enam kategori pertama menggunakan bahasa Mandarin, delapan sisanya menggunakan bahasa Inggris. Prompt perbandingan dan terjemahannya tidak dihitung sebagai entri tambahan.

Pilih arahan dari indeks, sesuaikan detailnya, lalu siapkan semua masukan. Keterangan referensi menjelaskan peran aset, bukan menandakan bahwa berkasnya disediakan. Atur durasi, rasio aspek, resolusi, dan suara pada antarmuka atau kolom permintaan yang dipilih; teks prompt saja tidak mengatur permintaan API. Lakukan percobaan kecil, lalu periksa aksi, bentuk, identitas, waktu, dan suara.

## Struktur prompt delapan lapis

```text
[Keluaran] durasi + rasio aspek + medium visual
[Subjek] ciri identitas tetap + pakaian atau bahan + detail yang tidak boleh berubah
[Lingkungan] waktu + tempat + cuaca + lapisan ruang
[Aksi] pemicu → gerakan berkelanjutan → hasil yang terlihat
[Kamera] ukuran pengambilan gambar + posisi + satu jalur gerak + komposisi akhir
[Visual] pencahayaan + warna + tekstur + kabur gerak
[Suara] suara lingkungan + suara aksi + musik + bahasa dialog (jika didukung)
[Batasan] hal yang harus dipertahankan + masalah yang harus dihindari
```

## Prompt perbandingan lengkap

**Mode:** teks menjadi video · **Pengaturan:** 10 detik, 16:9, suara aktif · **Masukan:** tidak ada

```text
Buat satu pengambilan gambar dokumenter berdurasi 10 detik dengan rasio 16:9 di tempat peminjaman perkakas warga yang tenang. Seorang relawan dewasa berambut keriting pendek, mengenakan celemek kuning mustard dan kemeja biru tua dengan lengan digulung, memperbaiki kipas meja kecil berwarna merah yang stekernya tetap tercabut sepanjang adegan. Pada 0–3 detik, relawan meletakkan kisi pelindung yang telah dilepas di samping kipas yang diam. Pada 3–7 detik, relawan menyeka debu dari satu bilah kipas dengan kain lembut sementara kamera bergeser perlahan ke kanan setinggi permukaan meja. Pada 7–10 detik, relawan meletakkan kain dan menyelaraskan kisi dengan rumah kipas, tanpa mencolokkan steker atau menyalakan kipas. Cahaya jendela memperlihatkan tekstur logam yang aus dan kain katun. Suara: gesekan kain, satu klik pelan dari kisi, dan suasana ruangan yang tenang; tanpa ucapan atau musik. Pertahankan orang dan kipas yang sama, tiga bilah, rumah kipas merah, serta kabel yang tetap tidak terhubung ke listrik. Jangan tampilkan bilah yang berputar, perkakas tambahan, label yang dapat dibaca, takarir, atau pergantian potongan gambar.
```

**Dapat disesuaikan:** warna celemek, warna kipas, cahaya ruangan. **Periksa:** steker tetap tercabut dan kipas tetap diam; jumlah bilah serta kontak tangan konsisten. Ini konsep kreatif, bukan petunjuk perbaikan peralatan listrik.

## Memilih API Wan 3.0 di bestimage.ai

| Jalur (halaman model berbahasa Inggris) | Masukan dan pemeriksaan |
|---|---|
| [Teks menjadi video](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Uraikan satu peristiwa lengkap dengan sebab, aksi antara, dan hasil yang terlihat |
| [Gambar menjadi video](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Jalur dalam dokumentasi platform ini membutuhkan gambar awal **dan akhir**; jelaskan transisi fisik dan pertahankan bentuk serta komposisi |
| [Referensi menjadi video](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Tetapkan satu peran untuk setiap referensi identitas, objek, ruang, gerakan, atau suara |
| [Penyuntingan video](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Sediakan video sumber dan satu perubahan terbatas; pertahankan penampilan, durasi, kamera, dan area lainnya |

Halaman model menyediakan antarmuka dan contoh permintaan publik terkini. Tidak semua produk Wan menyediakan kontrol yang sama. Lihat [kemampuan dan batasan](guides/model-capabilities.md).

[Panduan alur API dan pengendalian biaya](guides/bestimage-wan-3-api.md) berbahasa Inggris membahas permintaan, pemeriksaan status berkala, validasi masukan, dan perencanaan percobaan. **Host API bestimage.ai adalah `https://api.flaq.ai`.** Gunakan kunci API yang diterbitkan melalui akun bestimage.ai Anda. Periksa harga dan ketentuan terbaru pada halaman model dan akun sebelum menggunakan kredit.

## Menyiapkan gambar referensi dengan GPT Image 2

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) menghasilkan gambar statis; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) menyunting gambar dan menggabungkan referensi visual. Siapkan lembar karakter, referensi produk, atau komposisi awal dan akhir yang telah disetujui. Ekspor dan periksa gambar sebelum memasukkannya ke jalur Wan yang sesuai.

Keduanya adalah **model gambar terpisah**, bukan titik akhir video Wan. Repositori ini tidak mengotomatiskan perpindahan tersebut dan tidak mengklaim ilustrasi konsep dibuat melalui API itu. Lihat [alur persiapan gambar referensi](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Panduan dan kontribusi

[Panduan penulisan prompt](guides/prompting-guide.md), [kemampuan model](guides/model-capabilities.md), dan [pemecahan masalah](guides/troubleshooting.md) ditulis dalam bahasa Mandarin aksara sederhana; panduan API dalam bahasa Inggris. Tidak semua panduan diterjemahkan. Daftar kategori beserta jumlahnya tersedia di [panduan bahasa Inggris](README.md).

Baca [panduan kontribusi](CONTRIBUTING.md) sebelum berbagi. Cantumkan pengaturan tepat, peran masukan, hak penggunaan, pengamatan, dan status sudah atau belum diuji secara jujur. Jangan bagikan kredensial, dokumen pribadi, atau URL media bertanda tangan yang akan kedaluwarsa.

## Tentang bestimage.ai

Tim [bestimage.ai](https://bestimage.ai/) mengkurasi dan memelihara pustaka prompt ini, menghubungkan alur kerja kreatif dengan API model gambar dan video.

## Raih penghasilan melalui program afiliasi bestimage.ai

Membuat tutorial, berbagi prompt, atau menerbitkan integrasi API? Bergabunglah dengan [program afiliasi bestimage.ai](https://bestimage.ai/affiliate-program/) dan dapatkan komisi dengan memperkenalkan bestimage.ai kepada audiens Anda.

- **20%** dari pesanan berbayar pertama yang memenuhi syarat milik pengguna rujukan.
- **10%** dari pesanan berbayar berikutnya yang memenuhi syarat dalam **60 hari setelah pengguna tersebut mendaftar**.

Kelayakan pesanan dan pembayaran mengikuti [perjanjian afiliasi yang berlaku](https://bestimage.ai/affiliate-agreement/).

## Lisensi

[MIT](LICENSE).
