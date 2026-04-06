# Design System Strategy: The Neon Architect (Deep Navy Edition)

## 1. Overview & Creative North Star: "The Digital Blueprint"
The Creative North Star for this design system is **The Digital Blueprint**. We are moving away from the "standard" dark-mode portfolio template to create a space that feels like a high-end, architectural visualization of code. 

To achieve an editorial, premium feel, we break the "template" look by utilizing **intentional asymmetry** and **tonal depth**. Instead of a centered, linear scroll, we embrace large, offset typography and overlapping glass containers that mimic physical layers of schematics. This system isn't just about showing work; it’s about projecting an aura of technical mastery and structural elegance.

---

## 2. Colors & Surface Philosophy
The palette transitions from a structural `background` (#0b0e16) to a high-energy `primary` (#7fafff). We do not use color simply for decoration; we use it to represent "energy" flowing through the blueprint.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning. 
Boundaries must be defined solely through background color shifts or subtle tonal transitions. For example, a "Work Experience" section should be a `surface-container-low` block sitting on a `background` page, creating a soft, edge-less transition that feels integrated, not boxed in.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—stacked sheets of frosted glass.
*   **Base Layer:** `surface` (#0b0e16) - The foundation.
*   **Section Layer:** `surface-container-low` (#10131d) - Sub-regions or section backgrounds.
*   **Interaction Layer:** `surface-container-high` (#1c1f2b) - Hover states or active modules.
*   **Floating Layer:** `surface-container-highest` (#222532) - Modals or pop-overs.

### The "Glass & Gradient" Rule
To achieve the "Neon" vibe without looking dated, use **Glassmorphism**. Floating elements should use `surface-variant` at 40-60% opacity with a `backdrop-filter: blur(20px)`. 

### Signature Textures
Main CTAs and Hero accents must utilize a gradient transition from `primary` (#7fafff) to `secondary` (#9392ff). This "Vibrant Blue to Purple" shift provides the visual "soul" that flat colors cannot achieve.

---

## 3. Typography: The Technical Editorial
We use **Plus Jakarta Sans** across all levels to maintain a cohesive, tech-focused aesthetic. The hierarchy relies on extreme scale contrast.

*   **Display (Large/Medium):** Used for "Statement" text. Letter spacing should be set to `-0.02em` to feel tighter and more premium.
*   **Headline (Small/Medium):** Used for section titles. These should often be placed asymmetrically (e.g., far-left or vertical) to break the grid.
*   **Title (Medium/Small):** For card headers and navigation. Use `on-surface-variant` (#a9aab6) for a muted, sophisticated secondary read.
*   **Body (Large/Medium):** Primary reading. Line height must be generous (1.6x) to ensure the dark background doesn't "choke" the letterforms.
*   **Labels:** Always uppercase with `+0.05em` letter spacing to mimic architectural annotations.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden. We convey depth through **Tonal Layering** and **Luminous Shadows**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. The subtle shift in hex code creates a natural "lift" that feels modern and architectural.
*   **Luminous Shadows:** When a "floating" effect is required (e.g., a primary button), use a shadow tinted with the `primary` color (#7fafff) at 10% opacity, with a 32px blur. This mimics the "neon glow" of the Architect vibe.
*   **The "Ghost Border":** If a separator is required for accessibility, use the `outline-variant` token at **15% opacity**. Never use 100% opaque lines.
*   **Cyan Contrast:** Use the `tertiary` (#68d3ff) token sparingly for small "status" indicators or tiny accents to provide a sharp, high-contrast focal point against the deep navy.

---

## 5. Components

### Buttons
*   **Primary:** Gradient background (`primary` to `primary-dim`). Border-radius: `ROUND_EIGHT` (0.5rem). No border.
*   **Secondary:** Ghost style. `surface-container-high` background with a `primary` label.
*   **Tertiary:** No background. `primary` label with a "Cyan glow" underline (2px) on hover.

### Cards (The "Blueprint" Card)
*   **Styling:** Background of `surface-container-low`. No borders. 
*   **Hover:** Transition background to `surface-container-high` and add a subtle `primary` outer glow.
*   **Rule:** Forbid divider lines within cards. Use `body-sm` typography and vertical padding (1.5rem) to separate internal content.

### Chips (Tech Stack Tags)
*   **Styling:** `surface-variant` background at 50% opacity. `on-surface-variant` text. 
*   **Shape:** Full rounded (`9999px`) to contrast against the `ROUND_EIGHT` corners of the containers.

### Input Fields
*   **Styling:** `surface-container-lowest` background. 
*   **Focus State:** The "Ghost Border" becomes 100% opaque `primary`, accompanied by a subtle `primary` glow.

### Additional Component: The "Architectural Lead-in"
*   A thin vertical line (using `primary-dim` at 20% opacity) that connects a headline to a body paragraph, visually "guiding" the eye like a blueprint lead line.

---

## 6. Do's and Don'ts

### Do:
*   **Use Asymmetry:** Place your hero text off-center. Let elements overlap.
*   **Embrace Negative Space:** Give your content room to breathe. Use the `xl` spacing scale between sections.
*   **Tone over Texture:** Use color shifts to define areas rather than patterns or lines.

### Don't:
*   **No Pure Black:** Never use #000000 for backgrounds (except for the `surface-container-lowest` in specific nested contexts). Stick to the Navy palette.
*   **No High-Contrast Borders:** Avoid 1px solid white or light gray lines; they shatter the "neon" atmosphere.
*   **No Default Shadows:** Standard black drop-shadows will make the Navy background look "muddy." Use color-tinted glows only.
*   **No Center-Alignment Obsession:** Avoid making every section look the same. Vary the layout to keep the "Architect" feel dynamic.