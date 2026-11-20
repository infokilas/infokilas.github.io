# INFOKILAS GitHub Pages

Struktur root dibuat mengikuti contoh repository Media Core:
`_includes/`, `_layouts/`, `_posts/`, `assets/images/`, `README.md`, `_config.yml`, `artikel.html`, `index.md`.

## Instalasi
1. Ekstrak ZIP.
2. Upload **isi ZIP** langsung ke root repository `infokilas.github.io`.
3. Settings > Pages > Deploy from a branch > main > /(root).
4. Tunggu build GitHub Pages selesai.

## Artikel
Buat file baru di `_posts/YYYY-MM-DD-slug.md` dengan front matter `layout: post`, `title`, `date`, `categories`, `description`, `image`, `author`, `hide_buttons`.

Sitemap otomatis: `/sitemap.xml` melalui plugin jekyll-sitemap.
CSS ada di `assets/images/style.css` agar struktur folder di root sama seperti contoh.
