# Website Architecture & Design Blueprint: Educational Portal Template

This document serves as the technical and visual blueprint for the **Jerusalem Training 2027** website. It is designed to be used as a base for building similar high-performance, compact, and user-friendly educational or informational portals.

## 1. Core Architecture
- **Structure:** Static multi-page architecture for speed and SEO.
- **Root:** `index.html` acts as the primary district selection portal.
- **Sub-pages:** Individual HTML files for specific categories (e.g., `pages/east_jerusalem.html`) to maintain clean logic and fast loading.
- **Assets:** Centralized `/assets` for branding and `/data` for document resources (PDFs/Images).

## 2. Design System
### Visual Aesthetic
- **Compact Grid:** Uses a rows-of-four layout (`grid-template-columns: repeat(auto-fill, minmax(240px, 1fr))`) to maximize screen real estate.
- **Centered Alignment:** All elements (logos, icons, titles, buttons) are block-centered for a modern, symmetrical look.
- **Gentle Pastel Palette:** A 12-tone repeating sequence using `nth-child(12n+x)` to automatically color cards.
    - *Example:* Soft Rose (#FFEBEE), Light Sky Blue (#E3F2FD), Mint (#E8F5E9).

### Card UI Component
- **Header:** Subject-specific FontAwesome icon at the very top.
- **Title:** Bold `<h2>` centered title.
- **Interaction:** Entire card is clickable; no explicit buttons on the grid for a minimalist feel.
- **Call to Action:** Simple text like "לחץ למידע" (Click for info) integrated into the card flow.

## 3. Key Interactive Features
### Rich Summary View (Transition Logic)
- **Logic:** Clicking a card triggers a JavaScript function (`showDetail`) that hides the list and displays a detailed summary page without leaving the site.
- **Summary Content:** Includes a Program Essence box, bulleted Highlights, and Action Buttons.
- **Dual Actions:** Every summary provides two distinct options:
    1. **View PDF:** Opens the file in the browser's native full-screen viewer (`target="_blank"`).
    2. **Download:** Direct file download for offline use.

### Navigation Polish
- **Global "Back to Top":** A floating arrow button (`fixed` position, high `z-index`) on all pages for easy scrolling.
- **Logo Centering:** Logo remains the central branding element at the top of every page.
- **District Counselor Footers:** Standardized footers with contact details (Name, Tel, Email) specific to each page's context.

## 4. Localization Strategy
- **Arabic/Hebrew Split:**
    - **Homepage/District Pages:** Hebrew primary.
    - **East Jerusalem Page:** Full Arabic localization, including the HTML `lang="ar"` attribute, translated headers, and RTL-optimized summaries.

## 5. Technical Stack
- **Frameworks:** Vanilla HTML5, CSS3, and JavaScript (No external JS libraries for maximum speed).
- **Styling:** TailwindCSS (CDN) for utility classes combined with custom CSS for the design system.
- **Icons:** FontAwesome 6.5.1.
- **Fonts:** Google Fonts (Assistant).

## 6. How to Reuse
1. **Copy Structure:** Mirror the `/pages`, `/assets`, and `/data` folders.
2. **Update subjectData:** Edit the JSON object in the `<script>` tag of the district pages to change titles, summaries, and file paths.
3. **Customize Colors:** Adjust the pastel hex codes in the CSS block to match a new brand identity.
4. **Localization:** Change the `lang` and `dir` attributes on the `<html>` tag for different languages.

---
*Created by Gemini CLI for RIKA2026-bot | May 2026*