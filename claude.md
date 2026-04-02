# claude.md — Szó Ami Szó G&D Kézműves Cukrászda
## Master Project Specification for Claude Code

---

## 0. FIRST THING YOU MUST DO

A PDF containing the brand's design system has been uploaded alongside this prompt.
**Read the PDF in full before writing any CSS or choosing any font.**
Extract and apply:
- Exact color hex values (assign to CSS variables as specified below)
- Font names, weights, and use cases
- Any spacing, sizing, or typographic scale rules
- Any logo, icon, or decorative element guidance

If the PDF specifies anything that conflicts with the defaults in this document, **the PDF takes precedence.**

---

## 1. Project Overview

**Client:** Szó Ami Szó G&D Kézműves Cukrászda
**Type:** Ultra-premium artisanal bakery & pastry shop
**Location:** Balatonkenese / Balatonakarattya, Lake Balaton, Hungary
**Owners:** An elderly mother and her master pastry chef son — generational craft, world-class product
**Current presence:** Facebook + Instagram only. No website.
**Target audience:** Local loyal regulars + Balaton tourists (Hungarian + international, English-speaking)

**The feeling this website must evoke:**
Walking into one of the world's great patisseries — Ladurée, Pierre Hermé — but feeling the warmth of a family kitchen. Timeless, emotional, never corporate, never folksy. The digital embodiment of something made with your whole self.

---

## 2. Design Philosophy: "Heirloom Modernism"

The central tension to hold: **Parisian luxury + Hungarian family soul.**

Every design decision passes this test: *Does this feel handmade with care, or manufactured?*

- Never clinical. Never rustic. Never generic.
- Generous whitespace. Let things breathe.
- Typography does the heavy lifting — layout supports it, not the reverse.
- Animations are slow, deliberate, and never decorative for their own sake.
- Photography (when added) leads. The design frames it, never competes.

---

## 3. CSS Design System

Define all of the following as CSS custom properties at `:root`.
**Values below are fallback defaults. Override with PDF values if provided.**

```css
:root {
  /* --- COLORS --- */
  /* Base backgrounds */
  --color-bg-primary: #F7F2EA;       /* warm parchment — main page bg */
  --color-bg-secondary: #FDFAF5;     /* soft cream — card / section bg */
  --color-bg-dark: #1E1008;          /* near-black espresso — dark sections */

  /* Text */
  --color-text-primary: #2C1A0E;     /* deep espresso brown */
  --color-text-secondary: #8C7B6B;   /* warm taupe — captions, meta */
  --color-text-inverse: #F7F2EA;     /* light text on dark bg */

  /* Accents */
  --color-gold: #C9A84C;             /* antique gold — sparingly */
  --color-terracotta: #B5614A;       /* terracotta — very sparingly */
  --color-border: #E2D9CC;           /* subtle warm border */

  /* Image placeholders — replace with real images later */
  --color-placeholder-hero: #3D2410;
  --color-placeholder-story: #5C3D28;
  --color-placeholder-craft: #7A5140;
  --color-placeholder-gallery-1: #6B4430;
  --color-placeholder-gallery-2: #8C6050;
  --color-placeholder-gallery-3: #4A2E1A;
  --color-placeholder-gallery-4: #9E7055;
  --color-placeholder-gallery-5: #5E3A22;
  --color-placeholder-gallery-6: #7D5238;

  /* --- TYPOGRAPHY --- */
  /* Override font names below with PDF-specified values */
  --font-serif: 'Cormorant Garamond', Georgia, serif;       /* headlines, body */
  --font-body: 'EB Garamond', Georgia, serif;               /* body text */
  --font-mono: 'DM Mono', 'Courier New', monospace;         /* nav, buttons, UI */
  --font-accent: 'Cormorant Upright', serif;                /* pull quotes, names */

  /* Type scale */
  --text-hero: clamp(3.5rem, 8vw, 7rem);
  --text-h1: clamp(2.5rem, 5vw, 4.5rem);
  --text-h2: clamp(1.8rem, 3.5vw, 3rem);
  --text-h3: clamp(1.3rem, 2.5vw, 1.8rem);
  --text-body: clamp(1rem, 1.5vw, 1.125rem);
  --text-small: 0.8125rem;
  --text-mono-ui: 0.75rem;

  /* --- SPACING --- */
  --space-section: clamp(5rem, 12vw, 10rem);
  --space-block: clamp(2rem, 5vw, 4rem);
  --space-gap: clamp(1rem, 2.5vw, 2rem);
  --container-max: 1400px;
  --container-padding: clamp(1.5rem, 5vw, 5rem);

  /* --- MOTION --- */
  --transition-slow: 0.7s cubic-bezier(0.25, 0.1, 0.25, 1);
  --transition-medium: 0.4s cubic-bezier(0.25, 0.1, 0.25, 1);
  --transition-fast: 0.2s ease;

  /* --- BORDERS / RADIUS --- */
  --radius-soft: 2px;     /* almost no radius — refined, not bubbly */
  --border-thin: 1px solid var(--color-border);
  --border-gold: 1px solid var(--color-gold);
}
```

---

## 4. Font Loading

Load via Google Fonts. Include these weights:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&family=Cormorant+Upright:wght@300;400;500&family=DM+Mono:wght@300;400&family=EB+Garamond:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
```
**If the PDF specifies different fonts, replace these entirely.**

---

## 5. Tech Stack

- **Single HTML file** — no build step, no framework, no dependencies
- **Vanilla JS + CSS** — maximum portability, easy client handoff
- **Google Fonts** — via CDN link in `<head>`
- **Google Sheets CSV** — public CSV URL fetched client-side for the menu
- **Intersection Observer API** — for scroll-reveal animations
- **No external JS libraries**

---

## 6. HTML Structure

```html
<!DOCTYPE html>
<html lang="hu" data-lang="hu">
<head>
  <!-- meta, fonts, title -->
</head>
<body>
  <nav id="nav">…</nav>
  <main>
    <section id="hero">…</section>
    <section id="story">…</section>
    <section id="craft">…</section>
    <section id="menu">…</section>
    <section id="gallery">…</section>
    <section id="visit">…</section>
  </main>
  <footer id="footer">…</footer>
</body>
</html>
```

---

## 7. Navigation Bar

**Behavior:**
- Fixed/sticky top. Starts transparent over hero, transitions to `var(--color-bg-primary)` with a subtle border-bottom on scroll (threshold: 80px from top).
- No hamburger. On mobile: collapse nav links behind a minimal toggle (3 short lines, monospaced style).

**Elements (left to right):**
1. Logo / wordmark — "Szó Ami Szó" in `var(--font-accent)`, small caps, letter-spaced
2. Nav links (center or right): `A Mi Történetünk` · `Kézművesség` · `Napi Menü` · `Galéria` · `Látogatás`
3. Language toggle (far right): `HU / EN` — `var(--font-mono)`, `var(--text-mono-ui)`, uppercase. Active language in `var(--color-gold)`.

**Styling:**
- Font: `var(--font-mono)`, uppercase, `var(--text-mono-ui)`, letter-spacing: 0.12em
- Links: no underline, `var(--color-text-secondary)` default, `var(--color-text-primary)` on hover
- Transition: color `var(--transition-fast)`

---

## 8. Section 01 — Hero

**Layout:** Full viewport height (`100dvh`). Centered content, vertically and horizontally.

**Image placeholder:**
```css
.hero-bg {
  background-color: var(--color-placeholder-hero);
  /* Later: background-image: url('hero.jpg'); background-size: cover; background-position: center; */
}
```
Apply a dark overlay: `background: linear-gradient(to bottom, rgba(30,16,8,0.4) 0%, rgba(30,16,8,0.2) 50%, rgba(30,16,8,0.55) 100%)`

**Content:**
```
[HU] Amit a kezünk csinál, azt a szívünk érzi.
[EN] Made by hand. Felt by heart.
```
Headline: `var(--font-serif)`, `var(--text-hero)`, font-weight 300, color `var(--color-text-inverse)`, italic

Subline:
```
[HU] Kézműves sütemények a Balaton partján — minden reggel frissen sütve.
[EN] Artisanal pastries on the shores of Lake Balaton — baked fresh, every morning.
```
Font: `var(--font-mono)`, `var(--text-small)`, uppercase, letter-spacing 0.2em, color `rgba(253,250,245,0.75)`, margin-top: 2rem

**Scroll indicator:** A single thin vertical line (2px, 40px tall, `var(--color-gold)`, 50% opacity) centered at the bottom, with a slow fade-in animation (delay 1.5s). No text, no arrow.

**Animation on load:**
- Headline fades in and rises 20px over 1.2s, delay 0.3s
- Subline fades in over 1s, delay 0.8s
- Scroll indicator fades in over 0.8s, delay 1.5s

---

## 9. Section 02 — Our Story (A Mi Történetünk)

**Layout:** Two-column on desktop (image left, text right). Single column on mobile.

**Image placeholder (left column):**
```css
background-color: var(--color-placeholder-story);
aspect-ratio: 3/4;
/* Later: real photo of mother or son at work */
```

**Text content (right column):**

Opening label (above headline):
```
[HU] A mi történetünk  [EN] Our Story
```
Font: `var(--font-mono)`, uppercase, `var(--text-mono-ui)`, `var(--color-gold)`, letter-spacing 0.2em

Headline:
```
[HU] Két kéz. Egy tudás. Egy évtizedek óta tartó szeretet.
[EN] Two hands. One knowledge. A love that spans decades.
```
Font: `var(--font-serif)`, `var(--text-h1)`, font-weight 300, italic

Body copy — paragraph 1:
```
[EN] She learned to fold dough before she learned to drive. Her son learned it from watching her — flour on the counter at 5am, the kitchen warm before the rest of the house woke up. Szó Ami Szó is not a concept or a brand. It's a conversation between two people who believe that the best thing you can put on a table is something made with your whole self.

[HU] Még sofőrként nem, de tésztát hajtogatni már tudott, mielőtt levizsgázott volna. A fia nézve tanulta el — liszt a pulton hajnali 5-kor, a konyha meleg, még mielőtt a ház többi lakója ébredt volna. A Szó Ami Szó nem egy koncepció vagy egy márka. Egy párbeszéd két ember között, akik hisznek abban, hogy az asztalra legjobban azt lehet tenni, amit az ember teljes szívvel csinált.
```

Pull quote (styled differently — `var(--font-accent)`, large, `var(--color-gold)`, centered or offset):
```
[EN] "Balatonkenese isn't Paris. That's exactly the point."
[HU] „Balatonkenese nem Párizs. Ez pontosan a lényeg."
```

Body copy — paragraph 2:
```
[EN] The rétes here is made with the same discipline as anything you'd find on Rue du Bac — but it carries the memory of a specific kitchen, a specific summer, a specific set of hands that have never once taken a shortcut.

[HU] Az itt készülő rétes ugyanolyan fegyelemmel készül, mint bármi, amit a Rue du Bac-on kapna az ember — de magában hordoz egy konkrét konyha, egy konkrét nyár, egy konkrét kézpár emlékét, amely soha, egyetlen egyszer sem vett vissza.
```

Font for body: `var(--font-body)`, `var(--text-body)`, line-height 1.85

---

## 10. Section 03 — The Craft (Kézművesség)

**Layout:** A 2-column grid on desktop of editorial "item cards". Each card: image placeholder top, name, short description, price (optional).

**Items to include (6 total):**

| ID | HU Name | EN Name | HU Description | EN Description |
|---|---|---|---|---|
| croissant | Croissant | Croissant | 72 óra laminálás. Magyar vaj. Egy kéreg, amelyet hallani. | 72 hours of lamination. Hungarian butter. A crust you can hear. |
| kakao-csiga | Kakaós csiga | Chocolate swirl | Puha, sötét, és határeset. Az a fajta, amit állva eszel meg. | Soft, dark, and borderline dangerous. The kind you eat standing up. |
| retes | Rétes | Strudel | Az ő receptje. Változatlan. Nem modernizálva. | Her recipe. Not adjusted. Not modernized. |
| kovaszos-kenyer | Kovászos kenyér | Sourdough bread | Három napos kovász. Öntöttvas. Türelem. | Three-day starter. Cast iron. Patience. |
| linzer | Linzer | Linzer cookies | Az a linzer, amiért visszajönnek. | The linzer people come back for. |
| sezonalis | Szezonális különlegesség | Seasonal special | Mindig más. Mindig aktuális. Mindig friss. | Always different. Always seasonal. Always fresh. |

**Card styling:**
- Image placeholder: `var(--color-placeholder-craft)`, aspect-ratio 4/3
- Item name: `var(--font-serif)`, `var(--text-h3)`, font-weight 400
- Description: `var(--font-body)`, `var(--text-body)`, `var(--color-text-secondary)`, italic
- Thin gold bottom border on hover: `border-bottom: var(--border-gold)`
- No drop shadows. No border-radius beyond `var(--radius-soft)`.

---

## 11. Section 04 — Daily Menu (Napi Menü)

### Google Sheets Integration

**Sheet URL structure:**
The owner publishes their Google Sheet as a public CSV. The URL format is:
```
https://docs.google.com/spreadsheets/d/SHEET_ID/export?format=csv&gid=0
```
Define `SHEET_CSV_URL` as a constant at the top of the JS block. Use a clearly commented placeholder:
```js
const SHEET_CSV_URL = 'REPLACE_WITH_GOOGLE_SHEETS_CSV_URL';
```

**Expected CSV columns (in order):**
```
category, name_hu, name_en, description_hu, description_en, price, available, highlight, allergens
```

**Fetch and render logic:**
1. On page load, fetch the CSV URL
2. Parse CSV (handle quoted fields with commas)
3. Filter: only render rows where `available` === `TRUE`
4. Group by `category`
5. Render each category as a titled section
6. Items where `highlight === TRUE` get a small gold dot or "◆" marker
7. Show `allergens` as small text below description if non-empty
8. If fetch fails, show a graceful fallback message:
   ```
   [HU] A mai menüért kérjük látogasson el Facebook oldalunkra.
   [EN] For today's menu, please visit our Facebook page.
   ```

**Menu card layout:**
- Left: item name (HU or EN based on active language) + description
- Right: price in Ft (right-aligned, `var(--font-mono)`)
- Full-width separator line between items: `var(--color-border)`
- Category headers: `var(--font-mono)`, uppercase, letter-spacing 0.2em, `var(--color-gold)`

**Section header:**
```
[HU] Napi Menü
[EN] Today's Menu
```
Followed by the current date, auto-generated in JS:
```js
// Format: "2025. június 14." (HU) or "June 14, 2025" (EN)
```

---

## 12. Section 05 — Gallery (Galéria)

**Layout:** CSS masonry grid. 3 columns on desktop, 2 on tablet, 1 on mobile.

**Placeholders:** 6 blocks with varying heights to demonstrate masonry rhythm.
```
Block 1: var(--color-placeholder-gallery-1), height: 380px
Block 2: var(--color-placeholder-gallery-2), height: 260px
Block 3: var(--color-placeholder-gallery-3), height: 440px
Block 4: var(--color-placeholder-gallery-4), height: 300px
Block 5: var(--color-placeholder-gallery-5), height: 360px
Block 6: var(--color-placeholder-gallery-6), height: 280px
```

CSS masonry implementation:
```css
.gallery-grid {
  columns: 3;
  column-gap: var(--space-gap);
}
.gallery-item {
  break-inside: avoid;
  margin-bottom: var(--space-gap);
}
@media (max-width: 900px) { .gallery-grid { columns: 2; } }
@media (max-width: 600px) { .gallery-grid { columns: 1; } }
```

**Hover state:** Subtle scale(1.02) + brightness(1.05), transition `var(--transition-slow)`
**No lightbox for now.** Add later.

---

## 13. Section 06 — Visit Us (Látogatás)

**Layout:** Two columns. Left: info. Right: embedded Google Map.

**Info content:**

Address label: `var(--font-mono)`, uppercase, `var(--text-mono-ui)`, `var(--color-gold)`

```
[HU / EN] Szó Ami Szó G&D Kézműves Cukrászda
Balatonkenese / Balatonakarattya, Hungary
```

Opening hours (placeholder — confirm with client):
```
[HU]
Hétfő – Szerda: Zárva
Csütörtök – Péntek: 07:00 – 14:00
Szombat – Vasárnap: 07:00 – 15:00

[EN]
Monday – Wednesday: Closed
Thursday – Friday: 7:00 AM – 2:00 PM
Saturday – Sunday: 7:00 AM – 3:00 PM
```

Note (italic, small, terracotta):
```
[HU] Az áruk elfogyhatnak a zárás előtt. Érdemes korán érkezni.
[EN] Items may sell out before closing. We recommend arriving early.
```

**Google Maps embed:**
```html
<iframe
  src="https://www.google.com/maps/embed?pb=REPLACE_WITH_ACTUAL_EMBED_URL"
  width="100%"
  height="420"
  style="border:0; filter: sepia(20%) saturate(80%) brightness(95%);"
  allowfullscreen
  loading="lazy">
</iframe>
```
Apply the CSS filter to match warm site palette.

---

## 14. Footer

Minimal. Dark background (`var(--color-bg-dark)`), light text.

```
Szó Ami Szó G&D Kézműves Cukrászda
[social icons: Facebook · Instagram — SVG inline, no external icon library]
© 2025 Szó Ami Szó. Minden jog fenntartva. / All rights reserved.
```

Font: `var(--font-mono)`, `var(--text-mono-ui)`, `var(--color-text-inverse)` at 60% opacity
Language toggle mirrored here as well.

---

## 15. Language Toggle System

**Implementation:**
```js
const LANG = {
  hu: { /* all HU strings keyed by ID */ },
  en: { /* all EN strings keyed by ID */ }
};

let currentLang = 'hu';

function setLang(lang) {
  currentLang = lang;
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    if (LANG[lang][key]) el.innerHTML = LANG[lang][key];
  });
  document.documentElement.setAttribute('lang', lang);
  // Update toggle active state
}
```

All copy-bearing elements get `data-i18n="key_name"`. All string keys must be defined in both `LANG.hu` and `LANG.en`.

Menu section re-renders on language toggle (re-reads from already-fetched data).
Date also re-formats on language toggle.

---

## 16. Scroll Reveal Animations

Use `IntersectionObserver`. Apply to all major section elements.

```js
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('is-visible');
      revealObserver.unobserve(entry.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));
```

CSS:
```css
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity var(--transition-slow), transform var(--transition-slow);
}
.reveal.is-visible {
  opacity: 1;
  transform: translateY(0);
}
```

Apply `.reveal` class to: section headlines, body paragraphs, craft cards, menu categories, gallery items, visit info blocks.
Stagger multiple children using `transition-delay` in increments of 0.1s.

---

## 17. Responsive Breakpoints

```css
/* Mobile first */
/* Base: < 600px */
@media (min-width: 600px)  { /* tablet portrait */ }
@media (min-width: 900px)  { /* tablet landscape / small desktop */ }
@media (min-width: 1200px) { /* desktop */ }
@media (min-width: 1600px) { /* large desktop — max-width container clamps */ }
```

Key mobile behaviors:
- Nav collapses to minimal toggle
- Hero headline uses `clamp` min (already defined)
- Story section: single column
- Craft grid: single column
- Menu: full width, price right-aligned still
- Gallery: single column
- Visit: single column (map below info)

---

## 18. Performance & Polish

- `font-display: swap` on all font loads (handled by Google Fonts `display=swap` param)
- `loading="lazy"` on all images and iframes
- CSS `content-visibility: auto` on below-fold sections for paint performance
- No scroll-jacking. No parallax. Smooth scroll via `html { scroll-behavior: smooth; }`
- `prefers-reduced-motion` media query: disable all `.reveal` transitions and hero animations for users who prefer reduced motion

---

## 19. Build Order

Build in this exact sequence. Do not move to the next phase until the current one is complete and clean.

```
Phase 1 — Foundation
  HTML skeleton, <head>, CSS variables, font loading, reset styles

Phase 2 — Navigation
  Sticky nav, scroll transparency transition, mobile toggle, language toggle UI

Phase 3 — Hero
  Full-viewport, placeholder bg, headline + subline, scroll indicator, load animations

Phase 4 — Our Story
  Two-column layout, placeholder image, all copy (HU + EN), pull quote

Phase 5 — The Craft
  6-item editorial grid, placeholder images, all copy (HU + EN)

Phase 6 — Daily Menu
  CSV fetch logic, parser, render engine, language-aware display, fallback state

Phase 7 — Gallery
  Masonry grid, 6 placeholder blocks, hover states

Phase 8 — Visit Us
  Two-column, info block (HU + EN), map embed placeholder

Phase 9 — Footer
  Dark bg, social links (placeholder hrefs), copyright, language toggle

Phase 10 — Language System
  Wire all data-i18n keys, populate LANG object with all HU + EN strings

Phase 11 — Scroll Reveal
  Apply .reveal classes and IntersectionObserver across all sections

Phase 12 — Responsive Pass
  Test and fix all breakpoints, mobile nav, touch interactions

Phase 13 — Final Polish
  Spacing audit, typography hierarchy check, transition timing, reduced-motion query
```

---

## 20. Handoff Notes (for developer / client)

- **To update the menu:** Edit the connected Google Sheet. Changes reflect on next page load. No code changes needed.
- **To add real photos:** Replace `background-color: var(--color-placeholder-*)` with `background-image: url('...')` + `background-size: cover`.
- **To update opening hours:** Edit the `data-i18n` strings in the JS `LANG` object.
- **To update the map:** Replace the `src` attribute of the `<iframe>` in the Visit section.
- **For the social links:** Replace `href="#"` placeholders in the footer with actual Facebook and Instagram URLs.

---

*End of claude.md — Szó Ami Szó G&D Kézműves Cukrászda*
*Prepared for Claude Code. Upload this file + the brand PDF together as the first prompt.*
