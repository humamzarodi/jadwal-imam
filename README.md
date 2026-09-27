# Jadwal Imam Harian Masjid An-Nuur Kotagede

Situs statis untuk menampilkan jadwal imam harian — satu imam per hari.

## Struktur folder

```
jadwal-imam/
├── index.html
├── css/style.css
└── assets/logo.svg
```

**Catatan penting:** nama-nama imam di dalam tabel saat ini masih **contoh
placeholder** — silakan ganti dengan nama imam yang sebenarnya bertugas di
Masjid An-Nuur.

## Cara mengubah nama imam

Buka `index.html`, cari baris `<tbody>...</tbody>`. Setiap hari adalah satu
baris `<tr>...</tr>` dengan 3 kolom (Nomor, Hari, Imam). Contoh:

```html
<tr>
  <td class="no">1</td>
  <td class="hari">Senin</td>
  <td>Ust. Abdul Karim</td>
</tr>
```

Tinggal ganti angka nomor, nama hari, dan nama imam sesuai jadwal yang
sebenarnya.

## Cara upload ke GitHub & tayangkan lewat GitHub Pages

1. Buat repository baru di GitHub (public).
2. Upload seluruh isi folder ini lewat "Add file → Upload files", atau lewat git:
   ```bash
   git init
   git add .
   git commit -m "Jadwal imam harian"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Tambahkan file kosong bernama `.nojekyll` di root repo (mencegah error build).
4. Buka **Settings → Pages**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Situs akan tayang di `https://USERNAME.github.io/NAMA-REPO/`.
