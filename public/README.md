# GOALRUSH untuk Cloudflare Workers (situs statis)

Struktur (taruh di ROOT repo GitHub):
  wrangler.jsonc
  public/index.html

Pengaturan (link APK, versi, Telegram, jumlah klik, FAQ, dll) ada di <script id="cfg"> di public/index.html.
Edit JSON itu, commit, dan Cloudflare akan deploy ulang otomatis.

Batasan versi statis:
- Tidak ada panel admin dan tidak ada pengecekan di server (semua jalan di browser).
- Link APK terlihat di kode halaman.
- Satu file di Workers Assets maksimal 25 MiB, jadi APK TIDAK bisa ditaruh di public/.
  Pakai link eksternal (R2, GitHub Releases, dll) di field "apk".
