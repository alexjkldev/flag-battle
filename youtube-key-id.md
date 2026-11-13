# Flag Battle: kunci API YouTube Anda

Mode streamer membaca chat siaran langsung Anda melalui YouTube Data API. Tanpa kunci Anda mendapat uji coba 5 menit per hari; dengan kunci gratis milik sendiri Anda bisa siaran berjam-jam. Prosesnya sekitar 5 menit.

## 1. Buka Google Cloud

Buka [console.cloud.google.com](https://console.cloud.google.com/) dan masuk dengan akun Google apa saja (tidak harus akun channel Anda). Setujui persyaratannya jika diminta. Tidak perlu kartu kredit.

## 2. Buat proyek

Di bagian atas halaman, klik pemilih proyek (**Select a project**), lalu **New project**. Nama apa saja boleh, misalnya `flag-battle`. Klik **Create** dan pastikan proyek baru terpilih di atas — semua langkah berikutnya dilakukan di sana.

## 3. Aktifkan YouTube Data API v3 — sebelum membuat kunci

Buka [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) dan klik **Enable**. API aktif saat tombolnya berubah menjadi **Manage**. Tanpa langkah ini kunci tidak akan berfungsi.

## 4. Buat kunci

Buka [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Di daftar pembatasan API, centang hanya **YouTube Data API v3**, lalu klik **Create**. Jendela **API key created** menampilkan kunci Anda — salin.

Jika YouTube Data API v3 tidak ada di daftar, kembali ke langkah 3. Biarkan pembatasan aplikasi pada **None**.

## 5. Tempel di aplikasi

Di Flag Battle: layar utama → **Pengaturan** → mode **Duel** → **Mode streamer** → **Aktif**. Ketuk tombol tempel di samping **Kunci YouTube API v3-mu** — bukan di kolom teks petunjuk di bawahnya. Kunci hanya disimpan di ponsel Anda, di penyimpanan aman, dan tidak pernah ditampilkan di layar.

## Jika kunci ditolak

Penyebabnya terlihat di blok **BERIKUTNYA**:

- **«YouTube Data API v3 nonaktif untuk kunci ini»** — lakukan langkah 3 di proyek yang sama dengan kunci, lalu tunggu beberapa menit.
- **«pembatasan kunci memblokir YouTube»** — buka kunci di [Credentials](https://console.cloud.google.com/apis/credentials): pembatasan API harus berisi **YouTube Data API v3**, pembatasan aplikasi harus **None**.
- **«kunci YouTube tidak valid»** — kunci tersalin tidak lengkap: diawali `AIza` dan panjangnya 39 karakter.

Setelah itu kembali ke menu dan mulai siaran lagi.

## Perlu diketahui

- **Gratis.** Kuota standar adalah 10.000 unit per hari. Dalam mode «Instan» chat masuk secara real time dan kuota cukup untuk sekitar 6 jam siaran per hari; «Hemat» memperpanjangnya hingga sekitar 12 jam, dengan jeda hingga 10 detik. Mode dipilih di aplikasi.
- **Kuota direset tengah malam waktu Pasifik.** Jika habis, aplikasi menampilkannya di blok **BERIKUTNYA** dan pertarungan berlanjut dengan bendera acak.
- Gunakan project ini hanya untuk Flag Battle agar kuotanya tidak terpakai hal lain.
- Untuk mencabut kunci, hapus di [Credentials](https://console.cloud.google.com/apis/credentials).
