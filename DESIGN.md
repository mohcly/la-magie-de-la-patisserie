# Design System: The Digital Curator

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Curator."** This isn't just an e-commerce platform; it is a high-end editorial gallery where the product is treated as a masterpiece. 

To achieve a signature, premium feel, we move away from "templated" layouts. We embrace **intentional asymmetry**, where oversized typography overlaps with imagery, and **breathing room** takes precedence over information density. We reject the rigid constraints of the 1px border, opting instead for a tactile, layered approach that mimics the physical experience of stacking fine Italian vellum and frosted glass. The goal is to evoke the sensory richness of a Tiramisu—layers of depth, soft textures, and bold, sophisticated flavors.

---

## 2. Colors: Tonal Depth & The No-Line Rule
The palette is rooted in the ingredients of the craft: the bitterness of espresso, the warmth of cocoa, and the richness of mascarpone.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders for sectioning or containment. 
Boundaries must be defined through:
- **Background Shifts:** Transitioning from `surface` (#fefae9) to `surface-container-low` (#f8f4e3).
- **Tonal Contrast:** Using `surface-container-highest` (#e6e3d2) to anchor a specific content block against a lighter background.

### Surface Hierarchy & Nesting
Treat the UI as a physical arrangement of materials. 
- **Base Layer:** `surface` (#fefae9) is your canvas.
- **In-Page Sections:** Use `surface-container-low` for large content blocks.
- **Nested Components:** Place a `surface-container-lowest` (#ffffff) card inside a `surface-container` (#f2eedd) section to create a soft, "lifted" appearance without a single line of code.

### The Glass & Gradient Rule
To achieve "High-End Glassmorphism," floating elements (like navigation bars or hovering price tags) should use a semi-transparent `surface-container-lowest` with a `backdrop-filter: blur(20px)`. 
- **Signature Gradient:** Use a subtle radial gradient transitioning from `primary` (#271310) to `primary_container` (#3e2723) for hero CTAs to give them a "roasted espresso" sheen that flat hex codes cannot replicate.

---

## 3. Typography: The Editorial Voice
The typography is a dialogue between Italian heritage (`Playfair Display`) and modern precision (`Manrope`).

- **Display & Headlines (Playfair Display):** These are the "Curator's Voice." Use `display-lg` and `headline-lg` with generous tracking and occasional italicization for emphasis. Don't be afraid to let headers overlap image masks to create a high-fashion editorial look.
- **Body & Labels (Manrope):** These provide the "Scientific Precision." Use `body-lg` for descriptions. Manrope’s geometric clarity balances the ornate nature of the serif headlines, ensuring the brand feels "Artisanal yet Modern."
- **Visual Hierarchy:** Maintain a dramatic scale difference between your `display` and `body` styles. High contrast in size communicates luxury and confidence.

---

## 4. Elevation & Depth: Tonal Layering
In this system, depth is felt, not seen. We abandon traditional "Material" shadows in favor of ambient light.

- **The Layering Principle:** Stack `surface-container` tiers to create hierarchy. A `surface-container-high` element placed on a `surface` background provides all the "elevation" needed.
- **Ambient Shadows:** If an element must float (e.g., a modal), use a shadow with a 40px–60px blur and 5% opacity. Use a tinted shadow—color it with `primary` (#271310) at a very low alpha—to simulate the way light interacts with dark espresso surfaces.
- **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline_variant` at 15% opacity. It should be a suggestion of a line, not a hard stop.
- **Arch Clipping:** All primary product imagery must utilize the **Soft Arch Clipping Mask** (Top-rounded or full arch). This softens the "digital" feel and mimics the architectural elegance of an Italian pasticceria.

---

## 5. Components: The Artisanal Toolkit

### Buttons
- **Primary:** `primary` background, `on_primary` text. No borders. Use `xl` (1.5rem) corner radius for a soft, pill-like feel.
- **Secondary:** `surface-container-highest` background. Subtle, tonal, and tactile.
- **Interactive States:** On hover, primary buttons should shift to a subtle gradient rather than a flat color change.

### Cards & Lists
- **The Divider Rule:** Strictly forbid horizontal rules (`<hr>`). Separate list items using `surface-container-low` backgrounds or increased vertical spacing (32px+).
- **Product Cards:** Use the `surface-container-lowest` color. Images should sit in a "Soft Arch" mask at the top of the card.

### Floating Elements (Glassmorphism)
- **Floating Navigation:** Positioned at the bottom or top of the viewport. Background: `surface` at 70% opacity with 20px blur. This ensures the rich espresso and cocoa colors of the page content bleed through beautifully as the user scrolls.

### Selection Controls
- **Chips:** Use `secondary_container` for selected states. They should feel like small "tasting notes" scattered on the page.
- **Input Fields:** No bottom-line or boxed borders. Use `surface-container-high` as a full-color fill with `sm` (0.25rem) roundedness.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use asymmetrical layouts. Place an image on the right and a `display-lg` header that partially overlaps it on the left.
- **Do** use the `tertiary` (Gold) sparingly. It is an accent—for a "Premium" badge, a star rating, or a single word of emphasis.
- **Do** favor vertical white space over structural dividers. Let the content breathe.

### Don't:
- **Don't** use 1px solid borders. It breaks the "Digital Curator" illusion and makes the site look like a standard template.
- **Don't** use pure black (#000000). Use the `primary` espresso brown for all "dark" elements to maintain warmth.
- **Don't** use sharp corners. Refer to the Roundedness Scale; even `none` should be avoided in favor of `sm` or `md` to maintain the "creamy" mascarpone aesthetic.
- **Don't** crowd the interface. If a screen feels full, it isn't luxurious. Remove elements until only the essentials remain.