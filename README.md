# WEDNESDAY: Brand Website

Casual office wear untuk wanita modern. **Relaxed. Refined. Ready.** / *Effortless from 9 to Life.*

Repositori ini berisi starter kit untuk membangun website brand WEDNESDAY dengan bantuan coding agent (GitHub Copilot atau sejenisnya).

## Isi repositori

| File / folder | Fungsi |
| --- | --- |
| `PROMPT.md` | Prompt utama (brief lengkap pembuatan website) |
| `.github/copilot-instructions.md` | Aturan tetap yang dibaca Copilot di repo ini |
| `.github/ISSUE_TEMPLATE/build-website.md` | Template issue untuk ditugaskan ke Copilot coding agent |
| `public/assets/logo-wednesday.png` | Logo WEDNESDAY |
| `docs/brand-concept-wednesday.docx` | Dokumen brand concept & identity |

## Cara menghubungkan ke GitHub

1. Buat repository baru di github.com (misalnya `wednesday-brand-website`), tanpa README bawaan.
2. Ekstrak file zip ini, lalu dari folder hasil ekstrak jalankan:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: WEDNESDAY brand starter kit"
   git branch -M main
   git remote add origin https://github.com/USERNAME/wednesday-brand-website.git
   git push -u origin main
   ```
   Alternatif tanpa terminal: di halaman repo klik **Add file > Upload files**, lalu seret seluruh isi folder hasil ekstrak (termasuk folder `.github`).

## Cara menjalankan prompt

- **Copilot coding agent:** buka tab **Issues > New issue**, pilih template *Build WEDNESDAY website*, buat issue, lalu tugaskan (assign) ke **Copilot**. Ketersediaan fitur ini bergantung pada paket GitHub Copilot Anda.
- **Copilot Chat / agent lain:** buka `PROMPT.md`, salin isinya, dan tempel sebagai instruksi.

## Mengaktifkan GitHub Pages

Setelah website dibuat dan workflow deploy ada: **Settings > Pages > Build and deployment > Source: GitHub Actions**.

## Catatan

- Kode warna di `PROMPT.md` adalah estimasi dari logo; sesuaikan dengan kode warna asli bila ada.
- Klaim bahan (anti-kusut, tidak menerawang, breathable) belum boleh ditampilkan sebagai fakta sebelum diuji.
