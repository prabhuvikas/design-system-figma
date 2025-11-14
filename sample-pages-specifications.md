# Sample Dashboard Pages - Build Specifications

## Complete specifications for building sample dashboard pages in Figma

---

## 📊 Page 1: Main Dashboard - "Overview"

### Frame Setup:
- **Size:** 1440 x 1024px
- **Name:** "Dashboard - Overview [1440]"
- **Background:** Background/Default (#E4E7EA)
- **Grid:** 12 columns, 24px gutter, 80px margins (1440 breakpoint)

---

### Layout Structure:

```
┌─────────────────────────────────────────────────────────────┐
│ [Top Bar Component - 1440px x 64px]                         │
├──────┬──────────────────────────────────────────────────────┤
│      │ Page Header                                          │
│      │ ─────────────────────────────────────────────────────│
│  S   │ Dashboard    Home > Dashboard                        │
│  I   │                                                      │
│  D   │ KPI Section (4 columns x 3 grid columns each)       │
│  E   │ ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐       │
│  B   │ │ Total  │ │ Active │ │Revenue │ │ Growth │       │
│  A   │ │ Users  │ │ Users  │ │        │ │  Rate  │       │
│  R   │ │        │ │        │ │        │ │        │       │
│      │ │ 24,561 │ │ 18,432 │ │$125.5K │ │ +12.5% │       │
│  2   │ │  ↑ 12% │ │  ↑ 8%  │ │ ↑ 15%  │ │        │       │
│  4   │ └────────┘ └────────┘ └────────┘ └────────┘       │
│  0   │                                                      │
│  p   │ Chart Section (8 + 4 columns)                       │
│  x   │ ┌──────────────────────┐ ┌──────────────┐         │
│      │ │                      │ │              │         │
│      │ │  Revenue Chart       │ │ Top Products │         │
│      │ │  [Chart Placeholder] │ │              │         │
│      │ │                      │ │ • Product A  │         │
│      │ │                      │ │ • Product B  │         │
│      │ │                      │ │ • Product C  │         │
│      │ └──────────────────────┘ └──────────────┘         │
│      │                                                      │
│      │ Recent Activity Section (12 columns)                │
│      │ ┌────────────────────────────────────────────────┐ │
│      │ │ Recent Orders                                  │ │
│      │ │ ───────────────────────────────────────────────│ │
│      │ │ [Data Table with 5 rows]                       │ │
│      │ │                                                 │ │
│      │ └────────────────────────────────────────────────┘ │
└──────┴──────────────────────────────────────────────────────┘
```

---

### Step-by-Step Build Instructions:

#### 1. Create Base Frame
1. Press **F** to create frame
2. Set dimensions: 1440 x 1024px
3. Name: "Dashboard - Overview [1440]"
4. Fill: Background/Default color

#### 2. Apply Layout Grid
1. Select frame
2. Click **+** next to Layout grid
3. Settings:
   - Columns: 12
   - Gutter: 24px
   - Margin: 80px
   - Type: Stretch
   - Color: Red at 10% opacity (for visibility)

#### 3. Add Top Bar
1. Place **TopBar** component instance
2. Position: X: 0, Y: 0
3. Width: 1440px
4. Make sure it's full width

#### 4. Add Sidebar
1. Place **Sidebar/Expanded** component instance
2. Position: X: 0, Y: 64 (below top bar)
3. Height: 960px (1024 - 64)
4. Keep 240px width

#### 5. Create Content Container
1. Create frame for main content
2. Position: X: 240 (after sidebar), Y: 64
3. Width: 1200px (1440 - 240)
4. Height: Auto
5. Auto layout: Vertical
6. Padding: 40px (top), 80px (left/right), 40px (bottom)
7. Gap: 32px

#### 6. Add Page Header
Inside content container:

**Create frame with auto layout:**
- Direction: Horizontal
- Space between: justify
- Alignment: center

**Left side:**
- Heading/H1: "Dashboard"

**Right side:**
- Breadcrumbs text: "Home > Dashboard"
- Style: Body/Regular
- Color: Text/Secondary

#### 7. Create KPI Cards Section

**Container frame:**
- Auto layout: Horizontal
- Gap: 24px
- Fill: container width

**For each KPI Card (4 total):**

1. Create frame: Auto width x 140px
2. Auto layout: Vertical
3. Padding: 24px
4. Gap: 12px
5. Fill: Background/Surface (white)
6. Border radius: 12px
7. Shadow: Shadow/Level 1

**Card 1 - Total Users:**
```
Label (Caption style): "Total Users"
Value (H1 style): "24,561"
Change indicator:
  - Frame with horizontal auto layout
  - Up arrow icon (16x16) - green
  - Text: "+12%" - Success color
  - Gap: 4px
```

**Card 2 - Active Users:**
```
Label: "Active Users"
Value: "18,432"
Change: "↑ 8%" (green)
```

**Card 3 - Revenue:**
```
Label: "Total Revenue"
Value: "$125.5K"
Change: "↑ 15%" (green)
```

**Card 4 - Growth Rate:**
```
Label: "Growth Rate"
Value: "+12.5%"
No change indicator (or neutral)
```

#### 8. Create Chart Section

**Container frame:**
- Auto layout: Horizontal
- Gap: 24px
- Fill: container width

**Chart Card (8 columns = ~800px):**
1. Place Card/Large component
2. Width: ~800px, Height: 400px

**Header:**
- Title: "Revenue Overview"
- Dropdown: "Last 7 days"

**Content:**
- Chart placeholder:
  - Rectangle with gradient
  - Or use plugin like "Chart" to create visual
  - Show line/area chart style
  - Axes labels

**Top Products Card (4 columns = ~376px):**
1. Place Card/Medium component
2. Width: ~376px

**Content - Product List:**
```
Product Item (frame with auto layout horizontal):
├── Product icon/image (40x40)
├── Details (auto layout vertical)
│   ├── Product name (Body/Regular, Bold)
│   └── Sales: "$1,234" (Body/Caption)
└── Badge: "↑ 15%" (success)

Repeat for 5 products
Gap between items: 16px
```

#### 9. Create Recent Orders Table Section

**Container:**
- Full width (12 columns)
- Card with title "Recent Orders"

**Table:**
Use the Table component you built, or create here:

**Headers:**
- Order ID
- Customer
- Product
- Amount
- Status
- Date
- Actions

**Sample Row 1:**
```
#ORD-001 | John Doe | Product A | $299 | [Completed Badge] | Oct 24 | [•••]
```

**Sample Row 2:**
```
#ORD-002 | Jane Smith | Product B | $449 | [Pending Badge] | Oct 24 | [•••]
```

Repeat for 5 rows

**Status Badge variants:**
- Completed: Success (green)
- Pending: Warning (yellow)
- Cancelled: Error (red)
- Processing: Info (blue)

---

## 👥 Page 2: Users Table - "User Management"

### Frame Setup:
- **Size:** 1440 x 1024px
- **Name:** "Users - Table View [1440]"
- **Background:** Background/Default

---

### Layout Structure:

```
┌────────────────────────────────────────────────────┐
│ [Top Bar - Full width]                             │
├──────┬─────────────────────────────────────────────┤
│      │ Users                                       │
│      │                                             │
│  S   │ ┌───────────────────────────────────────┐  │
│  I   │ │ Search + Filters + Add User Button    │  │
│  D   │ └───────────────────────────────────────┘  │
│  E   │                                             │
│  B   │ ┌───────────────────────────────────────┐  │
│  A   │ │                                       │  │
│  R   │ │  [ Data Table - Users List ]          │  │
│      │ │                                       │  │
│  2   │ │  15 rows showing user data            │  │
│  4   │ │                                       │  │
│  0   │ │  - Avatar + Name                      │  │
│      │ │  - Email                              │  │
│      │ │  - Role Badge                         │  │
│      │ │  - Status                             │  │
│      │ │  - Join Date                          │  │
│      │ │  - Actions Menu                       │  │
│      │ │                                       │  │
│      │ └───────────────────────────────────────┘  │
│      │                                             │
│      │        [Pagination: 1 2 3 ... 10]          │
└──────┴─────────────────────────────────────────────┘
```

---

### Build Instructions:

#### 1. Base Frame + Grid
Same as Page 1

#### 2. Add Top Bar + Sidebar
Same as Page 1

#### 3. Add Page Header
- Heading/H1: "Users"
- Right side: "Add User" button (Primary, Medium)

#### 4. Create Filter Bar

**Frame with auto layout horizontal:**
- Space between: justify
- Padding: 16px
- Background: Surface (white)
- Border radius: 8px
- Shadow: Level 1

**Left side - Search & Filters:**
```
Search input (320px width)
Filter dropdown: "All Roles"
Filter dropdown: "All Status"
Gap: 12px
```

**Right side:**
```
Export button (Secondary)
Add User button (Primary)
```

#### 5. Create Users Table

**Table Header:**
```
☐ | Avatar | Name | Email | Role | Status | Join Date | Actions
```

**Sample User Rows:**

**Row 1:**
```
☐ | [AV] | John Smith | john@example.com | [Admin] | Active | Oct 15, 2024 | [•••]
```

**Row 2:**
```
☐ | [AV] | Sarah Johnson | sarah@example.com | [Editor] | Active | Oct 10, 2024 | [•••]
```

**Row 3:**
```
☐ | [AV] | Mike Williams | mike@example.com | [User] | Inactive | Oct 5, 2024 | [•••]
```

Continue for 12-15 rows

**Role Badges:**
- Admin: Info (blue)
- Editor: Warning (yellow)
- User: Neutral (gray)
- Moderator: Success (green)

**Status:**
- Active: Green dot + text
- Inactive: Gray dot + text

**Actions Menu:**
- Three dots icon
- On click shows: View, Edit, Delete

#### 6. Add Pagination
Place pagination component at bottom center

---

## 📝 Page 3: User Detail - "User Profile"

### Frame Setup:
- **Size:** 1440 x 1024px
- **Name:** "User Detail [1440]"

---

### Layout Structure:

```
┌────────────────────────────────────────────────────┐
│ [Top Bar]                                          │
├──────┬─────────────────────────────────────────────┤
│      │ ← Back  User Profile                       │
│      │                                             │
│  S   │ ┌──────────────────┐  ┌──────────────────┐│
│  I   │ │                  │  │                  ││
│  D   │ │   Main Profile   │  │   Quick Info     ││
│  E   │ │      Card        │  │      Card        ││
│  B   │ │                  │  │                  ││
│  A   │ │  [Avatar]        │  │  Status: Active  ││
│  R   │ │  John Smith      │  │  Role: Admin     ││
│      │ │  john@email.com  │  │  Joined: Oct 15  ││
│      │ │                  │  │                  ││
│      │ │  About           │  │  [Edit Button]   ││
│      │ │  Bio text...     │  │  [Delete Button] ││
│      │ │                  │  │                  ││
│      │ └──────────────────┘  └──────────────────┘│
│      │                                             │
│      │ ┌───────────────────────────────────────┐  │
│      │ │  Activity Timeline                    │  │
│      │ │  ──────────────────────────────────── │  │
│      │ │                                       │  │
│      │ │  • Logged in - 2 hours ago           │  │
│      │ │  • Updated profile - Yesterday        │  │
│      │ │  • Created post - 2 days ago         │  │
│      │ │  • Joined team - Oct 15, 2024        │  │
│      │ │                                       │  │
│      │ └───────────────────────────────────────┘  │
└──────┴─────────────────────────────────────────────┘
```

---

### Build Instructions:

#### 1. Add Back Button + Title

**Header frame (horizontal auto layout):**
```
← Back button (icon + text)
Gap: 16px
Title: "User Profile"
```

#### 2. Create Two-Column Layout

**Container:**
- Auto layout: Horizontal
- Gap: 24px
- Alignment: Top

#### 3. Main Profile Card (Left - 8 columns)

**Card structure (vertical auto layout, 24px padding, 16px gap):**

**Profile Header:**
```
Avatar (80x80) - centered
Name (H2): "John Smith"
Email (Body/Regular): "john@example.com"
Verified badge (optional)
```

**Divider line**

**About Section:**
```
Label (Caption, Bold): "ABOUT"
Bio text (Body/Regular):
  "Senior product manager with 5+ years experience
   in building user-centric products..."
```

**Divider line**

**Contact Information:**
```
Label: "CONTACT INFORMATION"

Phone: +1 (555) 123-4567
Location: San Francisco, CA
Department: Product Team
```

**Divider line**

**Statistics:**
```
Three stat blocks (horizontal):
├── Projects: 24
├── Tasks: 156
└── Reviews: 89
```

#### 4. Quick Info Card (Right - 4 columns)

**Card structure:**

**Status Badge (large):**
```
• Active (green badge, centered)
```

**Info List:**
```
Role
[Admin Badge]

Member Since
October 15, 2024

Last Active
2 hours ago

Email Verified
✓ Yes
```

**Divider**

**Action Buttons (vertical stack, 12px gap):**
```
[Edit Profile] - Primary button, full width
[Send Message] - Secondary button, full width
[Delete User] - Tertiary button, full width, red text
```

#### 5. Activity Timeline Card (Full width below)

**Card with timeline:**

```
Activity Timeline (H3)
───────────────────────────────

Timeline items (vertical, 16px gap):

┌─ ● Logged in successfully
│    2 hours ago
│    From: Chrome on Mac
│
├─ ● Updated profile information
│    Yesterday at 3:45 PM
│    Changed: Email, Phone
│
├─ ● Created new project "Dashboard Redesign"
│    2 days ago
│    Status: In Progress
│
├─ ● Uploaded 5 documents
│    3 days ago
│    Files: design-specs.pdf, mockups.fig...
│
└─ ● Joined the team
     October 15, 2024
     Invited by: Sarah Johnson
```

---

## ⚙️ Page 4: Settings - "Account Settings"

### Frame Setup:
- **Size:** 1440 x 1024px
- **Name:** "Settings [1440]"

---

### Layout Structure:

```
┌────────────────────────────────────────────────────┐
│ [Top Bar]                                          │
├──────┬─────────────────────────────────────────────┤
│      │ Settings                                    │
│      │                                             │
│  S   │ ┌──────────┐  ┌─────────────────────────┐ │
│  I   │ │          │  │                         │ │
│  D   │ │ Settings │  │  General Settings       │ │
│  E   │ │  Menu    │  │  ─────────────────────  │ │
│  B   │ │          │  │                         │ │
│  A   │ │► General │  │  Profile Photo          │ │
│  R   │ │  Account │  │  [Avatar Upload]        │ │
│      │ │  Security│  │                         │ │
│      │ │  Notif.  │  │  Display Name           │ │
│      │ │  Billing │  │  [Input Field]          │ │
│      │ │  Privacy │  │                         │ │
│      │ │          │  │  Email Address          │ │
│      │ │          │  │  [Input Field]          │ │
│      │ │          │  │                         │ │
│      │ │          │  │  Bio                    │ │
│      │ │          │  │  [Textarea]             │ │
│      │ │          │  │                         │ │
│      │ │          │  │  [Cancel] [Save Changes]│ │
│      │ └──────────┘  └─────────────────────────┘ │
└──────┴─────────────────────────────────────────────┘
```

---

### Build Instructions:

#### 1. Create Two-Column Layout

**Container (horizontal):**
- Left column: 240px (fixed)
- Right column: Fill remaining
- Gap: 24px

#### 2. Settings Menu (Left)

**Frame (vertical auto layout):**
- Width: 240px
- Padding: 0
- Gap: 4px

**Menu Items:**
```
General (active)
├─ Background: Primary at 10%
├─ Text: Primary color
└─ Border left: 3px Primary

Account (inactive)
Security (inactive)
Notifications (inactive)
Billing (inactive)
Privacy (inactive)

Each item:
- Padding: 12px 16px
- Body/Regular font
- Border radius: 8px
- Hover: light background
```

#### 3. Settings Content Area (Right)

**Card container:**
- Fill: Surface (white)
- Padding: 32px
- Border radius: 12px
- Shadow: Level 1

**Form Layout (vertical, 24px gap):**

**Section 1: Profile Photo**
```
Label: "Profile Photo"
Current avatar (80x80)
[Upload New Photo] button
[Remove] button (text only)
```

**Divider**

**Section 2: Basic Information**
```
Input Field:
├─ Label: "Display Name"
├─ Input: "John Smith"
└─ Helper: "This is how your name appears to others"

Input Field:
├─ Label: "Email Address"
├─ Input: "john@example.com"
└─ Helper: "Your primary email for notifications"

Input Field (Textarea):
├─ Label: "Bio"
├─ Input: "Product manager passionate about..."
└─ Helper: "Brief description for your profile"
```

**Divider**

**Section 3: Location & Language**
```
Dropdown:
├─ Label: "Timezone"
└─ Selected: "Pacific Time (PT)"

Dropdown:
├─ Label: "Language"
└─ Selected: "English (US)"
```

**Divider**

**Action Buttons (horizontal, right aligned):**
```
[Cancel] - Secondary button
[Save Changes] - Primary button
Gap: 12px
```

---

## 🔐 Page 5: Login Page - "Authentication"

### Frame Setup:
- **Size:** 1440 x 1024px
- **Name:** "Login [1440]"
- **Background:** Gradient or image

---

### Layout Structure:

```
┌────────────────────────────────────────────────────┐
│                                                    │
│                                                    │
│              [Logo/Brand]                          │
│                                                    │
│          ┌──────────────────────┐                 │
│          │                      │                 │
│          │   Welcome Back       │                 │
│          │                      │                 │
│          │   Email Address      │                 │
│          │   [Input Field]      │                 │
│          │                      │                 │
│          │   Password           │                 │
│          │   [Input Field]      │                 │
│          │                      │                 │
│          │   ☐ Remember me      │                 │
│          │        Forgot password?│                 │
│          │                      │                 │
│          │   [Sign In Button]   │                 │
│          │                      │                 │
│          │   ──── OR ────      │                 │
│          │                      │                 │
│          │   [Sign in with Google]│               │
│          │   [Sign in with GitHub]│               │
│          │                      │                 │
│          │   Don't have account?│                 │
│          │   Sign up            │                 │
│          │                      │                 │
│          └──────────────────────┘                 │
│                                                    │
└────────────────────────────────────────────────────┘
```

---

### Build Instructions:

#### 1. Create Centered Card

**Card (400px width, auto height):**
- Position: Center of frame
- Padding: 40px
- Background: Surface (white)
- Border radius: 12px
- Shadow: Level 3

#### 2. Card Content (vertical, 24px gap)

**Logo:**
```
Brand logo or text (centered)
32px height
```

**Header:**
```
H2: "Welcome Back"
Body/Regular: "Sign in to your account"
Text align: center
Gap: 8px
```

**Form Fields:**
```
Input Field:
├─ Label: "Email Address"
├─ Input placeholder: "you@example.com"
└─ Type: email

Input Field:
├─ Label: "Password"
├─ Input placeholder: "••••••••"
└─ Type: password, with show/hide icon
```

**Options Row (horizontal, space between):**
```
Left: ☐ Remember me (checkbox + text)
Right: "Forgot password?" (link)
```

**Sign In Button:**
```
Primary button
Full width
Large size
Text: "Sign In"
```

**Divider with text:**
```
Line ──── "OR" ──── Line
```

**Social Login Buttons:**
```
Secondary button, full width:
[G] Sign in with Google

Secondary button, full width:
[GitHub icon] Sign in with GitHub

Gap: 12px
```

**Footer:**
```
Center aligned text:
"Don't have an account? " (regular)
"Sign up" (link, primary color)
```

---

## 🎨 Color & Styling Tips

### Consistency Checklist:
- ✅ All cards use Background/Surface fill
- ✅ All shadows use defined shadow styles
- ✅ All text uses text styles (not hard-coded)
- ✅ All colors reference color styles
- ✅ All spacing uses multiples of 4 (4, 8, 12, 16, 24, 32)
- ✅ All border radius consistent (8px buttons, 12px cards)

### Visual Hierarchy:
- **Page titles:** H1 (32px)
- **Section headers:** H2 (24px)
- **Card titles:** H3 (20px)
- **Body content:** Body/Regular (14px)
- **Labels:** Body/Caption (12px)

### Spacing Guidelines:
- Component padding: 24px
- Section gaps: 32px
- Form field gaps: 16px
- Button groups gap: 12px
- List items gap: 8px

---

Build these pages in this order, and you'll have a complete dashboard design system! 🚀
