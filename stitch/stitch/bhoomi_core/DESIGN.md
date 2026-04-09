# Design System Strategy: The Sovereign Earth Intelligence

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Cartographer"**

This design system moves away from the "app-like" clutter of typical SaaS platforms. Instead, it adopts the persona of a high-end, authoritative digital archive. It is a "Digital Cartographer"—precise, silent, and indisputable.

To achieve a "government-grade" futuristic feel, we avoid the tropes of glowing neon and busy HUDs. We utilize **Intentional Asymmetry** and **Massive Negative Space** to command authority. By breaking the rigid 12-column grid with overlapping data modules and offset typography, we create an editorial experience that feels custom-built for high-stakes decision-making. The layout should feel like a premium printed map brought to life through fluid, glass-like interactions.

---

## 2. Colors & Atmospheric Depth

Our palette is grounded in the stability of the earth and the vastness of the sky. We use a "High-Contrast, Low-Noise" approach.

### The "No-Line" Rule
**Borders are a design failure.** In this system, 1px solid borders for sectioning are strictly prohibited. We define space through:
*   **Tonal Shifts:** Moving from `surface` (#f8faf9) to `surface-container-low` (#f2f4f3).
*   **Optical Weight:** Using large typography or iconography to anchor a section without boxing it in.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of translucent materials.
*   **Base Layer:** `surface` (#f8faf9) for the global canvas.
*   **Secondary Layer:** `surface-container` (#eceeed) for main content hubs.
*   **Tertiary Layer:** `surface-container-highest` (#e1e3e2) for focused sidebars or data panels.
*   **Interactive Layer:** `surface-container-lowest` (#ffffff) for active cards, creating a "lifted" effect against the slightly darker container.

### The "Glass & Gradient" Rule
To bridge the gap between "grounded" and "futuristic," use **Glassmorphism** for floating utility panels. Apply `surface-variant` at 60% opacity with a `24px` backdrop blur.
*   **Signature Texture:** Main action areas should utilize a subtle linear gradient: `primary` (#02241d) to `primary-container` (#1a3a32). This adds a "weighted silk" texture that flat colors lack.

---

## 3. Typography: The Authoritative Voice

We pair the geometric precision of **Public Sans** with the utilitarian clarity of **Inter**.

*   **Display & Headlines (Public Sans):** These are our "Statement" layers. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create an authoritative, editorial impact. Headlines should be used sparingly to define major sectors of land data.
*   **Titles & Body (Inter):** These represent our "Data" layers. Inter’s tall x-height ensures that complex coordinates and land metrics remain legible at small sizes (`body-sm`).
*   **Labeling (Inter):** Use `label-md` (0.75rem) in All-Caps with +0.05em tracking for metadata. This mimics the labeling found on professional topographical maps.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows are too "web-standard." We use **Ambient Depth**.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface-container-lowest` (#ffffff) element sitting on a `surface-container-low` (#f2f4f3) background provides all the separation required.
*   **Ambient Shadows:** For floating AI-insight modals, use a shadow with a `48px` blur and `4%` opacity, tinted with `primary` (#02241d). It shouldn't look like a shadow; it should look like a soft occlusion of light.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline-variant` (#c1c8c4) at 15% opacity. It must be felt, not seen.

---

## 5. Signature Components

### Buttons (The Precision Actuator)
*   **Primary:** A solid block of `primary` (#02241d) with `on-primary` (#ffffff) text. Use `DEFAULT` (0.25rem) rounding. No gradients on buttons; they must feel like heavy, physical switches.
*   **Secondary:** `surface-container-highest` (#e1e3e2) background with `on-surface` (#191c1c) text. This blends into the UI until hovered.

### Input Fields (The Data Entry)
*   **Form:** Forbid the "box" look. Use a bottom-only stroke using `outline` (#717975) at 30% opacity. When focused, transition to a `primary` (#02241d) 2px bottom stroke. This maintains the "clean, government-grade" minimal aesthetic.

### Cards & Lists (The Dossier)
*   **Forbid Divider Lines:** Use `24px` or `32px` of vertical whitespace to separate list items. The `spacing` parameter is currently set to `2`, indicating a normal, more spacious feel. This aligns well with the request for significant whitespace between list items.
*   **Interaction:** On hover, a list item should shift its background to `surface-container-high` (#e6e9e8) with a soft `md` (0.375rem) corner radius.

### AI Insight Chips
*   Use `secondary-container` (#d7e2ff) with `on-secondary-container` (#5a647c). These should feel like "labels" pinned to a map—small, precise, and non-intrusive.

### Data Visualization (The Pulse)
*   Use `tertiary` (#2b1c03) for earth-related data points and `secondary` (#545e76) for water/infrastructure metrics. Graphs should never have background grids—only a single "Baseline" axis.

---

## 6. Do’s and Don'ts

### Do:
*   **Embrace Asymmetry:** Offset your text columns. Let a map occupy 65% of the screen while data cards overlap the edge of the map.
*   **Use Mono-spacing for Coordinates:** Use Inter for numerical data to ensure column alignment in data tables.
*   **Respect the "Grounded" Palette:** Use `tertiary-fixed` (#fcdeb6) sparingly for "Warning" states instead of harsh oranges; it feels more like natural earth/sand.

### Don’t:
*   **Don't use 100% Black:** Always use `on-background` (#191c1c) for text to maintain the sophisticated, deep-navy ink feel.
*   **Don't use Rounded "Pill" Buttons:** Stick to the `DEFAULT` (0.25rem) or `sm` (0.125rem) rounding. This isn't a social media app; it's a precision instrument.
*   **Don't Over-animate:** Transitions should be "Linear-Out / Slow-In" and fast (200ms). Movement should feel like a high-end camera lens snapping into focus.

---

**Director’s Final Note:**
This system is about the tension between the organic (the land) and the digital (the AI). Keep your layouts breathing. If the screen feels full, remove a container, don't shrink the text. Authority is found in the space between the data points.