# Grid System Configuration

## Overview
12-column responsive grid system with centered content container (max-width: 1200px)

## Breakpoints & Specifications

### 1280px - Small Laptop
- **Frame Width:** 1280px
- **Frame Height:** Auto / 1024+ px
- **Columns:** 12
- **Gutter:** 24px
- **Margins:** 40px (left & right)
- **Content Max Width:** 1200px (centered)
- **Grid Type:** Stretch
- **Use Case:** 3-column or 2-column sections, narrower margins

### 1440px - Standard Desktop (Default)
- **Frame Width:** 1440px
- **Frame Height:** Auto / 1024+ px
- **Columns:** 12
- **Gutter:** 24px
- **Margins:** 80px (left & right)
- **Content Max Width:** 1200px (centered)
- **Grid Type:** Stretch
- **Use Case:** 3 or 4-column grids, default layout

### 1536px - Large Desktop
- **Frame Width:** 1536px
- **Frame Height:** Auto / 1024+ px
- **Columns:** 12
- **Gutter:** 24px
- **Margins:** 96px (left & right)
- **Content Max Width:** 1200px (centered)
- **Grid Type:** Stretch
- **Use Case:** Slightly wider spacing, more breathing room

### 1920px - Full HD Monitor
- **Frame Width:** 1920px
- **Frame Height:** Auto / 1024+ px
- **Columns:** 12
- **Gutter:** 24px
- **Margins:** 160px (left & right)
- **Content Max Width:** 1200px (centered)
- **Grid Type:** Stretch
- **Use Case:** Increase margins, allow card grids to expand
- **Note:** Do NOT increase button or text sizes

## Implementation Guide

### Figma Setup
1. Create 4 frames with dimensions: 1280, 1440, 1536, 1920 px wide
2. Set frame height to Auto or minimum 1024px
3. Inside each frame, create a centered container (max-width: 1200px)
4. Apply layout grid with specifications above
5. Margins adjust automatically based on breakpoint

### CSS Grid Implementation
```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding-left: var(--grid-margin);
  padding-right: var(--grid-margin);
}

.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}

/* Breakpoint-specific margins */
@media (min-width: 1280px) {
  :root {
    --grid-margin: 40px;
  }
}

@media (min-width: 1440px) {
  :root {
    --grid-margin: 80px;
  }
}

@media (min-width: 1536px) {
  :root {
    --grid-margin: 96px;
  }
}

@media (min-width: 1920px) {
  :root {
    --grid-margin: 160px;
  }
}
```

## Column Spanning Examples

### Full Width (12 columns)
Header, Footer, Hero sections

### Half Width (6 columns)
Two-column layouts

### Third Width (4 columns)
Three-column card grids

### Quarter Width (3 columns)
Four-column layouts

### Custom Spans
Flexible combinations based on design needs
