# PROMPT: Build the WEDNESDAY Brand Website

> This file lives in the repo root. Give it to a coding agent (GitHub Copilot coding agent, Copilot Chat, etc.) or use the issue template in `.github/ISSUE_TEMPLATE/`.
> Logo reference: `public/assets/logo-wednesday.png`. Full brand document: `docs/brand-concept-wednesday.docx`.

---

## 1. Role & Goal

You are a senior front-end developer and brand-aware UI designer. Build a **responsive, single-brand website (landing page + lookbook + collection page)** for **WEDNESDAY**, a women's casual office wear brand from Indonesia.

The site must feel **clean, minimalist, modern, relaxed and refined**, and must faithfully follow the brand identity below. Do not turn it into a formal/conventional officewear site.

---

## 2. Brand Overview

- **Brand name:** WEDNESDAY (store label: "Fashion Store, Est. 2025")
- **Category:** Casual office wear for modern women
- **Target market:** Women aged 20-40: office workers, young professionals, career women, entrepreneurs, creatives, marketing/HR/admin staff, high-mobility and hybrid workers. They like oversized, minimalist, modest and smart-casual styles.
- **Philosophy:** Named after Wednesday, the midpoint of the work week. It represents balance between busyness and comfort, professionalism and freedom, work and personal life. Clothes are *not too formal, not too casual*.
- **Vision:** The go-to casual office wear brand for modern women, balancing comfort, style and professionalism in every activity.
- **Mission:** Modern, minimalist, comfortable workwear; relaxed cuts that stay neat; easy-to-mix colors; flexible for indoor and outdoor use; help women express personal style without losing a professional look.
- **Brand tagline:** *Relaxed. Refined. Ready.*
  - Relaxed = comfort via loose cuts and mobility-friendly materials
  - Refined = aesthetics, neatness, professional impression
  - Ready = ready for office and beyond
- **Campaign tagline:** *Effortless from 9 to Life.*
- **Brand essence:** *Comfortable clothing, effortless styling, and confidence in every moment.*
- **USP:** "Relaxed tailoring": oversized comfort with a neat, professional finish. Relaxed fit without looking oversized; easy mix & match; comfortable everyday workwear; office-to-after-hours styling; minimalist but refined.
- **Brand character:** Clean & Minimalist, Casual & Modern, Relaxed & Comfortable, Stylish & Versatile, Simple but Refined.
- **Key messages:** "Comfort is a Style" / "Professional Without Being Formal" / "One Outfit, More Possibilities".
- **Sample promo copy:** *You don't have to choose between looking good and feeling good. With WEDNESDAY, stay comfortable, look refined, and be ready for everything.*

---

## 3. Visual Identity

### Logo (reference file: `public/assets/logo-wednesday.png`)
- Wordmark in **lowercase, stacked in 4 lines: `wed / nes / day / wear`**
- Typeface: **rounded, chunky, playful** (bubbly, friendly, approachable, not rigid)
- Color: **deep red** on **cream / off-white** background
- Small badge below the wordmark: **"FASHION STORE EST.2025"** in the same playful style
- Logo philosophy: playful rounded type = relaxed, approachable, expressive, confident. Red + cream = boldness balanced with simplicity and comfort.

### Color system (define as CSS variables / Tailwind tokens)
| Token | Role | Value |
| --- | --- | --- |
| `--brand-red` | Logo, key accents, CTA highlights only | `#A80000` (match the logo as closely as possible) |
| `--brand-cream` | Main page background | `#F5F3EF` |
| `--sand` | Product palette / neutral surface | `#D8C3A5` |
| `--mocha` | Product palette / text accent | `#7B5E4B` |
| `--olive` | Product palette | `#6B6B3A` |
| `--navy` | Product palette / dark text option | `#1F2A44` |
| `--off-white` | Cards / surfaces | `#FAF8F4` |
| `--dusty-blue` | Supporting | `#8FA3B8` |
| `--dusty-rose` | Supporting | `#C9A0A0` |
| `--charcoal` | Body text | `#333333` |

Rules:
- The page is mostly **cream + neutral/earthy tones** (clean, timeless, versatile). Use **brand red sparingly** as the bold accent (logo, small highlights, buttons on hover), never as a full-page color.
- Keep contrast accessible (WCAG AA for all text).

### Typography
- Display / logo-style headings: a **rounded, playful display font** similar to the logo (suggest *Fredoka*, *Baloo 2* or *Chewy* from Google Fonts), used only for big headings and the brand name, lowercase.
- Body: a clean, minimal sans-serif (suggest *Inter* or *DM Sans*).
- Generous whitespace, large type, minimal ornamentation.

### Imagery & layout feel
- Lots of whitespace, editorial/lookbook layout, soft shadows or none, rounded corners that echo the rounded logo.
- Models/photos should look modest, professional and natural. Use neutral placeholder images (solid color blocks or `https://placehold.co`) with `alt` text; clearly mark where real photos go.
- Subtle motion only (fade/slide on scroll, soft hover). Respect `prefers-reduced-motion`.

---

## 4. Site Structure

Single-page site with smooth-scroll sections plus a collection page.

1. **Header / Nav:** logo (stacked wordmark small), links: Collection, Lookbook, About, Contact. Sticky, cream background, mobile hamburger menu.
2. **Hero:** big stacked wordmark `wed nes day wear` in brand red on cream, tagline *Relaxed. Refined. Ready.*, campaign line *Effortless from 9 to Life.*, CTA "Lihat Koleksi".
3. **Brand Story / Philosophy:** why "Wednesday" (midpoint of the week, balance of work and life). Short, airy text.
4. **Three Key Messages:** cards for Comfort is a Style / Professional Without Being Formal / One Outfit, More Possibilities.
5. **Collection 001: THE EVERYDAY EDIT** (theme: *Your everyday workwear, made effortless.*): product grid (data below) with color swatches per product.
6. **Product Categories:** Relaxed Tops, Relaxed Bottoms, Modern Outerwear, One-Piece Collection, Essential Collection (short description each).
7. **Design & Quality Standards:** table/list (silhouette, style, comfort, look, colors, flexibility, sizes S-XXL).
8. **Color Identity:** visual swatches for primary (Sand, Mocha, Olive, Navy) and supporting (Off White, Dusty Blue, Dusty Rose, Charcoal).
9. **Lookbook / Styling:** "Office to after hours" outfit-combination cards using the Collection 001 pieces.
10. **Contact / Footer:** Instagram link placeholder, WhatsApp CTA placeholder, "Fashion Store, Est. 2025", copyright.

---

## 5. Product Data (use a typed data file, e.g. `src/data/products.ts`)

Collection 001: THE EVERYDAY EDIT

| Product | Category | Colors |
| --- | --- | --- |
| Relaxed Oversized Shirt | Relaxed Tops | Off White, Dusty Blue |
| Minimalist Loose Blouse | Relaxed Tops | Sand, Olive |
| Wide-Leg Tailored Pants | Relaxed Bottoms | Black, Mocha |
| Casual Sleeveless Vest | Modern Outerwear | Navy, Sand |
| Relaxed Shirt Dress | One-Piece | Mocha, Off White |
| Basic Knit Top | Essential | Charcoal, Dusty Rose |

Each product object: `id`, `name`, `category`, `colors[] (name + hex)`, `sizes: ["S","M","L","XL","XXL"]`, `description` (short, Indonesian), `image` (placeholder), `price` (leave as `null` / "Segera hadir").

Category design standards to reflect in descriptions:
- **Tops:** loose but proportional, not tight, comfortable length, not see-through, simple modern details.
- **Bottoms:** comfortable waist for long sitting, not tight, clean falling silhouette, easy to mix.
- **Outerwear:** not stiff, light and comfortable, easy to layer, material adjusted for AC offices / outdoors.
- **One-piece:** modest, practical, modern silhouette, office and semi-formal.
- **Essentials:** basic tees, long sleeves, inner tops, knitwear for efficient outfit combinations.

---

## 6. Tech Stack & Project Setup

- **Vite + React + TypeScript + Tailwind CSS**
- Static build deployable to **GitHub Pages** (configure `base` in `vite.config.ts`, add a GitHub Actions workflow `.github/workflows/deploy.yml`)
- Components: `Header`, `Hero`, `BrandStory`, `KeyMessages`, `ProductGrid`, `ProductCard`, `CategoryList`, `QualityStandards`, `ColorPalette`, `Lookbook`, `Footer`
- Use design tokens from Section 3 in `tailwind.config.ts`
- Include `README.md` with run/build/deploy instructions and where to replace logo/photos

---

## 7. Language & Copywriting

- Site language: **Bahasa Indonesia** as the main language, with English brand taglines kept as-is (*Relaxed. Refined. Ready.* / *Effortless from 9 to Life.*).
- Tone of voice: warm, relaxed, confident, simple. Not stiff or salesy. Speak to modern working women.
- Do not invent facts (awards, press, reviews, prices, stock). Use placeholders.
- **Important:** do not claim "anti-kusut / anti-wrinkle", "tidak menerawang" or "breathable" as proven product benefits on the site. The brand document states these claims must be tested per material first. Phrase them as design intentions only.

---

## 8. Acceptance Criteria

- [ ] Mobile-first and fully responsive (360px to 1440px+)
- [ ] Hero shows the stacked `wed nes day wear` wordmark in brand red on cream, matching the logo
- [ ] Colors and typography follow Section 3; red is used only as an accent
- [ ] All 6 products of Collection 001 render with correct color swatches
- [ ] All 10 sections in Section 4 exist and are navigable
- [ ] Lighthouse: Performance, Accessibility, Best Practices, SEO all 90+
- [ ] Semantic HTML, alt text, keyboard-navigable, visible focus states
- [ ] Meta title/description + Open Graph tags (title: "WEDNESDAY | Effortless from 9 to Life")
- [ ] Clean, commented, typed code; no unused dependencies
- [ ] Builds without errors and deploys via GitHub Actions to GitHub Pages

---

## 9. Constraints

- Do not use formal/corporate styling (dark heavy navy-and-gray blocks, stiff stock-photo feel).
- Do not add features beyond this brief (no checkout, no login) unless asked.
- Ask before changing the brand name, taglines, color tokens or logo treatment.
