# Figma Component Build Guide
## Step-by-Step Instructions to Build Each Component

This guide provides exact, copy-paste ready specifications for building each component in Figma.

---

## 🎨 STEP 1: Set Up Color Styles

### How to Create Color Styles:
1. Draw a rectangle in Figma (R key)
2. Fill it with the color
3. Click the fill color → Color styles icon → Create style
4. Name it using the format below

### Colors to Create:

```
Primary/Main
- Hex: #013576
- RGB: 1, 53, 118

Primary/Hover
- Hex: #1C73E8
- RGB: 28, 115, 232

Primary/Light
- Hex: #1C73E8
- RGB: 28, 115, 232

Background/Default
- Hex: #E4E7EA
- RGB: 228, 231, 234

Background/Surface
- Hex: #FFFFFF
- RGB: 255, 255, 255

Text/Primary
- Hex: #1A1A1A
- RGB: 26, 26, 26

Text/Secondary
- Hex: #6C6C6C
- RGB: 108, 108, 108

Border/Default
- Hex: #D0D5DA
- RGB: 208, 213, 218

State/Success
- Hex: #32C665
- RGB: 50, 198, 101

State/Error
- Hex: #E53935
- RGB: 229, 57, 53

State/Warning
- Hex: #FFB300
- RGB: 255, 179, 0

State/Info
- Hex: #1E88E5
- RGB: 30, 136, 229
```

---

## 📝 STEP 2: Set Up Text Styles

### How to Create Text Styles:
1. Create a text element (T key)
2. Style it with font, size, weight
3. Click the text properties → Text styles icon → Create style
4. Name it

### Text Styles to Create:

```
Heading/H1
- Font: Nunito Sans
- Weight: Bold (700)
- Size: 32px
- Line height: 40px

Heading/H2
- Font: Nunito Sans
- Weight: Bold (700)
- Size: 24px
- Line height: 32px

Heading/H3
- Font: Nunito Sans
- Weight: Bold (700)
- Size: 20px
- Line height: 28px

Body/Large
- Font: Nunito Sans
- Weight: Regular (400)
- Size: 16px
- Line height: 24px

Body/Regular
- Font: Nunito Sans
- Weight: Regular (400)
- Size: 14px
- Line height: 20px

Body/Caption
- Font: Nunito Sans
- Weight: Regular (400)
- Size: 12px
- Line height: 16px
```

---

## 💎 STEP 3: Set Up Effect Styles (Shadows)

### How to Create Effect Styles:
1. Select a shape
2. Add drop shadow effect
3. Configure values
4. Click effect icon → Create style

### Shadows to Create:

```
Shadow/Level 1
- Type: Drop shadow
- X: 0
- Y: 1
- Blur: 3
- Color: #000000
- Opacity: 10%

Shadow/Level 2
- Type: Drop shadow
- X: 0
- Y: 4
- Blur: 8
- Color: #000000
- Opacity: 12%

Shadow/Level 3
- Type: Drop shadow
- X: 0
- Y: 8
- Blur: 16
- Color: #000000
- Opacity: 16%
```

---

## 🔘 BUILD: Large Button Component

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "Button/Large/Primary"
   - Width: Auto (will be set by auto layout)
   - Height: 48px

2. **Add Auto Layout** (Shift + A)
   - Direction: Horizontal
   - Horizontal padding: 20px
   - Vertical padding: 14px (to achieve 48px height with text)
   - Gap between items: 8px
   - Alignment: Center both axes

3. **Add Text Layer** (press T)
   - Text: "Button"
   - Style: Body/Large (16px)
   - Color: #FFFFFF (white)
   - Alignment: Center

4. **Style the Frame:**
   - Fill: Primary/Main color style
   - Border radius: 8px
   - No stroke

5. **Create Component** (Cmd/Ctrl + Option/Alt + K)
   - Description: "Large primary button"

6. **Add Variants:**
   - Click "+" next to component name
   - Add property "State" with values: Default, Hover, Pressed, Disabled, Loading
   - Add property "Icon" with boolean: True/False
   - Add property "Style" with values: Primary, Secondary, Tertiary

7. **Style Each Variant:**

   **Hover State:**
   - Background: Primary/Hover color style

   **Pressed State:**
   - Background: Darker shade (multiply Primary by 0.9)

   **Disabled State:**
   - Background: #E4E7EA
   - Text color: #6C6C6C
   - Opacity: 50%

   **Secondary Style:**
   - Background: Transparent
   - Stroke: 1px, Primary/Main
   - Text color: Primary/Main

   **Tertiary Style:**
   - Background: Transparent
   - No stroke
   - Text color: Primary/Main

8. **Add Icon Variant:**
   - Duplicate default variant
   - Set Icon property to True
   - Add icon frame (20x20px) before text
   - Use placeholder icon

---

## 🔘 BUILD: Medium & Small Buttons

### Medium Button:
Follow same steps as Large Button but with:
- Height: 40px
- Horizontal padding: 18px
- Vertical padding: 11px
- Text: Body/Regular (14px)
- Icon size: 20px

### Small Button:
Follow same steps as Large Button but with:
- Height: 32px
- Horizontal padding: 16px
- Vertical padding: 7px
- Text: Body/Regular (14px)
- Icon size: 16px

---

## 📝 BUILD: Input Field Component

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "Input/Text"
   - Width: 320px (or flexible)
   - Height: 40px

2. **Add Auto Layout** (Shift + A)
   - Direction: Horizontal
   - Horizontal padding: 12px
   - Vertical padding: 10px (to achieve 40px with text)
   - Gap: 8px
   - Alignment: Left vertically, Center vertically

3. **Add Text Placeholder** (press T)
   - Text: "Enter text..."
   - Style: Body/Regular (14px)
   - Color: Text/Secondary (#6C6C6C)

4. **Style the Frame:**
   - Fill: Background/Surface (white)
   - Stroke: 1px, Border/Default color
   - Border radius: 8px

5. **Create Component** (Cmd/Ctrl + Option/Alt + K)

6. **Add Variants:**
   - Property "State": Default, Hover, Focused, Error, Disabled
   - Property "Leading Icon": Boolean
   - Property "Trailing Icon": Boolean

7. **Style Variants:**

   **Hover:**
   - Stroke color: Primary/Main at 50% opacity

   **Focused:**
   - Stroke: 2px, Primary/Main
   - Add outer glow effect (optional)

   **Error:**
   - Stroke: 2px, State/Error
   - Text color can change

   **Disabled:**
   - Background: #F5F5F5
   - Text opacity: 50%

8. **Add Icon Variants:**
   - For leading icon: Add 20x20 icon frame at start
   - For trailing icon: Add 20x20 icon frame at end

---

## 📦 BUILD: Card Component - Small

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "Card/Small"
   - Width: 320px
   - Height: Auto (will grow with content)

2. **Add Auto Layout** (Shift + A)
   - Direction: Vertical
   - Padding: 24px all sides
   - Gap between items: 16px
   - Alignment: Left, Top

3. **Add Card Header Section:**
   - Create frame with auto layout (horizontal)
   - Add title text (Heading/H3)
   - Add action icon on right (24x24)
   - Space between: justify

4. **Add Content Area:**
   - Frame with auto layout (vertical)
   - Add sample text content
   - Gap: 12px

5. **Add Footer (optional):**
   - Frame with auto layout (horizontal)
   - Add button or text
   - Align right

6. **Style the Card Frame:**
   - Fill: Background/Surface (white)
   - Border radius: 12px
   - Effect: Shadow/Level 1

7. **Create Component** (Cmd/Ctrl + Option/Alt + K)

8. **Add Variants:**
   - Property "Size": Small, Medium, Large
   - Property "Variant": Default, Outlined, Elevated

9. **Style Variants:**

   **Outlined:**
   - Remove shadow
   - Add stroke: 1px, Border/Default

   **Elevated:**
   - Shadow: Shadow/Level 2
   - On hover: Shadow/Level 3

10. **Create Medium and Large Sizes:**
    - Medium: 540px width
    - Large: 800px width
    - Adjust padding and gaps proportionally

---

## 🧭 BUILD: Navigation Sidebar - Expanded

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "Sidebar/Expanded"
   - Width: 240px
   - Height: 800px (or auto)

2. **Add Auto Layout** (Shift + A)
   - Direction: Vertical
   - Padding: 24px
   - Gap: 8px
   - Alignment: Left, Top

3. **Add Logo Section:**
   - Frame: 192px x 48px
   - Add logo placeholder or text
   - Margin bottom: 16px

4. **Create Navigation Item Component:**

   **Nav Item Build:**
   - Frame: 192px x 40px
   - Auto layout: Horizontal
   - Padding: 12px horizontal, 8px vertical
   - Gap: 12px
   - Alignment: Left, Center

   **Add Icon:**
   - 20x20px frame
   - Use icon placeholder
   - Color: Text/Secondary

   **Add Label:**
   - Text: "Dashboard"
   - Style: Body/Regular
   - Color: Text/Primary

   **Style:**
   - Border radius: 8px
   - Background: Transparent (default)

   **Create Component and Variants:**
   - State: Default, Hover, Active, Disabled

   **Style Variants:**
   - Hover: Background rgba(0,0,0,0.05)
   - Active: Background Primary/Light at 10% opacity
   - Disabled: Opacity 50%

5. **Add Nav Items to Sidebar:**
   - Place multiple nav item instances
   - Label them: Dashboard, Analytics, Users, Settings

6. **Add Divider:**
   - 1px line, Border/Default color
   - Full width

7. **Add Secondary Section:**
   - More nav items: Help, Support, Logout

8. **Add User Profile Section at Bottom:**
   - Frame with avatar + name
   - Auto layout horizontal
   - Gap: 12px

9. **Create Component** (Cmd/Ctrl + Option/Alt + K)

10. **Create Collapsed Variant:**
    - Duplicate component
    - Change width to 72px
    - Hide labels (set opacity 0 or remove)
    - Center icons
    - Add property "Expanded": Boolean

---

## 📊 BUILD: Top Bar / Header

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "TopBar"
   - Width: 1200px (content width) or flexible
   - Height: 64px

2. **Add Auto Layout** (Shift + A)
   - Direction: Horizontal
   - Padding: 0px (handled by grid margins)
   - Horizontal padding: 24px
   - Gap: 24px
   - Alignment: Space between, Center vertically

3. **Create Left Section:**
   - Frame with auto layout horizontal
   - Gap: 16px
   - Add:
     - Menu icon (24x24) - for mobile toggle
     - Page title (Heading/H2)
     - Breadcrumbs (optional)

4. **Create Right Section:**
   - Frame with auto layout horizontal
   - Gap: 16px
   - Add:
     - Search bar component instance
     - Notification icon with badge (24x24)
     - Settings icon (24x24)
     - Profile avatar (32x32 circle)

5. **Style the TopBar Frame:**
   - Fill: Background/Surface (white)
   - Bottom border: 1px, Border/Default
   - OR use Shadow/Level 1

6. **Create Component** (Cmd/Ctrl + Option/Alt + K)

7. **Add Variants (optional):**
   - Property "With Search": Boolean
   - Property "With Breadcrumbs": Boolean

---

## 📋 BUILD: Data Table

### Step-by-Step:

1. **Create Table Header:**

   **Frame Setup:**
   - Name: "Table/Header"
   - Width: 1000px (or flexible)
   - Height: 48px
   - Auto layout: Horizontal
   - Padding: 16px
   - Gap: 16px
   - Alignment: Space between, Center

   **Add Header Cells:**
   - Checkbox (20x20)
   - Column text (Body/Regular, Bold)
   - Sort icon (16x16) next to sortable columns
   - Actions column (right aligned)

   **Style:**
   - Background: rgba(0,0,0,0.02)
   - Bottom border: 1px, Border/Default

2. **Create Table Row:**

   **Frame Setup:**
   - Name: "Table/Row"
   - Same width as header
   - Height: 56px
   - Auto layout: Horizontal
   - Padding: 16px
   - Gap: 16px
   - Alignment: Space between, Center

   **Add Cells:**
   - Checkbox
   - Avatar + name (frame with auto layout)
   - Status badge component
   - Date text
   - Actions menu icon (24x24)

   **Style:**
   - Background: white (default)
   - Bottom border: 1px, Border/Default

   **Create Component and Variants:**
   - State: Default, Hover, Selected

   **Style Variants:**
   - Hover: Background rgba(0,0,0,0.02)
   - Selected: Background Primary at 5% opacity

3. **Assemble Table:**
   - Frame with auto layout vertical
   - Gap: 0
   - Add header
   - Add multiple row instances
   - Add pagination at bottom

4. **Create Empty State:**
   - Center aligned
   - Icon + text + button
   - Show when no data

---

## 🔔 BUILD: Alert / Toast Component

### Step-by-Step:

1. **Create Frame** (press F)
   - Name: "Alert/Success"
   - Width: 400px
   - Height: Auto

2. **Add Auto Layout** (Shift + A)
   - Direction: Horizontal
   - Padding: 16px
   - Gap: 12px
   - Alignment: Left, Top

3. **Add Icon:**
   - 24x24px frame
   - Success icon (checkmark circle)
   - Color: State/Success

4. **Add Content Section:**
   - Frame with auto layout vertical
   - Gap: 4px

   **Add Title:**
   - Text: "Success!"
   - Style: Body/Regular, Bold
   - Color: Text/Primary

   **Add Message:**
   - Text: "Your changes have been saved"
   - Style: Body/Regular
   - Color: Text/Secondary

5. **Add Dismiss Button:**
   - 24x24 close icon
   - Color: Text/Secondary
   - Clickable

6. **Style Frame:**
   - Fill: State/Success at 10% opacity
   - Border: 1px, State/Success
   - Border radius: 8px
   - Shadow: Shadow/Level 2

7. **Create Component** (Cmd/Ctrl + Option/Alt + K)

8. **Add Variants:**
   - Property "Type": Success, Error, Warning, Info

9. **Style Each Type:**
   - Error: Red colors (State/Error)
   - Warning: Yellow colors (State/Warning)
   - Info: Blue colors (State/Info)

---

## 🪟 BUILD: Modal Component

### Step-by-Step:

1. **Create Overlay:**
   - Frame: Full screen size (1440x1024)
   - Name: "Modal/Overlay"
   - Fill: Black (#000000) at 40% opacity

2. **Create Modal Container:**
   - Frame: 600px width (medium), auto height
   - Name: "Modal/Medium"
   - Position: Center of overlay

3. **Add Auto Layout to Modal:**
   - Direction: Vertical
   - Padding: 0 (handled by sections)
   - Gap: 0
   - Alignment: Left, Top

4. **Create Header Section:**
   - Frame with auto layout horizontal
   - Width: Fill
   - Height: 64px
   - Padding: 24px
   - Gap: 16px
   - Space between: justify

   **Add:**
   - Title (Heading/H3)
   - Close button (24x24 icon)

   **Style:**
   - Bottom border: 1px, Border/Default

5. **Create Content Section:**
   - Frame with auto layout vertical
   - Padding: 24px
   - Gap: 16px
   - Add sample content/form fields

6. **Create Footer Section:**
   - Frame with auto layout horizontal
   - Padding: 24px
   - Gap: 12px
   - Alignment: Right

   **Add Buttons:**
   - Cancel button (secondary)
   - Primary action button

   **Style:**
   - Top border: 1px, Border/Default

7. **Style Modal Container:**
   - Fill: Background/Surface (white)
   - Border radius: 12px
   - Shadow: Shadow/Level 3

8. **Group Everything:**
   - Select overlay + modal
   - Frame selection
   - Name: "Modal/Complete"

9. **Create Component** (Cmd/Ctrl + Option/Alt + K)

10. **Add Variants:**
    - Property "Size": Small (400px), Medium (600px), Large (800px)
    - Property "Type": Default, Confirmation, Form

---

## ✅ Quick Build Tips

### Auto Layout Shortcuts:
- **Shift + A** - Add auto layout
- **Option/Alt + drag** - Adjust padding
- **Command/Ctrl + drag** - Adjust gap

### Component Shortcuts:
- **Cmd/Ctrl + Option/Alt + K** - Create component
- **Cmd/Ctrl + Option/Alt + B** - Create component set

### Selection Shortcuts:
- **Cmd/Ctrl + click** - Deep select
- **Enter** - Select child
- **Shift + Enter** - Select parent

### Measurement Helper:
- **Option/Alt + hover** - Show distances

---

## 🎯 Testing Your Components

After building each component, test:
1. ✅ All variants work correctly
2. ✅ Auto layout resizes properly
3. ✅ Text doesn't overflow
4. ✅ Colors use style references (not hard coded)
5. ✅ Spacing matches design tokens
6. ✅ Component has clear description
7. ✅ Properties are set up correctly
8. ✅ Hover states look good

---

This guide gives you exact specifications to build production-ready components in Figma!
