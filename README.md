# ANDRITZ Power BI Portal - GitHub Pages Version

Versi ini dibuat untuk GitHub Pages (`github.io`), jadi bentuknya static HTML/CSS/JavaScript.

GitHub Pages tidak menjalankan PHP atau Laravel. Menurut dokumentasi resmi GitHub, Pages mem-publish file HTML, CSS, dan JavaScript dari repository.

## File

- `index.html` - aplikasi portal static.
- `.nojekyll` - agar GitHub Pages menyajikan file apa adanya.
- `images/` - logo ANDRITZ dan ikon divisi.

## Akun Demo

Portal:

```text
admin / admin12345
```

Divisi:

```text
Finance & Accounting: finance / finance123
Human Resources: hr / hr123
Project Management: pm / pm123
Commercial: commercial / commercial123
Field Services: fieldservice / fieldservice123
EPS: eps / eps123
Automation: automation / automation123
```

## Mengubah Link Power BI

Buka `index.html`, cari bagian `const DIVISIONS = [...]`, lalu isi properti `url` pada dashboard yang diinginkan.

Contoh:

```js
{ slug: "cashflow", title: "Cashflow", description: "...", url: "https://app.powerbi.com/view?r=..." }
```

## Hosting di GitHub Pages

1. Buat repository bernama `<username>.github.io` untuk user site, atau repository biasa untuk project site.
2. Upload semua isi folder ini ke repository tersebut.
3. Buka `Settings > Pages`.
4. Pilih `Deploy from a branch`.
5. Pilih branch `main` dan folder `/root`.
6. Tunggu publish selesai, biasanya beberapa menit.

## Catatan Keamanan

Login pada versi static ini hanya simulasi di browser. Username dan password tersimpan di JavaScript sehingga bisa dilihat dari source code. Untuk login sungguhan yang aman, gunakan hosting yang mendukung backend seperti PHP/Laravel, VPS, shared hosting PHP, atau layanan cloud app.
