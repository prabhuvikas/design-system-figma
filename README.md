# Figma Dashboard Design System

A comprehensive design system boilerplate for desktop web dashboards, supporting breakpoints at 1280px, 1440px, 1536px, and 1920px.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Design Tokens](#design-tokens)
- [Grid System](#grid-system)
- [Components](#components)
- [File Structure](#file-structure)
- [Implementation](#implementation)
- [Figma Setup](#figma-setup)
- [Development](#development)
- [Contributing](#contributing)

## 🎨 Overview

This design system provides a complete foundation for building dashboard interfaces with:

- **4 responsive breakpoints** (1280, 1440, 1536, 1920 px)
- **12-column grid system** with adaptive margins
- **Comprehensive component library** (buttons, inputs, cards, navigation, etc.)
- **Design tokens** for colors, spacing, typography, and shadows
- **Atomic Design methodology** for component organization
- **Accessibility-first** approach with WCAG AA compliance

### Design Philosophy

- **Consistency:** Unified spacing scale, color palette, and typography
- **Scalability:** Modular components built from atoms to organisms
- **Accessibility:** Keyboard navigation, ARIA labels, and color contrast
- **Flexibility:** Adaptable to various dashboard and admin panel use cases

## ✨ Features

### Design Tokens
- 9-step spacing scale (4px to 64px)
- Semantic color system with state colors
- Typography scale (6 levels)
- 3-level shadow system
- Consistent border radius values

### Component Library
- **Atoms:** Buttons, Inputs, Labels, Icons, Badges
- **Molecules:** Input Fields, Search Bars, Navigation Items, Pagination
- **Organisms:** Sidebar Navigation, Top Bar, Cards, Tables, Modals
- **Templates:** Dashboard layouts, List views, Detail views

### Grid System
- 12-column flexible grid
- Max content width: 1200px
- 24px gutter (consistent across breakpoints)
- Responsive margins:
  - 1280px: 40px
  - 1440px: 80px
  - 1536px: 96px
  - 1920px: 160px

## 🚀 Getting Started

### Prerequisites

- **For Figma:** Figma desktop app or web access
- **For Development:** Node.js 14+ (if implementing in code)
- **Font:** Nunito Sans (available on Google Fonts)

### Quick Start

1. **Clone or download this repository:**
   ```bash
   git clone <repository-url>
   cd design-system-figma
   ```

2. **For Figma implementation:**
   - Open Figma
   - Follow the [Figma Setup Guide](docs/figma-setup.md)
   - Import `design-tokens.json` using a tokens plugin

3. **For code implementation:**
   ```bash
   # Install dependencies (example for npm)
   npm install

   # Import design tokens
   import tokens from './design-tokens.json';

   # Import CSS variables
   import './styles/variables.css';
   import './styles/typography.css';
   import './styles/utilities.css';
   ```

## 🎯 Design Tokens

All design tokens are defined in `design-tokens.json` and can be imported into Figma or code.

### Color Palette

#### Primary
- **Main:** `#013576` - Primary brand color
- **Hover:** `#1C73E8` - Interactive hover state
- **Light:** `#1C73E8` - Accent/highlight color

#### Text
- **Primary:** `#1A1A1A` - Main text
- **Secondary:** `#6C6C6C` - Supporting text

#### Background
- **Default:** `#E4E7EA` - Page background
- **Surface:** `#FFFFFF` - Card/component background

#### States
- **Success:** `#32C665` - Positive actions
- **Error:** `#E53935` - Errors and warnings
- **Warning:** `#FFB300` - Caution states
- **Info:** `#1E88E5` - Informational messages

### Spacing Scale

```
4px   (xs)   - Tiny gaps, icon spacing
8px   (sm)   - Small gaps, compact layouts
12px  (md)   - Medium gaps
16px  (base) - Default spacing
24px  (lg)   - Large gaps, section spacing
32px  (xl)   - Extra large spacing
40px  (2xl)  - Component padding
48px  (3xl)  - Large component spacing
64px  (4xl)  - Section dividers
```

### Typography

**Font Family:** Nunito Sans

| Style       | Size | Line Height | Weight | Use Case                    |
|-------------|------|-------------|--------|-----------------------------|
| H1          | 32px | 40px        | 700    | Page titles                 |
| H2          | 24px | 32px        | 700    | Section headings            |
| H3          | 20px | 28px        | 700    | Subsection headings         |
| Body Large  | 16px | 24px        | 400    | Emphasis text, large buttons|
| Body        | 14px | 20px        | 400    | Default body text           |
| Caption     | 12px | 16px        | 400    | Helper text, small labels   |

## 📐 Grid System

### Specifications

- **Max Content Width:** 1200px (centered)
- **Columns:** 12
- **Gutter:** 24px (fixed across all breakpoints)
- **Grid Type:** Stretch

### Breakpoint-Specific Margins

| Breakpoint | Width  | Margins | Use Case            |
|------------|--------|---------|---------------------|
| Small      | 1280px | 40px    | Small laptops       |
| Medium     | 1440px | 80px    | Standard desktops   |
| Large      | 1536px | 96px    | Large desktops      |
| X-Large    | 1920px | 160px   | Full HD monitors    |

### Usage Example (CSS)

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--grid-margin);
}

.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}

.col-6 {
  grid-column: span 6;
}
```

See [grid-system.md](grid-system.md) for detailed documentation.

## 🧩 Components

### Button Component

Three sizes with consistent variants:

#### Large Button
- Height: 48px
- Padding: 16px/20px
- Text: 16px
- Radius: 8px

#### Medium Button
- Height: 40px
- Padding: 14px/18px
- Text: 14px
- Radius: 8px

#### Small Button
- Height: 32px
- Padding: 12px/16px
- Text: 14px
- Radius: 8px

**States:** Default, Hover, Pressed, Disabled, Loading

**Variants:** Primary, Secondary, Tertiary, With icon (left/right), Full-width

### Input Field Component

- Height: 40px
- Border: 1px solid
- Radius: 8px
- Padding: 12px horizontal
- Label: 12px
- Input text: 14px
- Helper text: 12px

**States:** Default, Hover, Focused, Error, Disabled

**Features:** Leading icon, Trailing icon, Helper text, Error text

### Card Component

- Padding: 24px
- Radius: 12px
- Gap: 16px (internal spacing)
- Shadow: Level 1 (0 1px 3px rgba(0,0,0,0.1))

**Sizes:**
- Small: 300-360px
- Medium: 480-600px
- Large: 800-900px

### Navigation Sidebar

**Expanded:**
- Width: 240px
- Padding: 24px
- Item height: 40px
- Icon size: 20px

**Collapsed:**
- Width: 72px
- Icons only
- Tooltips on hover

### Top Bar / Header

- Height: 64px
- Padding: Matches grid margins
- Elements: Title, breadcrumbs, actions, profile, notifications

### Additional Components

- **Tables:** Header rows, data rows, hover states, sorting, pagination
- **Modals:** Small (400px), Medium (600px), Large (800px)
- **Alerts/Toasts:** Success, Error, Warning, Info with icons
- **Badges:** Status indicators in 5 variants
- **Forms:** Checkbox, Radio, Toggle, Dropdown, Date Picker, Search

See [component-specifications.md](component-specifications.md) for complete details.

## 📁 File Structure

```
design-system-figma/
├── README.md
├── design-tokens.json
├── grid-system.md
├── component-specifications.md
├── directory-structure.md
│
├── components/
│   ├── atoms/          # Basic components
│   ├── molecules/      # Composite components
│   ├── organisms/      # Complex components
│   └── templates/      # Page layouts
│
├── styles/
│   ├── variables.css   # CSS custom properties
│   ├── typography.css  # Typography styles
│   └── utilities.css   # Utility classes
│
├── assets/
│   └── icons/          # Icon library
│
└── docs/
    └── figma-setup.md  # Figma implementation guide
```

See [directory-structure.md](directory-structure.md) for detailed organization.

## 💻 Implementation

### CSS Variables Implementation

1. **Import base styles:**
   ```html
   <link rel="stylesheet" href="styles/variables.css">
   <link rel="stylesheet" href="styles/typography.css">
   <link rel="stylesheet" href="styles/utilities.css">
   ```

2. **Use design tokens:**
   ```css
   .button {
     padding: var(--button-padding-md);
     background: var(--color-primary);
     border-radius: var(--radius-md);
     color: white;
   }
   ```

### React Component Example

```jsx
import React from 'react';
import tokens from './design-tokens.json';

export const Button = ({
  size = 'medium',
  variant = 'primary',
  children
}) => {
  return (
    <button
      className={`button button--${size} button--${variant}`}
      style={{
        height: tokens.button.height[size],
        padding: tokens.button.padding[size],
        borderRadius: tokens.borderRadius.md,
      }}
    >
      {children}
    </button>
  );
};
```

### Vue Component Example

```vue
<template>
  <button
    :class="['button', `button--${size}`, `button--${variant}`]"
    :style="buttonStyles"
  >
    <slot />
  </button>
</template>

<script>
import tokens from './design-tokens.json';

export default {
  props: {
    size: {
      type: String,
      default: 'medium'
    },
    variant: {
      type: String,
      default: 'primary'
    }
  },
  computed: {
    buttonStyles() {
      return {
        height: tokens.button.height[this.size],
        padding: tokens.button.padding[this.size],
        borderRadius: tokens.borderRadius.md,
      };
    }
  }
};
</script>
```

## 🎨 Figma Setup

Complete step-by-step instructions for implementing this design system in Figma:

1. Create breakpoint frames (1280, 1440, 1536, 1920 px)
2. Add content containers (1200px max-width, centered)
3. Apply 12-column layout grids
4. Create color styles
5. Create text styles
6. Create effect styles (shadows)
7. Build component library
8. Organize using Atomic Design

**Full guide:** [docs/figma-setup.md](docs/figma-setup.md)

### Recommended Figma Plugins

- **Iconify** - Access to free icon libraries
- **Design Tokens** - Export design tokens
- **Stark** - Accessibility checker
- **Autoflow** - Create flow diagrams
- **Content Reel** - Generate placeholder content

## 🛠 Development

### Setting Up for Development

```bash
# Clone repository
git clone <repository-url>

# Navigate to directory
cd design-system-figma

# Install dependencies (if using a framework)
npm install

# Start development server
npm run dev
```

### Building Components

Follow the Atomic Design methodology:

1. **Start with Atoms** (Button, Input, Label, Icon)
2. **Build Molecules** (Input Field = Input + Label + Helper Text)
3. **Create Organisms** (Form = Multiple Input Fields + Buttons)
4. **Design Templates** (Dashboard = Sidebar + Top Bar + Content)

### Testing Checklist

- [ ] All breakpoints render correctly
- [ ] All component states work (hover, focus, disabled)
- [ ] Color contrast meets WCAG AA standards
- [ ] Keyboard navigation works
- [ ] Screen reader compatibility
- [ ] Responsive behavior verified
- [ ] Cross-browser testing completed

## 📚 Documentation

- **[Grid System](grid-system.md)** - Complete grid documentation
- **[Component Specifications](component-specifications.md)** - Detailed component specs
- **[Directory Structure](directory-structure.md)** - File organization guide
- **[Figma Setup Guide](docs/figma-setup.md)** - Step-by-step Figma implementation

## 🎯 Use Cases

This design system is perfect for:

- Admin panels and dashboards
- SaaS applications
- Data visualization tools
- Analytics platforms
- Internal business tools
- Customer portals
- Project management interfaces

## 🌓 Dark Mode Support

CSS variables include dark mode support:

```css
@media (prefers-color-scheme: dark) {
  :root {
    --color-bg-default: #1A1A1A;
    --color-bg-surface: #2D2D2D;
    --color-text-primary: #FFFFFF;
    --color-text-secondary: #B0B0B0;
  }
}
```

Or use data attribute for manual toggle:

```html
<html data-theme="dark">
```

## ♿️ Accessibility

This design system follows WCAG 2.1 Level AA guidelines:

- ✅ Color contrast ratios meet minimum standards
- ✅ All interactive elements are keyboard accessible
- ✅ ARIA labels provided for screen readers
- ✅ Focus indicators visible
- ✅ Reduced motion support
- ✅ Semantic HTML structure

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit with clear messages (`git commit -m 'Add some AmazingFeature'`)
5. Push to branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

### Commit Message Format

```
feat(Button): add loading state
fix(Input): correct focus outline
docs(README): update installation guide
style(Card): adjust padding values
refactor(Modal): improve structure
test(Button): add unit tests
```

## 📄 License

This design system boilerplate is open source and available under the MIT License.

## 🙏 Acknowledgments

- Based on Figma Dashboard Template specifications
- Font: Nunito Sans by Google Fonts
- Methodology: Atomic Design by Brad Frost
- Inspired by modern design system best practices

## 📞 Support

For questions, issues, or suggestions:

- Create an issue in the repository
- Refer to the documentation files
- Check the Figma setup guide

## 🔄 Changelog

### Version 1.0.0 (Initial Release)
- Complete design token system
- 12-column responsive grid (4 breakpoints)
- Comprehensive component library
- CSS implementation with variables
- Figma setup documentation
- Atomic Design structure
- Accessibility guidelines
- Dark mode support

---

**Happy Designing! 🎨**

For detailed implementation instructions, please refer to the documentation files in this repository.
