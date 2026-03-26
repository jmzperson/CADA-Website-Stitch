# Design System Specification: The Digital Curator

This design system is a bespoke framework designed to elevate the digital experience from a standard website to a premium editorial publication. It balances the authority of high-end journalism with the warmth of a community-driven platform. By prioritizing tonal depth over rigid borders and intentional asymmetry over generic grids, we create an environment that feels curated, not just constructed.

---

## 1. Creative North Star: The Digital Curator
The "Digital Curator" philosophy treats the browser window like a high-end gallery or a limited-edition art book. We move away from the "boxed-in" nature of the web by using white space as a structural element and "Playfair Display" to inject a sense of history and human touch. 

**Core Principles:**
*   **Intentional Asymmetry:** Break the vertical rhythm. Allow images to bleed off-canvas or stagger content blocks to guide the eye naturally rather than mechanically.
*   **Tonal Layering:** We do not use lines to separate ideas; we use subtle shifts in the "Cream" and "White" palettes to suggest depth.
*   **Editorial Authority:** High-contrast typography scales and the frequent use of italics create a voice that is sophisticated, trustworthy, and inviting.

---

## 2. Color & Surface Architecture

Our palette is rooted in an "Ink on Paper" aesthetic, utilizing a sophisticated range of neutrals to create a multi-layered experience.

### The Palette
*   **Primary (Navy - #0A1628):** Our "Ink." Used for core branding, footers, and high-impact CTAs.
*   **Secondary Accent (Teal - #00B4BC):** Our "Highlight." Used for interactive elements and brand-specific flourishes.
*   **Tertiary Accent (Coral - #FF6B4A):** Our "Spark." Used for secondary actions and community-driven alerts.
*   **Surface Neutrals:**
    *   `surface` (Cream - #FAF8F4): The primary hero and page background.
    *   `surface-container-low` (Cream 2 - #F2EFE8): Used for form backgrounds and subtle section differentiation.
    *   `surface-container-lowest` (White - #FFFFFF): Reserved for cards and elevated floating elements.

### The "No-Line" Rule
Standard 1px borders are prohibited for sectioning. Boundaries must be defined through background shifts. For example:
*   A `surface-container-lowest` (White) card should sit on a `surface` (Cream) background to define its edges naturally.
*   Use the `outline-variant` (#E8E4DC) only at **10-20% opacity** for "Ghost Borders" when accessibility requires a hard container.

### The "Glass & Gradient" Rule
To add soul to the interface, use "Glow Shadows" for Teal and Coral buttons—soft, colored blurs that mimic a neon light reflecting on paper. For floating navigation, use `surface-container-lowest` with an **80% opacity** and a **20px backdrop-blur** to create a sophisticated glassmorphism effect.

---

## 3. Typography: Editorial Sophistication

We pair the classical elegance of **Playfair Display** with the modern utility of **DM Sans**.

| Level | Font | Weight/Style | Role |
| :--- | :--- | :--- | :--- |
| **Display** | Playfair Display | Bold | Hero statements; high-impact editorial headers. |
| **Headline** | Playfair Display | Bold Italic | Section headers; used to denote community stories. |
| **Title** | DM Sans | Bold (All Caps) | Category labels and navigational titles. |
| **Body** | DM Sans | Regular | Primary reading experience; optimized for legibility. |
| **Label** | DM Sans | Medium | Micro-copy, metadata, and button text. |

**Hierarchy Note:** Always lead with Playfair Display for storytelling. Use DM Sans for the "workhorse" tasks—navigation, forms, and instructions.

---

## 4. Elevation & Depth

We avoid heavy, artificial shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking" surfaces. A white card on a cream background provides all the "lift" necessary. 
*   **Ambient Shadows:** When a card is hovered, apply a shadow with a large blur (30px+) and low opacity (5% Ink #1A202C). The shadow should feel like a soft glow rather than a dark silhouette.
*   **Glassmorphism:** Use semi-transparent layers for the fixed navigation bar (`surface-container-lowest` at 85% alpha) to allow the editorial content to "ghost" through as the user scrolls, maintaining a sense of place.

---

## 5. Components

### Navigation
*   **The Logo:** Playfair Display. "C" "A" "D" in Navy; the second "A" in Teal.
*   **The Bar:** Fixed top, translucent blur, white background. No bottom border; use a subtle `surface-container-low` shadow on scroll only.

### Buttons (The Pill)
*   **Shape:** 999px radius (Full pill).
*   **Primary (Dark):** Navy background, White text.
*   **Teal/Coral:** Solid color with a "Glow Shadow" (a 12px blur of the button's own hex code at 30% opacity).
*   **Ghost:** Transparent background, 1px Navy border.
*   **Interaction:** All buttons `translateY(-2px)` on hover with a 0.3s ease-out.

### Cards
*   **Contextual Backgrounds:** If the section is White, the card is Cream (#F2EFE8). If the section is Cream, the card is White.
*   **Radius:** 20px (`md` scale).
*   **Interaction:** `translateY(-5px)` on hover with a soft ambient shadow. **Do not use dividers** inside cards; use 1.5rem (24px) spacing to separate title from body.

### Inputs & Forms
*   **Background:** Always use `surface-container-low` (Cream 2) for input fields to differentiate from the page surface.
*   **Focus:** Transition the border to Teal (#00B4BC) with a 2px soft outer glow.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use staggering: Place an image slightly higher than its accompanying text block to create an editorial feel.
*   **Do** use Bold Italic headers for quotes or community features to break the "corporate" tone.
*   **Do** embrace white space. If a layout feels "full," add 2rem of padding.

### Don’t
*   **Don’t** use 100% opaque black for text. Use "Ink" (#1A202C) to maintain a soft, premium feel.
*   **Don’t** use divider lines. If you feel the need for a line, try a 40px gap or a subtle background color shift instead.
*   **Don’t** use standard "Drop Shadows." If it looks like a default Photoshop shadow, it is too heavy.

---

## 7. Motion & Reveal

Movement should feel like the turning of a heavy, high-quality page.
*   **Global Reveal:** Elements use a "Fade Up" animation (34px travel) on scroll.
*   **Timing:** 0.65s duration using a `cubic-bezier(0.16, 1, 0.3, 1)` easing for a snappy yet smooth transition.
*   **Staggering:** In lists or grids, apply a 0.05s incremental delay to each item to create a "waterfall" effect.