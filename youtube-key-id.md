# Flag Battle: kunci API YouTube Anda

Mode streamer membaca chat siaran langsung Anda melalui YouTube Data API. Tanpa kunci Anda mendapat uji coba 5 menit per hari; dengan kunci gratis milik sendiri Anda bisa siaran berjam-jam. Prosesnya sekitar 5 menit.

## 1. Buka Google Cloud

Buka [console.cloud.google.com](https://console.cloud.google.com/) dan masuk dengan akun Google apa saja (tidak harus akun channel Anda). Setujui persyaratannya jika diminta. Tidak perlu kartu kredit.

## 2. Buat project

Di bagian atas halaman, klik pemilih project (**Select a project**), lalu **New project**. Nama apa pun boleh, misalnya `flag-battle`. Klik **Create** dan pastikan project baru sudah terpilih di bagian atas.

## 3. Aktifkan YouTube Data API

Buka [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) lalu klik **Enable**.

## 4. Buat kunci

Buka [Credentials](https://console.cloud.google.com/apis/credentials), klik **Create credentials** → **API key**. Buka kunci baru itu untuk diedit:

- **API restrictions** → **Restrict key** → centang hanya **YouTube Data API v3**. Dengan begitu kunci yang bocor tidak bisa dipakai untuk hal lain.
- **Application restrictions** boleh tetap **None**.

Klik **Save**, lalu salin kuncinya (**Show key** → salin).

## 5. Tempelkan di aplikasi

Di Flag Battle buka **Pengaturan → Duel → Mode streamer** lalu ketuk tombol tempel di samping kolom kunci API YouTube. Kunci hanya disimpan di ponsel Anda, di penyimpanan aman, dan tidak pernah ditampilkan di layar.

## Perlu diketahui

- **Gratis.** Kuota standar adalah 10.000 unit per hari. Dalam mode «Instan» chat masuk secara real time dan kuota cukup untuk sekitar 6 jam siaran per hari; «Hemat» memperpanjangnya hingga sekitar 12 jam, dengan jeda hingga 10 detik. Mode dipilih di aplikasi.
- **Kuota direset tengah malam waktu Pasifik.** Jika habis, aplikasi menampilkannya di blok **BERIKUTNYA** dan pertarungan berlanjut dengan bendera acak.
- Gunakan project ini hanya untuk Flag Battle agar kuotanya tidak terpakai hal lain.
- Untuk mencabut kunci, hapus di [Credentials](https://console.cloud.google.com/apis/credentials).
