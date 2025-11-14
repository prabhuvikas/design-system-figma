# Component Specifications

## 1. Button Components

### Large Button
- **Height:** 48px
- **Padding:** 16px horizontal / 20px with icon
- **Border Radius:** 8px
- **Text Size:** 16px
- **Font:** Nunito Sans
- **Auto Layout:** Horizontal, center

### Medium Button
- **Height:** 40px
- **Padding:** 14px horizontal / 18px with icon
- **Border Radius:** 8px
- **Text Size:** 14px
- **Font:** Nunito Sans
- **Auto Layout:** Horizontal, center

### Small Button
- **Height:** 32px
- **Padding:** 12px horizontal / 16px with icon
- **Border Radius:** 8px
- **Text Size:** 14px
- **Font:** Nunito Sans
- **Auto Layout:** Horizontal, center

### Button States
- Default
- Hover
- Pressed
- Disabled
- Loading

### Button Variants
- With icon (left)
- With icon (right)
- Without icon
- Full-width variant
- Primary, Secondary, Tertiary styles

---

## 2. Input Field Component

### Specifications
- **Height:** 40px
- **Border Radius:** 8px
- **Padding (inside):** 12px left/right
- **Border:** 1px
- **Label Text:** 12px
- **Input Text:** 14px
- **Helper Text:** 12px

### Input States
- Default
- Hover
- Focused
- Error
- Disabled

### Input Variants
- Text Input
- Textarea (variable height)
- Dropdown / Select
- Date Picker
- Search Input
- Autocomplete Input

### Properties
- Leading icon
- Trailing icon
- Helper text
- Error text
- Disabled state

---

## 3. Card Component

### Base Specifications
- **Padding:** 24px
- **Border Radius:** 12px
- **Gap:** 16px (internal spacing)
- **Shadow:** Level 1 (0 1px 3px rgba(0,0,0,0.1))

### Card Sizes
- **Small:** 300–360px width
- **Medium:** 480–600px width
- **Large:** 800–900px width

### Card Variants
- With header
- With icon
- With buttons
- With status badges

### Card States
- Default
- Hover
- Selected

---

## 4. Navigation Sidebar

### Expanded State
- **Width:** 240px (fixed)
- **Padding:** 24px
- **Section Gap:** 24px
- **Item Height:** 40px
- **Icon Size:** 20px

### Collapsed State
- **Width:** 72px (fixed)
- **Icons only**
- **Tooltip on hover**

### Sidebar Elements
- Logo/Brand area
- Navigation items
- Section headers
- Active state indicator
- Hover state
- Disabled state
- Icons + labels

---

## 5. Top Bar / Header

### Specifications
- **Height:** 64px
- **Left Padding:** Match grid margin (responsive)
- **Right Padding:** Match grid margin (responsive)

### Header Elements
- Title + breadcrumbs
- Action buttons
- Profile menu
- Notification icon
- Search bar variant

---

## 6. Table System

### Table Components
- Table header row
- Data rows
- Hover row state
- Selected row state
- Striping option
- Sorting indicators
- Column resizing option

### Table Extras
- Pagination component (numbers + next/prev)
- Empty state pattern
- Bulk action toolbar
- Search/filter bar

---

## 7. Modal / Dialog System

### Modal Sizes
- **Small:** 400px width
- **Medium:** 600px width
- **Large:** 800px width

### Modal Parts
- Header (with title)
- Subheader (optional)
- Content area (scrollable if needed)
- Footer with action buttons

### Modal States
- Default
- Scrollable content
- With form
- Loading state

---

## 8. Alerts / Toasts

### Alert Types
- Success (green)
- Error (red)
- Warning (yellow)
- Info (blue)

### Alert Elements
- Icon (type-specific)
- Title
- Message
- Dismiss button

### Alert Placement
- Top right (toast)
- Top center (banner)
- Inline (contextual)

---

## 9. Badges & Tags

### Badge Variants
- Success (green - #32C665)
- Warning (yellow - #FFB300)
- Error (red - #E53935)
- Info (blue - #1E88E5)
- Neutral (gray)

### Badge Sizes
- **Small:** 12px text
- **Medium:** 14px text

### Badge Properties
- Solid background
- Outline variant
- With dot indicator
- Pill shape (high border radius)

---

## 10. Form Controls

### Checkbox
- Size: 20x20px
- Border radius: 4px
- Check icon: 16px
- States: unchecked, checked, indeterminate, disabled

### Radio Button
- Size: 20x20px diameter
- Inner dot: 10px
- States: unselected, selected, disabled

### Toggle/Switch
- Width: 44px
- Height: 24px
- Handle: 20px diameter
- States: off, on, disabled

---

## 11. Charts Placeholder Kit

### Chart Types (Placeholder)
- Line chart placeholder
- Bar chart placeholder
- Donut chart placeholder
- Area chart placeholder
- KPI blocks (large numbers with labels)

### KPI Block
- **Number Size:** H1 (32px/40px)
- **Label Size:** Body (14px/20px)
- **Change Indicator:** Small badge with arrow
- **Padding:** 24px
- **Background:** Surface color

---

## 12. Pagination Component

### Elements
- Previous button
- Page numbers (1, 2, 3...)
- Ellipsis (...) for overflow
- Next button
- Items per page selector (optional)

### Specifications
- Button height: 32px
- Button width: 32px (square) or auto for prev/next
- Gap: 8px
- Active state: Primary color background

---

## 13. Search Bar

### Specifications
- Height: 40px
- Border radius: 8px
- Padding: 12px
- Icon size: 20px
- Placeholder text: 14px

### Features
- Leading search icon
- Clear button (trailing)
- Loading state
- Dropdown suggestions (optional)

---

## 14. Icon System

### Recommended Library
- **Lucide Icons** (free, consistent)
- Line + Filled versions available

### Icon Sizes
- **Small:** 16px
- **Medium:** 20px (primary size for navigation)
- **Large:** 24px (primary size for buttons and UI)

### Icon Usage
- Navigation: 20px
- Buttons: 16-20px (based on button size)
- Input fields: 20px
- Cards: 24px

---

## 15. Empty States

### Structure
- Icon/Illustration (64-128px)
- Heading (H3)
- Description (Body text)
- Call-to-action button

### Padding
- Container: 48px vertical
- Gap: 16px

---

## 16. Loading States

### Spinner
- Size: 24px, 32px, 48px
- Color: Primary
- Thickness: 2-3px

### Skeleton Loader
- Shape matches content
- Animated shimmer effect
- Background: rgba(0,0,0,0.05)

---

## Auto Layout Best Practices

### Settings to Use Everywhere
- **Padding:** From spacing scale (4, 8, 12, 16, 24, 32, 40, 48, 64)
- **Gap:** 8px, 12px, or 16px
- **Alignment:** Center or left
- **Sizing:**
  - Hug content for text
  - Fill for containers
  - Fixed for specific dimensions

### Direction
- Horizontal for buttons, nav items, inline elements
- Vertical for lists, forms, stacked content

---

## Component Naming Convention

Use Atomic Design methodology:

### Atoms
- Button
- Input
- Label
- Icon
- Badge

### Molecules
- Input Field (input + label + helper text)
- Search Bar (input + icon + button)
- Nav Item (icon + label)
- Card Header (title + action button)

### Organisms
- Navigation Sidebar
- Top Bar Header
- Data Table
- Modal
- Form

### Templates
- Dashboard Layout
- Settings Page Layout
- List View Layout
- Detail View Layout
