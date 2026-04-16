# Design System Document: The Organic Editorial

## 1. Overview & Creative North Star
This design system is built to transform the digital presence of a sustainable tableware brand from a standard e-commerce interface into a "High-End Editorial" experience. 

**Creative North Star: "The Conscious Curator"**
The aesthetic avoids the "crunchy" or "recycled" clichés of eco-branding. Instead, it adopts a sophisticated, gallery-like approach. We prioritize **intentional structure**, where controlled use of `background` creates breathing room. By maintaining a clean, balanced grid with overlapping elements and floating "glass" containers, we mimic the tactile layering of modern lifestyle publications.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the earth, but executed with digital precision.

### The Color Tokens
*   **Primary (`#40916C`):** The "Lush Forest." Used for high-impact brand moments and primary actions.
*   **Secondary (`#B5836D`):** The "Warm Terracotta." Provides a grounded, clay-like counterpoint to the green.
*   **Tertiary (`#D4A373`):** The "Natural Ochre." Used for accents and highlighting eco-credentials.
*   **Neutral (`#2B2D24`):** The "Deep Moss." Our base for dark text and low-light surfaces.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined solely through background color shifts. To separate a hero from a product grid, transition from `surface` to `surface-container-low`. The UI must feel like a single continuous piece of organic material, not a collection of boxes.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine, fibrous paper.
*   **Deep Background:** `surface-container-lowest`
*   **Standard Section:** `surface`
*   **Floating Cards/Modals:** `surface-bright` with 80% opacity and a 12px backdrop-blur (The Glassmorphism Rule).

### Signature Textures
To add "soul," incorporate subtle gradients. Do not use flat hexes for large CTAs. Instead, use a linear gradient from `primary` (#40916C) to `primary_container` at a 135-degree angle. This provides a soft, satin-like sheen reminiscent of a waxy sugarcane leaf.

---

## 3. Typography: The Editorial Voice
We use typography to bridge the gap between "Industrial Tech" and "Human Craft."

*   **Headlines (Display & Headline Scales):** **Space Grotesk.** A quirky, monospaced-adjacent sans-serif. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create authoritative headers.
*   **Body & Labels (Title, Body, Label Scales):** **Manrope.** A modern geometric sans that ensures high legibility. Use `body-lg` (1rem) with a comfortable line-height (1.5) to maintain a clean, readable feel.

**Hierarchy Note:** Use `tertiary` (#D4A373) for small `label-sm` accents to provide a "hand-stamped" feel to metadata or eco-certifications.

---

## 4. Elevation & Depth
Traditional drop shadows are too "digital" for this system. We use **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-highest` element on a `surface` background to create a "recessed" look. Place a `surface-bright` element on `surface` to create a "protruding" look.
*   **Ambient Shadows:** If a floating element requires a shadow, use a custom shadow: `0px 20px 40px rgba(43, 45, 36, 0.06)`. The shadow is a dark olive-grey, never pure black.
*   **The "Ghost Border" Fallback:** For input fields or necessary boundaries, use `outline-variant` at **15% opacity**.

---

## 5. Components

### Buttons
*   **Primary:** Gradient of `primary` to `primary_container`. Text: `on-primary`. Roundedness: `Moderate` (radius 2).
*   **Secondary:** Ghost style. No background. `outline-variant` (20% opacity) border. Text: `primary`.
*   **Tertiary:** Text-only. `label-md` uppercase with 0.1em letter spacing.

### Cards & Lists
*   **The Container:** Use `surface-container-low`. 
*   **Spacing:** Follow the `Normal` spacing scale (level 2). Ensure consistent 24px-32px gaps between elements.
*   **No Dividers:** Never use horizontal lines. Use a change in background tone or vertical white space to separate list items.

### Input Fields
*   **Style:** Minimalist underline or soft-filled. Use `surface-variant` for the fill. 
*   **State:** On focus, the bottom border transitions to `primary` with a 2px thickness. Roundedness: `Moderate` (radius 2).

### Signature Component: The "Leaf Navigation"
A floating navigation bar using **Glassmorphism**. 
*   Background: `surface` at 70% opacity.
*   Blur: `backdrop-filter: blur(16px)`.
*   Edge: `Ghost Border` (outline-variant @ 10%).

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical image placements to break the grid.
*   **Do** use the `secondary` (#B5836D) color for call-outs regarding "Earth-friendly" or "Compostable" facts.
*   **Do** use `Moderate` roundedness (radius 2) for all containers and interactive elements to soften the interface.

### Don’t:
*   **Don’t** use pure `#000000` for body text. Use `on_surface_variant` to keep the contrast soft and organic.
*   **Don’t** use "pill" buttons (fully rounded) or sharp 0-radius corners. Stick to the `Moderate` scale.
*   **Don’t** use excessive "Spacious" padding; maintain the `Normal` density (level 2) for a professional, balanced UI.

### Accessibility Note:
While we use soft tones, always ensure that text on `surface` or `surface-container` meets WCAG AA standards by using the `on-surface` and `on-background` tokens for all essential reading material.