# Langsung ke WA Aja 🎀

Website satu halaman untuk mengumpulkan nama + nomor WhatsApp. Setiap kali ada yang submit, kamu langsung dapat notifikasi ke Gmail. Tampilan sudah responsif untuk HP maupun PC.

## Struktur folder

```
project/
├── index.html     -> seluruh website (HTML, CSS, JS jadi satu file)
└── README.md      -> file ini
```

Vercel otomatis mengenali `index.html` sebagai halaman utama tanpa konfigurasi tambahan, jadi tidak perlu `vercel.json`.

---

## Langkah 1 — Notifikasi email (Web3Forms) ✅ Sudah selesai

Email tujuan: **habib7bkn@gmail.com**
Access Key sudah ditempel di `index.html`: `6186daa6-ad36-4246-b78d-adb054de2120`

Tidak perlu diubah lagi — begitu website online, setiap submit langsung masuk ke Gmail kamu.

---

## Langkah 2 — Unggah ke GitHub

Buka terminal, arahkan ke folder project ini, lalu jalankan:

```bash
cd project
git init
git add .
git commit -m "Website form WA pertama"
```

Buat repository baru di GitHub (lewat browser):
1. Buka **https://github.com/new**
2. Isi nama repo, misalnya `wa-form-website`
3. Pilih **Public** atau **Private**, jangan centang "Add README" (karena sudah ada)
4. Klik **Create repository**

GitHub akan menampilkan perintah untuk menghubungkan repo lokal. Jalankan (ganti `USERNAME` dengan username GitHub kamu):

```bash
git remote add origin https://github.com/USERNAME/wa-form-website.git
git branch -M main
git push -u origin main
```

---

## Langkah 3 — Deploy ke Vercel

1. Buka **https://vercel.com** lalu login/daftar pakai akun GitHub kamu.
2. Klik **Add New... → Project**.
3. Pilih repository `wa-form-website` yang barusan di-push, klik **Import**.
4. Di bagian **Framework Preset**, pilih **Other** (karena ini website statis biasa).
5. Biarkan pengaturan lain default, klik **Deploy**.
6. Tunggu ± 30 detik, Vercel akan kasih URL seperti:
   ```
   https://wa-form-website.vercel.app
   ```
7. Selesai — website sudah online dan bisa diakses siapa saja.

---

## Update website setelah live

Kalau nanti mau ubah teks/warna, edit `index.html` lalu jalankan:

```bash
git add .
git commit -m "Update tampilan"
git push
```

Vercel otomatis re-deploy setiap kali kamu push ke branch `main` — tidak perlu upload manual lagi.

---

## Catatan

- Website ini sudah responsif otomatis: layout menyesuaikan sendiri di HP (satu kolom, padding lebih kecil) maupun di layar PC (kartu form melebar, lebih banyak ruang).
- Nomor dan nama yang masuk hanya dikirim ke email tujuan yang kamu atur di Formspree — tidak disimpan di tempat lain.
