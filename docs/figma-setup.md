# Figma Setup Guide

## Getting Started

This guide will help you set up the Figma Dashboard Template with all components, grids, and tokens.

## Step 1: Create Breakpoint Frames

Create 4 artboards in Figma with the following dimensions:

### Frame 1: Small Laptop (1280px)
- Width: 1280px
- Height: Auto (minimum 1024px)
- Name: "Desktop / 1280"

### Frame 2: Standard Desktop (1440px)
- Width: 1440px
- Height: Auto (minimum 1024px)
- Name: "Desktop / 1440"

### Frame 3: Large Desktop (1536px)
- Width: 1536px
- Height: Auto (minimum 1024px)
- Name: "Desktop / 1536"

### Frame 4: Full HD (1920px)
- Width: 1920px
- Height: Auto (minimum 1024px)
- Name: "Desktop / 1920"

**Quick Tip:** Use Frame tool (F) and manually set dimensions in the properties panel.

---

## Step 2: Add Content Container

For each frame:

1. Create a rectangle inside the frame
2. Set width: 1200px
3. Set height: Hug contents
4. Center horizontally in the frame
5. Name: "Content Container"

**Quick Tip:** Select rectangle → Right-click → Add Auto Layout → Direction: Vertical → Alignment: Center

---

## Step 3: Apply Layout Grid

Select the Content Container in each frame and apply grid:

### For 1280px Frame
1. Click "+" next to Layout grid
2. Choose "Grid"
3. Settings:
   - Type: Stretch
   - Count: 12
   - Gutter: 24
   - Margins: 40

### For 1440px Frame
- Type: Stretch
- Count: 12
- Gutter: 24
- Margins: 80

### For 1536px Frame
- Type: Stretch
- Count: 12
- Gutter: 24
- Margins: 96

### For 1920px Frame
- Type: Stretch
- Count: 12
- Gutter: 24
- Margins: 160

---

## Step 4: Create Color Styles

Go to your assets panel and create these color styles:

### Primary Colors
- **Primary/Main:** #013576
- **Primary/Hover:** #1C73E8
- **Primary/Light:** #1C73E8

### Background Colors
- **Background/Default:** #E4E7EA
- **Background/Surface:** #FFFFFF

### Border Colors
- **Border/Default:** #D0D5DA

### Text Colors
- **Text/Primary:** #1A1A1A
- **Text/Secondary:** #6C6C6C

### State Colors
- **Success:** #32C665
- **Error:** #E53935
- **Warning:** #FFB300
- **Info:** #1E88E5

**How to create:**
1. Select → Fill → Color Styles icon → + Create style
2. Name using the format above
3. Group with "/" for organization

---

## Step 5: Create Text Styles

Create the following text styles:

### Headings
- **H1:** Nunito Sans, 32px, Line height 40px, Bold
- **H2:** Nunito Sans, 24px, Line height 32px, Bold
- **H3:** Nunito Sans, 20px, Line height 28px, Bold

### Body Text
- **Body Large:** Nunito Sans, 16px, Line height 24px, Regular
- **Body:** Nunito Sans, 14px, Line height 20px, Regular
- **Caption:** Nunito Sans, 12px, Line height 16px, Regular

**How to create:**
1. Create text element
2. Style it
3. Click text styles icon → + Create style
4. Name it

---

## Step 6: Create Effect Styles (Shadows)

Create these shadow effects:

### Shadow Level 1
- X: 0, Y: 1, Blur: 3
- Color: #000000, Opacity: 10%

### Shadow Level 2
- X: 0, Y: 4, Blur: 8
- Color: #000000, Opacity: 12%

### Shadow Level 3
- X: 0, Y: 8, Blur: 16
- Color: #000000, Opacity: 16%

**How to create:**
1. Select object → Effects → + Drop shadow
2. Configure values
3. Click effect styles icon → + Create style

---

## Step 7: Build Component Library

Create a separate page called "Components" or "Design System"

### Organize in Sections:

#### 1. Atoms
- Buttons (S, M, L)
- Inputs
- Checkboxes
- Radio buttons
- Badges
- Icons

#### 2. Molecules
- Input fields (with labels)
- Search bars
- Nav items
- Pagination

#### 3. Organisms
- Navigation sidebar
- Top bar
- Cards
- Tables
- Modals

---

## Step 8: Create Button Component

### Large Button Example:

1. **Create Frame:**
   - Press F for Frame tool
   - Draw button shape
   - Name: "Button/Large"

2. **Add Auto Layout:**
   - Right-click → Add Auto Layout
   - Direction: Horizontal
   - Alignment: Center
   - Padding: 16px horizontal
   - Gap: 8px (for icon spacing)

3. **Add Text:**
   - Press T for Text tool
   - Type "Button"
   - Apply Body Large text style
   - Center align

4. **Style:**
   - Height: 48px
   - Border radius: 8px
   - Fill: Primary/Main color
   - Text color: White

5. **Create Component:**
   - Select frame → Cmd+Option+K (Mac) or Ctrl+Alt+K (Win)
   - Name: "Button/Large/Primary"

6. **Add Variants:**
   - Click "+" next to component name
   - Create variants for: Default, Hover, Pressed, Disabled
   - Adjust colors for each state

7. **Create Properties:**
   - Add boolean property: "hasIcon"
   - Add variant property: "size" (Small, Medium, Large)
   - Add variant property: "variant" (Primary, Secondary)

---

## Step 9: Create Input Component

1. **Create Frame:**
   - Width: 320px (flexible)
   - Height: 40px

2. **Add Auto Layout:**
   - Padding: 12px horizontal
   - Gap: 8px

3. **Add Text (Placeholder):**
   - Text: "Enter text..."
   - Color: Text/Secondary
   - Size: 14px

4. **Style:**
   - Border: 1px, Border/Default color
   - Border radius: 8px
   - Background: Surface color

5. **Create States:**
   - Default
   - Hover (border color: Primary)
   - Focused (border: 2px, Primary color)
   - Error (border color: Error)
   - Disabled (opacity: 50%)

---

## Step 10: Create Card Component

1. **Create Frame:**
   - Width: 360px (or desired size)
   - Height: Auto

2. **Add Auto Layout:**
   - Direction: Vertical
   - Padding: 24px
   - Gap: 16px

3. **Add Content:**
   - Header (H3)
   - Body text
   - Action buttons (optional)

4. **Style:**
   - Background: Surface
   - Border radius: 12px
   - Shadow: Level 1

5. **Create Variants:**
   - Size: Small (300-360), Medium (480-600), Large (800-900)
   - With/without header
   - With/without buttons

---

## Step 11: Create Navigation Sidebar

### Expanded State (240px)

1. **Create Frame:**
   - Width: 240px
   - Height: Auto (or fill container)

2. **Add Auto Layout:**
   - Direction: Vertical
   - Padding: 24px
   - Gap: 8px

3. **Add Nav Items:**
   - Frame with auto layout
   - Icon (20px) + Text (14px)
   - Height: 40px
   - Padding: 12px
   - Gap: 12px
   - Border radius: 8px

4. **Create States:**
   - Default (transparent background)
   - Hover (light gray background)
   - Active (primary light background)

### Collapsed State (72px)

1. Duplicate expanded sidebar
2. Change width to 72px
3. Hide text labels
4. Center icons
5. Add tooltip component

---

## Step 12: Create Top Bar

1. **Create Frame:**
   - Width: Fill container (1200px)
   - Height: 64px

2. **Add Auto Layout:**
   - Direction: Horizontal
   - Padding: Match grid margins
   - Space between (push content to edges)

3. **Add Left Content:**
   - Logo or Title (H3)
   - Breadcrumbs (optional)

4. **Add Right Content:**
   - Search bar
   - Notification icon
   - Profile menu

---

## Step 13: Create Table Component

1. **Header Row:**
   - Auto layout horizontal
   - Cells with text style: Body Bold
   - Height: 48px
   - Background: Light gray
   - Border bottom: 1px

2. **Data Rows:**
   - Auto layout horizontal
   - Height: 56px
   - Border bottom: 1px
   - Hover state: Light background

3. **Create Columns:**
   - Fixed width or flexible
   - Text alignment: Left (default)
   - Padding: 16px

---

## Step 14: Create Modal Component

1. **Overlay:**
   - Full screen rectangle
   - Fill: Black 40% opacity
   - Name: "Modal Overlay"

2. **Modal Container:**
   - Width: 400px, 600px, or 800px
   - Auto layout vertical
   - Border radius: 12px
   - Shadow: Level 3
   - Background: Surface

3. **Modal Parts:**
   - Header (padding: 24px, border bottom)
   - Content (padding: 24px, scrollable)
   - Footer (padding: 24px, border top, buttons aligned right)

---

## Step 15: Organize and Document

### Create Component Page Structure:
```
📄 Cover Page
📄 Components
   📁 Atoms
   📁 Molecules
   📁 Organisms
📄 Breakpoints
   🖼️ 1280
   🖼️ 1440
   🖼️ 1536
   🖼️ 1920
📄 Tokens
   🎨 Colors
   📝 Typography
   📏 Spacing
```

### Add Descriptions:
- Use text frames to document component usage
- Add specs (dimensions, spacing) next to components
- Create "Do" and "Don't" examples

---

## Step 16: Export Assets

### For Development Handoff:

1. **Export Components:**
   - Select component → Export → SVG or PNG
   - Use 1x, 2x, 3x for icons

2. **Export Tokens:**
   - Use plugins like "Design Tokens" or "Style Dictionary"
   - Export as JSON or CSS variables

3. **Export Specs:**
   - Use plugins like "Zeplin" or "Figma Inspect"
   - Or use Figma Dev Mode

---

## Pro Tips

### Keyboard Shortcuts:
- **F:** Frame tool
- **T:** Text tool
- **R:** Rectangle tool
- **Shift + A:** Add auto layout
- **Cmd/Ctrl + Option/Alt + K:** Create component
- **Cmd/Ctrl + D:** Duplicate
- **Option/Alt + Drag:** Duplicate while dragging

### Plugins to Install:
- **Iconify:** Free icon library
- **Autoflow:** Create flow arrows
- **Content Reel:** Generate placeholder content
- **Stark:** Accessibility checker
- **Design Tokens:** Export design tokens

### Best Practices:
- Name layers clearly and consistently
- Use auto layout for everything
- Create components from atoms up
- Document as you go
- Use naming conventions (Button/Size/Variant)
- Keep your component library organized
- Version control with Figma branches

---

## Testing Your Design System

Before finalizing:
1. ✅ Check all breakpoints render correctly
2. ✅ Test all component states
3. ✅ Verify color contrast (WCAG AA)
4. ✅ Check spacing consistency
5. ✅ Test responsive behavior
6. ✅ Validate typography hierarchy
7. ✅ Review with stakeholders
8. ✅ Create example screens using the system

---

## Next Steps

After Figma setup:
1. Share with team for feedback
2. Export design tokens
3. Hand off to developers
4. Create component library in code
5. Maintain design-dev parity
6. Iterate based on usage

---

## Resources

- [Figma Best Practices](https://www.figma.com/best-practices/)
- [Atomic Design Methodology](https://atomicdesign.bradfrost.com/)
- [Design System Checklist](https://www.designsystemchecklist.com/)
- [Figma Community - Design Systems](https://www.figma.com/community/tag/design%20systems)
