# FORME

Sistem informasi akuntansi membership dan pengakuan pendapatan pada FORME Fitness & Wellness. Aplikasi memakai HTML, CSS, JavaScript, Node.js built-in HTTP server, dan Supabase PostgreSQL melalui REST API.

## Struktur

- `public/` - dashboard frontend
- `sql/schema.sql` - ERD empat entitas, constraint, index, RLS, dan seed data
- `app.js` - static server dan health endpoint

## Menjalankan

```bash
node app.js
```

Buka `http://localhost:3000`, lalu masukkan Project URL dan Publishable Key Supabase melalui menu Pengaturan. Jalankan isi `sql/schema.sql` di SQL Editor Supabase terlebih dahulu.

## ERD

`customers` menjadi entitas pelanggan. `membership_plans` menyimpan katalog paket. `memberships` menghubungkan pelanggan ke paket dan mencatat periode/nominal. `payments` mencatat pembayaran membership dan menjadi dasar informasi pendapatan.

> Publishable Key aman dipakai di browser hanya jika RLS sudah aktif dan policy disesuaikan dengan kebutuhan keamanan produksi. Jangan menaruh service role key di frontend.
