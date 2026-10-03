# Hank — Generative Art

> A seed-based generative system for drifting ellipse compositions.  
> A reproducible catalogue of computational motion studies.

---

## What is this?

**Hank** is a generative design system that drifts a single stroked ellipse across a two-tone field. Its position, rotation, scale, and colour all oscillate independently — producing a continuous, never-repeating trace that is neither fully planned nor fully random, but **emergent**.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the coiled unit of yarn — a single continuous strand, wound and rewound, its colour shifting as it turns — **Hank** translates that logic into code.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Hank-Generative-Art/)**

---

## The System

The generator combines two layers:

| Layer | Description |
|-------|-------------|
| **Ellipse drift** | A stroked ellipse translated, rotated, and scaled per frame — bounding against the canvas edges. |
| **Colour oscillation** | The stroke colour drifts through RGB space, bounded by the spectrum. |

Both layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Ellipse count** — a single continuous stroked ring
- **Stroke width** — derived from canvas scale
- **Drift velocity** — X/Y translation, width/height scale, rotation rate, all seeded
- **Colour range** — RGB oscillation bounded per seed
- **Palette pair** — two-tone diagonal gradient drawn from the palette

---

## Structure

```
Hank-Generative-Art/
├── index.html          ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── hank-tote.png
│   ├── hank-tee.png
│   └── hank-cushion.png
├── Hank.jpg            ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live animation** — cover, plate, and framed print drift continuously
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download the current frame directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Each composition is drawn from a curated palette of 180+ named colours:

- **Palette pair** — two colours chosen per seed, blended into a diagonal gradient background
- **Stroke colour** — an RGB value that drifts through the spectrum, bounded per seed
- **Tile bias** — the palette includes deep tones, muted mid-tones, and bright accents, giving each seed a distinct character

Each seed selects a unique combination — no two compositions share the same palette.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Static seeded stills for archive and surfaces — live `requestAnimationFrame` loops for cover, plate, and framed print
- `IntersectionObserver` pauses off-screen animation; `visibilitychange` pauses all loops when the tab is hidden
- `prefers-reduced-motion` respected

---

## About

**Hank** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Hank** is an attempt to render that logic visible.

> *A line drifts across a field — and in that drift, colour remembers itself.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Hank — Autumn 2026

---

<p align="center">
  <em>Generative Ellipse Drift</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>