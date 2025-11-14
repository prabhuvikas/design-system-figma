# Figma Project Structure

## Overview
This document provides a complete structure for building a production-ready dashboard design system in Figma, based on our design system boilerplate.

---

## 📑 Figma File Structure

Your Figma file should contain the following pages in this order:

### 1. 📄 Cover Page
A branded cover page with:
- Design system name: "Dashboard Design System"
- Version number
- Last updated date
- Brief description
- Navigation guide
- Color preview swatches

### 2. 🎨 Design Tokens
Organized sections showing all design tokens:

#### Color Tokens
- **Primary Colors** (grid of color swatches with hex codes)
  - Primary Main: #013576
  - Primary Hover: #1C73E8
  - Primary Light: #1C73E8

- **Background Colors**
  - Default: #E4E7EA
  - Surface: #FFFFFF

- **Text Colors**
  - Primary: #1A1A1A
  - Secondary: #6C6C6C

- **State Colors**
  - Success: #32C665
  - Error: #E53935
  - Warning: #FFB300
  - Info: #1E88E5

#### Spacing Scale
Visual representation of spacing (rectangles showing each size):
- 4px (xs)
- 8px (sm)
- 12px (md)
- 16px (base)
- 24px (lg)
- 32px (xl)
- 40px (2xl)
- 48px (3xl)
- 64px (4xl)

#### Typography
All text styles with examples:
- H1 - 32px/40px - Bold
- H2 - 24px/32px - Bold
- H3 - 20px/28px - Bold
- Body Large - 16px/24px - Regular
- Body - 14px/20px - Regular
- Caption - 12px/16px - Regular

#### Shadows
Examples of each shadow level on cards

#### Border Radius
Visual examples of each radius size

---

### 3. 🔲 Grid System
One frame for each breakpoint showing the grid:

#### Frame: "1280px Breakpoint"
- Frame: 1280 x 1024px
- Content container: 1200px centered
- Grid: 12 columns, 24px gutter, 40px margins
- Label annotations showing measurements

#### Frame: "1440px Breakpoint"
- Frame: 1440 x 1024px
- Content container: 1200px centered
- Grid: 12 columns, 24px gutter, 80px margins

#### Frame: "1536px Breakpoint"
- Frame: 1536 x 1024px
- Content container: 1200px centered
- Grid: 12 columns, 24px gutter, 96px margins

#### Frame: "1920px Breakpoint"
- Frame: 1920 x 1024px
- Content container: 1200px centered
- Grid: 12 columns, 24px gutter, 160px margins

#### Grid Usage Examples
Show various column spanning patterns:
- Full width (12 columns)
- Half width (6 columns)
- Third width (4 columns)
- Quarter width (3 columns)

---

### 4. ⚛️ Components - Atoms

#### Section: Buttons
All button components with variants:

**Large Primary Button** (Component)
- Default state
- Hover state
- Pressed state
- Disabled state
- Loading state
- With icon left
- With icon right

**Medium Primary Button** (Component)
Same states as large

**Small Primary Button** (Component)
Same states as large

**Button Variants:**
- Primary (solid blue background)
- Secondary (outline style)
- Tertiary (text only)
- Destructive (red for delete actions)

#### Section: Input Fields

**Text Input** (Component with variants)
- Default
- Hover
- Focused
- Error
- Disabled
- With leading icon
- With trailing icon

#### Section: Form Controls

**Checkbox** (Component)
- Unchecked
- Checked
- Indeterminate
- Disabled unchecked
- Disabled checked

**Radio Button** (Component)
- Unselected
- Selected
- Disabled unselected
- Disabled selected

**Toggle/Switch** (Component)
- Off
- On
- Disabled off
- Disabled on

#### Section: Badges

**Badge** (Component with variants)
- Success
- Error
- Warning
- Info
- Neutral
- Small size
- Medium size

#### Section: Icons
Icon library (20px and 24px):
- Navigation icons (home, settings, users, etc.)
- Action icons (edit, delete, add, search)
- Status icons (check, error, warning, info)
- Arrow icons (up, down, left, right)
- UI icons (menu, close, chevron, etc.)

---

### 5. 🧬 Components - Molecules

#### Input Field Group (Component)
- Label
- Input field
- Helper text
- Error state with error message

#### Search Bar (Component)
- Search icon (leading)
- Input field
- Clear button (trailing)
- Dropdown suggestions variant

#### Navigation Item (Component)
- Icon (20px)
- Label text
- States: default, hover, active, disabled

#### Breadcrumbs (Component)
- Home icon or text
- Separator (chevron or slash)
- Current page items
- Auto layout

#### Pagination (Component)
- Previous button
- Page numbers (1, 2, 3, ..., 10)
- Next button
- Active page state

#### Status Badge with Label (Component)
- Status badge
- Label text
- Various status types

---

### 6. 🧩 Components - Organisms

#### Navigation Sidebar (Component)

**Expanded State (240px)**
Structure:
```
├── Logo/Brand Area (64px height)
├── Navigation Section
│   ├── Section Label
│   ├── Nav Item (Dashboard)
│   ├── Nav Item (Analytics)
│   ├── Nav Item (Users)
│   └── Nav Item (Settings)
├── Divider
├── Secondary Section
│   ├── Nav Item (Help)
│   └── Nav Item (Logout)
└── User Profile Area (64px height)
```

**Collapsed State (72px)**
- Icon only
- Active indicator
- Tooltips on hover (documentation)

#### Top Bar / Header (Component)
Structure (64px height):
```
Left Section:
├── Menu toggle icon (for sidebar)
├── Page title (H2)
└── Breadcrumbs

Right Section:
├── Search bar
├── Notification icon (with badge)
├── Settings icon
└── Profile avatar + dropdown
```

#### Card Component (Component with variants)

**Small Card (320px)**
- Header with title and action icon
- Content area
- Footer with button

**Medium Card (540px)**
- Header with title and action icon
- Content area with chart/data placeholder
- Footer with stats or actions

**Large Card (800px)**
- Full featured card
- Header with title, subtitle, actions
- Content area
- Footer with multiple actions

**Card Variants:**
- Default (with shadow)
- Outlined (border instead of shadow)
- Elevated (larger shadow on hover)

#### Data Table (Component)

**Table Structure:**
```
Header Row:
├── Checkbox (select all)
├── Column 1 (sortable) - Name
├── Column 2 (sortable) - Status
├── Column 3 (sortable) - Date
└── Actions

Data Row (repeat):
├── Checkbox
├── Cell - Name with avatar
├── Cell - Status badge
├── Cell - Date
└── Actions (dropdown menu)

States:
├── Default row
├── Hover row
├── Selected row
└── Empty state
```

**Table Features:**
- Sorting indicators
- Pagination component
- Row selection
- Bulk actions toolbar
- Search/filter bar
- Column headers

#### Modal / Dialog (Component)

**Small Modal (400px)**
```
├── Overlay (dark background)
└── Modal Container
    ├── Header (title + close button)
    ├── Content area
    └── Footer (Cancel + Primary button)
```

**Medium Modal (600px)**
Same structure, more content space

**Large Modal (800px)**
Same structure, full form capability

**Modal Variants:**
- Confirmation dialog
- Form modal
- Alert modal

#### Alert / Toast (Component)
```
├── Icon (status based)
├── Content
│   ├── Title
│   └── Message
└── Dismiss button
```

Variants by type:
- Success (green)
- Error (red)
- Warning (yellow)
- Info (blue)

Position variants:
- Top right (toast)
- Top center (banner)
- Inline

---

### 7. 📐 Components - Templates

#### Dashboard Layout Template
```
┌─────────────────────────────────────────┐
│ Top Bar (64px)                          │
├───┬─────────────────────────────────────┤
│   │ Page Title + Breadcrumbs            │
│ S │                                     │
│ i │ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐│
│ d │ │ KPI  │ │ KPI  │ │ KPI  │ │ KPI  ││
│ e │ │ Card │ │ Card │ │ Card │ │ Card ││
│ b │ └──────┘ └──────┘ └──────┘ └──────┘│
│ a │                                     │
│ r │ ┌─────────────────┐ ┌──────────────┐│
│   │ │                 │ │              ││
│   │ │   Chart Card    │ │  Stats Card  ││
│   │ │                 │ │              ││
│   │ └─────────────────┘ └──────────────┘│
│   │                                     │
│   │ ┌─────────────────────────────────┐│
│   │ │                                 ││
│   │ │      Data Table                 ││
│   │ │                                 ││
│   │ └─────────────────────────────────┘│
│   │                                     │
└───┴─────────────────────────────────────┘
```

#### Table/List View Template
```
┌─────────────────────────────────────────┐
│ Top Bar                                 │
├───┬─────────────────────────────────────┤
│   │ Page Title                          │
│ S │                                     │
│ i │ ┌───────────────────────────────────┐│
│ d │ │ Search + Filters + Actions       ││
│ e │ └───────────────────────────────────┘│
│ b │                                     │
│ a │ ┌───────────────────────────────────┐│
│ r │ │                                   ││
│   │ │                                   ││
│   │ │       Data Table                 ││
│   │ │                                   ││
│   │ │                                   ││
│   │ └───────────────────────────────────┘│
│   │                                     │
│   │           [Pagination]              │
└───┴─────────────────────────────────────┘
```

#### Detail View Template
```
┌─────────────────────────────────────────┐
│ Top Bar                                 │
├───┬─────────────────────────────────────┤
│   │ ← Back + Title                      │
│ S │                                     │
│ i │ ┌───────────────┐ ┌────────────────┐│
│ d │ │               │ │                ││
│ e │ │               │ │  Info Card     ││
│ b │ │  Main Content │ │                ││
│ a │ │     Card      │ ├────────────────┤│
│ r │ │               │ │                ││
│   │ │               │ │  Actions Card  ││
│   │ │               │ │                ││
│   │ └───────────────┘ └────────────────┘│
│   │                                     │
│   │ ┌───────────────────────────────────┐│
│   │ │  Related Items / Activity         ││
│   │ └───────────────────────────────────┘│
└───┴─────────────────────────────────────┘
```

#### Settings Page Template
```
┌─────────────────────────────────────────┐
│ Top Bar                                 │
├───┬─────────────────────────────────────┤
│   │ Settings                            │
│ S │                                     │
│ i │ ┌──────────┐ ┌────────────────────┐│
│ d │ │          │ │                    ││
│ e │ │ Settings │ │  General Settings  ││
│ b │ │   Tabs   │ │                    ││
│ a │ │          │ │  [Form Fields]     ││
│ r │ │ General  │ │                    ││
│   │ │ Account  │ │  [Form Fields]     ││
│   │ │ Security │ │                    ││
│   │ │ Billing  │ │  [Save Button]     ││
│   │ │          │ │                    ││
│   │ └──────────┘ └────────────────────┘│
└───┴─────────────────────────────────────┘
```

---

### 8. 📱 Sample Pages (Real Examples)

#### Page: "Dashboard - Overview" (1440px)
Fully designed dashboard using components:
- Complete top bar with real content
- Sidebar with navigation items
- 4 KPI cards with real numbers
- Chart card with chart placeholder
- Data table with sample data
- All components properly aligned to grid

#### Page: "Analytics Dashboard" (1440px)
Analytics-focused design:
- Date range picker in top bar
- Multiple chart cards
- Statistics cards
- Performance metrics

#### Page: "Users Table" (1440px)
Table/list view:
- Search and filters
- Full data table with user data
- Bulk actions
- Pagination

#### Page: "User Detail" (1440px)
Detail view:
- User profile information
- Activity timeline
- Related data cards
- Action buttons

#### Page: "Settings" (1440px)
Settings page:
- Tab navigation
- Form fields
- Save/cancel actions

#### Page: "Login" (1440px)
Authentication page:
- Centered login card
- Input fields
- Social login buttons
- Forgot password link

---

### 9. 🎭 Light & Dark Mode

Create a duplicate page structure showing dark mode variants:

**Dark Mode Tokens:**
- Background Default: #1A1A1A
- Background Surface: #2D2D2D
- Text Primary: #FFFFFF
- Text Secondary: #B0B0B0
- Border: #404040

All components should have dark mode variants.

---

### 10. 📋 Component States Reference

A reference page showing all possible states for each component:
- Default
- Hover
- Active/Pressed
- Focused
- Disabled
- Loading
- Error
- Success

---

### 11. 📐 Layout Examples

Page showing different layout patterns:
- Single column
- Two column (60/40 split)
- Three column (equal)
- Sidebar + content
- Centered content
- Full width content

---

### 12. ♿ Accessibility Guidelines

Page documenting accessibility features:
- Color contrast ratios
- Focus states
- Keyboard navigation patterns
- ARIA label examples
- Screen reader considerations

---

## 🎨 Figma Styles to Create

### Color Styles
Create these color styles in Figma (Assets panel):

**Primary/**
- Primary/Main
- Primary/Hover
- Primary/Light

**Background/**
- Background/Default
- Background/Surface

**Text/**
- Text/Primary
- Text/Secondary

**State/**
- State/Success
- State/Error
- State/Warning
- State/Info

**Border/**
- Border/Default

### Text Styles
Create these text styles:

**Heading/**
- Heading/H1
- Heading/H2
- Heading/H3

**Body/**
- Body/Large
- Body/Regular
- Body/Caption

### Effect Styles (Shadows)
- Shadow/Level 1
- Shadow/Level 2
- Shadow/Level 3

---

## 🔧 Component Properties

### Button Component Properties
- **Variant:** Primary, Secondary, Tertiary, Destructive
- **Size:** Small, Medium, Large
- **State:** Default, Hover, Pressed, Disabled, Loading
- **Icon Position:** None, Left, Right
- **Full Width:** Boolean

### Input Component Properties
- **State:** Default, Hover, Focused, Error, Disabled
- **Type:** Text, Email, Password, Number
- **Leading Icon:** Boolean
- **Trailing Icon:** Boolean
- **Size:** Medium, Large

### Card Component Properties
- **Size:** Small, Medium, Large
- **Variant:** Default, Outlined, Elevated
- **Has Header:** Boolean
- **Has Footer:** Boolean

---

## 📏 Auto Layout Best Practices

Every component should use auto layout:

**Buttons:**
- Direction: Horizontal
- Padding: Based on size (16/20, 14/18, 12/16)
- Gap: 8px (between icon and text)
- Alignment: Center
- Resizing: Hug horizontal, Fixed vertical

**Cards:**
- Direction: Vertical
- Padding: 24px all sides
- Gap: 16px between elements
- Resizing: Fill horizontal, Hug vertical

**Forms:**
- Direction: Vertical
- Gap: 16px between fields
- Label gap from input: 4px

---

## 📦 Export Settings

Set up export settings for development:

**Icons:**
- SVG format
- 1x size
- Optimize for web

**Images:**
- PNG format
- 1x, 2x, 3x sizes

**Components:**
- Use Figma Dev Mode for CSS export

---

## 🎯 Component Naming Convention

Use consistent naming:

```
ComponentType/Variant/Size/State

Examples:
- Button/Primary/Large/Default
- Button/Primary/Large/Hover
- Button/Secondary/Medium/Disabled
- Input/Text/Default
- Card/Small/Default
```

---

## ✅ Build Checklist

- [ ] Create cover page
- [ ] Document all design tokens
- [ ] Create color styles
- [ ] Create text styles
- [ ] Create effect styles
- [ ] Build grid system frames
- [ ] Create all atom components
- [ ] Create all molecule components
- [ ] Create all organism components
- [ ] Create template layouts
- [ ] Design sample pages
- [ ] Add dark mode variants
- [ ] Document accessibility
- [ ] Test all component variants
- [ ] Add descriptions to components
- [ ] Organize into proper sections
- [ ] Add auto layout to all components
- [ ] Set up component properties
- [ ] Test responsive behavior

---

This structure will give you a professional, production-ready design system in Figma that matches our design boilerplate!
