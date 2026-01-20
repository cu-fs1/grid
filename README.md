# CSS Grid + Bento Grids - Code Explanation

## index.html

**Lines 1-7:** Standard HTML5 setup with UTF-8 charset, responsive viewport, title, and CSS link.

**Lines 10-11:** Body opens with main h1 heading.

**Lines 13-23 (Example 1):** Basic 3-column grid with 6 boxes using `grid-template-columns: repeat(3, 1fr)`.

**Lines 25-35 (Example 2):** Responsive grid using `repeat(auto-fit, minmax(180px, 1fr))` for flexible columns.

**Lines 37-50 (Example 3):** Demonstrates spanning with `.hero` (2 cols × 3 rows) and `.tall` (2 rows).

**Lines 52-60 (Example 4):** Named grid areas (Bento layout) using `grid-template-areas` with hero, notes, cta, and mini sections.

**Lines 62-73 (Example 5):** 12-column grid system with span utilities (span-3 through span-8).

**Lines 75-83 (Example 6):** `justify-content: center` - centers entire grid horizontally.

**Lines 85-93 (Example 7):** `justify-items: center` - centers items within their cells horizontally.

**Lines 95-103 (Example 8):** `align-content: center` - centers entire grid vertically.

**Lines 105-113 (Example 9):** `align-items: center` - centers items within their cells vertically.

**Lines 115-123 (Example 10):** `place-items: center` - shorthand for centering items both directions.

**Lines 124-137 (Example 11):** `auto-fill` creates empty tracks; items don't stretch.

**Lines 139-151 (Example 12):** `auto-fit` collapses empty tracks; items stretch to fill space.

**Lines 153-175 (Comparison):** Summary section comparing auto-fill vs auto-fit with styled lists.

---

## styles.css

**Lines 3-7:** Body styles - system font, 20px margin, max-width 1000px.

**Lines 9-11:** Section spacing - 22px vertical margin.

**Lines 13-17:** `.grid` - enables grid layout with 12px gap and aqua background.

**Lines 19-26:** `.box` - grid items with dashed border, padding, light gray background, flexbox centering.

**Line 30:** `.basic` - 3 equal columns.

**Line 35:** `.responsive` - auto-fit with 180px min columns.

**Lines 40-50:** `.spans`, `.hero` (span 2×3), `.tall` (span 2 rows).

**Lines 54-74:** `.bento-areas` - 6 columns, 80px rows, named areas defined with ASCII grid. Classes `.a-hero`, `.a-notes`, `.a-cta`, `.a-mini` assign elements to areas.

**Lines 77-82:** Media query - single column layout for bento-areas under 700px.

**Lines 85-106:** `.bento-12` - 12 columns with span utilities (span-3 through span-8).

**Lines 110-120:** `.align-container` - 200px height, 3×100px columns, dashed border. `.short` - 60×40px for alignment demos.

**Lines 122-143:** Alignment classes - `justify-content-center`, `justify-items-center`, `align-content-center`, `align-items-center`, `place-items-center`.

**Lines 146-156:** `.auto-fill-demo` (pink, keeps empty tracks) and `.auto-fit-demo` (blue, collapses empty tracks).

**Lines 158-164:** `.note` - yellow highlight with amber left border.

**Lines 167-205:** `.comparison-box` (responsive grid), `.comparison-item` (rounded cards), custom green checkmarks using `::before` pseudo-element.

**Lines 206-218:** Media query - bento-12 becomes 2 columns, span utilities reset under 700px.

---

## Key Concepts

- **Grid Layout:** `display: grid` with `grid-template-columns` and `gap`
- **Responsive:** `repeat(auto-fit, minmax())` and media queries
- **Spanning:** `grid-column: span N` and `grid-row: span N`
- **Named Areas:** `grid-template-areas` with `grid-area` assignments
- **Alignment:** justify/align with content/items distinctions
- **auto-fill vs auto-fit:** Empty track handling difference
