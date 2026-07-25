# CEPOTECH — Design System

## Neo-Brutalism Tech Style Guide

---

## Design Philosophy

Cepotech UI menggunakan pendekatan **Neo-Brutalism Tech** — terinspirasi dari karakter Cepot (wayang) yang dipadukan dengan estetika tech modern.

### Karakter Desain

- **Bold** — elemen besar, berani, dominan
- **High Contrast** — hitam-putih sebagai fondasi, warna primer sebagai aksen kuat
- **Playful but Intelligent** — fun tapi tetap profesional
- **Minimal Gradient** — tidak ada gradient, semua warna flat/solid
- **Flat Strong Colors** — palet tegas tanpa transparansi berlebihan
- **Thick Borders** — border tebal 3-4px menjadi ciri khas visual
- **Slightly Imperfect Layout** — sedikit asimetris, tidak "corporate" kaku
- **Expressive Typography** — heading besar, tegas, jarak luas

### Tujuan

- Mudah diingat
- Terasa modern
- Berbeda dari SaaS dashboard biasa

### Brand Personality

- **Smart** — cerdas dan solutif
- **Rebellious** — berani melawan arus desain SaaS generik
- **Creative** — ekspresif dan tidak membosankan
- **Culturally Rooted** — akar budaya Nusantara (Cepot, wayang, batik)
- **Futuristic** — teknologi AI & automation terdepan

---

## Color Palette

### Primary Colors

| Token           | Hex       | Tailwind       | Kegunaan                                       |
| --------------- | --------- | -------------- | ---------------------------------------------- |
| **Cepot Red**   | `#FF3B30` | `bg-[#FF3B30]` | Primary buttons, CTA, highlights, important UI |
| **Wayang Gold** | `#FFC93C` | `bg-[#FFC93C]` | Accent, hover states, badges, highlights       |

### Neutral Colors

| Token            | Hex       | Tailwind       | Kegunaan                                 |
| ---------------- | --------- | -------------- | ---------------------------------------- |
| **Brutal Black** | `#000000` | `bg-black`     | Outlines, borders, strong contrast, text |
| **Soft Paper**   | `#F8F8F8` | `bg-[#F8F8F8]` | Card backgrounds, content areas          |

### Cultural Accent

| Token           | Hex       | Tailwind       | Kegunaan                              |
| --------------- | --------- | -------------- | ------------------------------------- |
| **Batik Brown** | `#7A4A2A` | `bg-[#7A4A2A]` | Decorative elements, cultural accents |

### Tech Accent

| Token             | Hex       | Tailwind       | Kegunaan                 |
| ----------------- | --------- | -------------- | ------------------------ |
| **Electric Blue** | `#2F80ED` | `bg-[#2F80ED]` | Links, analytics, graphs |

### Color Rules (Neo-Brutalism)

```
✅ Semua warna FLAT SOLID — tidak ada gradient
✅ Kontras TINGGI — hitam + warna cerah
✅ Card putih + border hitam tebal
✅ Button merah + text hitam
✅ Hover → warna bertukar (merah ↔ gold)
❌ Tidak ada gradient
❌ Tidak ada opacity/transparency berlebihan
❌ Tidak ada glassmorphism
```

---

## Typography

### Font Stack

| Priority  | Font              | Kegunaan                                  |
| --------- | ----------------- | ----------------------------------------- |
| Primary   | **Space Grotesk** | Headings & body — geometric, modern, kuat |
| Secondary | **Inter**         | Fallback & UI components                  |

### Scale

| Element   | Size               | Weight                               | Letter Spacing          |
| --------- | ------------------ | ------------------------------------ | ----------------------- |
| **H1**    | 48px (`text-5xl`)  | **Bold** (700) / **ExtraBold** (800) | Tight                   |
| **H2**    | 36px (`text-4xl`)  | **Bold** (700)                       | Tight                   |
| **H3**    | 28px (`text-3xl`)  | **SemiBold** (600)                   | Normal                  |
| **Body**  | 16px (`text-base`) | Normal (400)                         | Normal                  |
| **Small** | 14px (`text-sm`)   | Normal / Medium                      | Normal                  |
| **Badge** | 12px (`text-xs`)   | **Bold** (700)                       | Wide (`tracking-wider`) |

### Typography Rules

```
✅ Heading BESAR dan tegas
✅ Jarak antar baris LUAS
✅ Tidak terlalu banyak style variant
✅ UPPERCASE untuk badges dan labels
✅ Warna heading: hitam (#000)
```

---

## Border System

### The Neo-Brutalist Border

Border tebal adalah **ciri khas utama** neo-brutalism.

| Property          | Value                                    |
| ----------------- | ---------------------------------------- |
| **Border Width**  | `3px` (default) atau `4px` (emphasis)    |
| **Border Color**  | Black (`#000000`)                        |
| **Border Radius** | `0px` (square) atau `6px` (slight round) |

### Usage

```css
/* Card */
border: 3px solid black;
border-radius: 6px;

/* Button */
border: 3px solid black;
border-radius: 6px;

/* Input */
border: 3px solid black;
border-radius: 0px;
```

---

## Shadow System

### Offset Shadow (Brutal Shadow)

Neo-brutalism menggunakan **offset shadow yang keras** — bukan blur shadow biasa.

| Variant          | CSS                               | Tailwind                       |
| ---------------- | --------------------------------- | ------------------------------ |
| **Default**      | `box-shadow: 6px 6px 0px #000`    | `shadow-[6px_6px_0px_#000]`    |
| **Small**        | `box-shadow: 4px 4px 0px #000`    | `shadow-[4px_4px_0px_#000]`    |
| **Hover**        | `box-shadow: 8px 8px 0px #000`    | `shadow-[8px_8px_0px_#000]`    |
| **Active/Click** | `box-shadow: 2px 2px 0px #000`    | `shadow-[2px_2px_0px_#000]`    |
| **Red Shadow**   | `box-shadow: 6px 6px 0px #FF3B30` | `shadow-[6px_6px_0px_#FF3B30]` |
| **Gold Shadow**  | `box-shadow: 6px 6px 0px #FFC93C` | `shadow-[6px_6px_0px_#FFC93C]` |

Efeknya terasa seperti **komik / sticker** — 3D tapi flat.

---

## Buttons

### Primary Button

```
Background : Cepot Red (#FF3B30)
Text       : Black (#000)
Border     : 3px solid black
Shadow     : 6px 6px 0px black
Radius     : 6px
Font       : Bold, uppercase

Hover:
  Background → Wayang Gold (#FFC93C)
  Shadow     → 8px 8px 0px black

Active:
  Shadow     → 2px 2px 0px black
  Transform  → translate(4px, 4px)
```

### Secondary Button

```
Background : White
Text       : Black
Border     : 3px solid black
Shadow     : 4px 4px 0px black

Hover:
  Background → Cepot Red (#FF3B30)
  Color      → Black
```

### Ghost Button

```
Background : Transparent
Text       : Black
Border     : 3px solid black

Hover:
  Background → Soft Paper (#F8F8F8)
```

---

## Cards

### Standard Card

```
Background : White (#FFFFFF)
Border     : 3px solid black
Shadow     : 6px 6px 0px black
Padding    : 24px
Radius     : 6px

Hover:
  Shadow   → 8px 8px 0px black
  Transform → translate(-2px, -2px)
```

### Accent Card (Featured)

```
Background : Wayang Gold (#FFC93C)
Border     : 3px solid black
Shadow     : 6px 6px 0px black
```

### Dark Card

```
Background : Black (#000)
Border     : 3px solid #333
Text       : White
Shadow     : 6px 6px 0px #FF3B30
```

---

## Layout

### Grid

- **Columns**: 12-column grid
- **Container**: `max-w-[1200px]` (1200px)

### Spacing Scale

```
8px   → p-2
16px  → p-4
24px  → p-6
32px  → p-8
48px  → p-12
64px  → p-16
```

### Neo-Brutalist Layout Rules

```
✅ Sedikit asimetris — tidak harus perfectly centered
✅ Overlap dan offset elements diperbolehkan
✅ Generous whitespace
✅ Content tetap readable dan usable
❌ Tidak terlalu chaotic — tetap functional
```

---

## Navigation

### Top Navigation Bar

```
Background : White (#FFFFFF)
Border     : bottom 3px solid black
Position   : Sticky top
```

### Menu Items

```
Text       : Black, bold
Hover      : Background → Wayang Gold (#FFC93C)
Active     : Background → Cepot Red (#FF3B30), text → Black
```

### Mobile Menu

```
Background : White
Border     : 3px solid black
Shadow     : offset brutal
```

---

## Icons

### Style

- **Type**: Outline
- **Weight**: Bold / 2px stroke
- **Style**: Simple, geometric

### Recommended Libraries

- **Lucide Icons** (primary)
- **Heroicons** (alternative)

### Icon Rules

```
Stroke     : 2px
Size       : 20px (default), 24px (large)
Color      : Black (default), inherit from parent
```

---

## Interaction & Animation

### Minimalis — tidak banyak animasi

Neo-brutalism mengedepankan **kesederhanaan interaksi**.

### Micro Interactions

| Interaction | Effect                       |
| ----------- | ---------------------------- |
| **Hover**   | Color swap (red ↔ gold)      |
| **Click**   | Slight scale + shadow reduce |
| **Focus**   | Bold outline ring            |

### Transitions

```
Duration   : 150ms
Easing     : ease-in-out
Properties : background-color, box-shadow, transform
```

### Rules

```
✅ Hover → warna bertukar
✅ Click → slight press (translate + shadow shrink)
✅ Transition cepat — 150ms
❌ Tidak ada parallax
❌ Tidak ada scroll-triggered fade animations
❌ Tidak ada floating/glow effects
```

---

## Mascot — Cepot AI

### Karakter

- Styling: **Chibi / simplified** Cepot wayang
- Posisi: **Pojok kanan bawah** (floating)
- Role: **AI assistant**

### Dialog Example

```
"Cepot AI:
Butuh bantuan bikin automation bisnis?"

"Cepot AI:
Bisnis kamu makin otomatis. ✨"
```

---

## UX Writing

### Tone

**Friendly tech expert** — ahli tapi tidak sombong.

### Bahasa Rules

```
✅ Sederhana & langsung
✅ Helpful, bukan teknis berlebihan
✅ Bahasa Indonesia campur istilah tech yang umum
```

### Microcopy Examples

| Jangan                        | Gunakan                                 |
| ----------------------------- | --------------------------------------- |
| "Submit Form"                 | "Buat Website"                          |
| "Automation Workflow Created" | "Automation ready."                     |
| "Error occurred"              | "Sesuatu rusak. Cepot sedang perbaiki." |
| "Success"                     | "Done. Bisnis kamu makin otomatis."     |
| "Loading..."                  | "Sedang disiapkan..."                   |

---

## UI Feeling

Cepotech harus terasa seperti campuran:

- **Figma** — clean, design-tool feel
- **Gumroad** — bold, indie, creator-first
- **Vercel** — minimal, prestise tech
- **Neo brutalist startup sites** — berani, beda, memorable

**Dengan sentuhan budaya Nusantara futuristik.**

---

## Visual Identity Goal

> Cepotech harus terasa seperti **tech startup futuristik dari Indonesia** yang **berani dan kreatif**.
>
> Bukan corporate kaku. Tapi **smart rebel tech company**.

---

## Quick Reference — CSS Classes

```css
/* Brutal Card */
.brutal-card {
  background: #fff;
  border: 3px solid #000;
  box-shadow: 6px 6px 0px #000;
  border-radius: 6px;
  padding: 24px;
}

/* Brutal Button Primary */
.brutal-btn {
  background: #ff3b30;
  color: #000;
  border: 3px solid #000;
  box-shadow: 6px 6px 0px #000;
  border-radius: 6px;
  font-weight: 700;
  text-transform: uppercase;
  transition: all 150ms ease-in-out;
}
.brutal-btn:hover {
  background: #ffc93c;
  box-shadow: 8px 8px 0px #000;
  transform: translate(-2px, -2px);
}
.brutal-btn:active {
  box-shadow: 2px 2px 0px #000;
  transform: translate(4px, 4px);
}

/* Brutal Shadow utility */
.brutal-shadow {
  box-shadow: 6px 6px 0px #000;
}
.brutal-shadow-sm {
  box-shadow: 4px 4px 0px #000;
}
.brutal-shadow-lg {
  box-shadow: 8px 8px 0px #000;
}
.brutal-shadow-red {
  box-shadow: 6px 6px 0px #ff3b30;
}
.brutal-shadow-gold {
  box-shadow: 6px 6px 0px #ffc93c;
}
```

---

## Tailwind Quick Tokens

```
Border:    border-3 border-black  (custom) atau border-[3px] border-black
Shadow:    shadow-[6px_6px_0px_#000]
Red:       bg-[#FF3B30]
Gold:      bg-[#FFC93C]
Paper:     bg-[#F8F8F8]
Brown:     bg-[#7A4A2A]
Blue:      bg-[#2F80ED]
Radius:    rounded-md (6px) atau rounded-none
Font:      font-['Space_Grotesk']
```
