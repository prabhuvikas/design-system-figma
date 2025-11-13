# Design System Directory Structure

## Overview
This design system follows **Atomic Design** methodology for organizing components and assets.

## Directory Structure

```
design-system-figma/
│
├── design-tokens.json           # Core design tokens (colors, spacing, typography)
├── grid-system.md               # Grid system documentation
├── component-specifications.md   # Detailed component specs
├── README.md                     # Main documentation
│
├── components/                   # Component library
│   ├── atoms/                   # Basic building blocks
│   │   ├── Button/
│   │   ├── Input/
│   │   ├── Label/
│   │   ├── Icon/
│   │   ├── Badge/
│   │   └── Checkbox/
│   │
│   ├── molecules/               # Simple component combinations
│   │   ├── InputField/         # Input + Label + Helper
│   │   ├── SearchBar/          # Input + Icon + Button
│   │   ├── NavItem/            # Icon + Label
│   │   ├── CardHeader/         # Title + Action
│   │   └── Pagination/
│   │
│   ├── organisms/              # Complex component combinations
│   │   ├── NavigationSidebar/
│   │   ├── TopBar/
│   │   ├── DataTable/
│   │   ├── Modal/
│   │   ├── Card/
│   │   └── Form/
│   │
│   └── templates/              # Page-level layouts
│       ├── DashboardLayout/
│       ├── SettingsLayout/
│       ├── ListView/
│       └── DetailView/
│
├── styles/                     # Styling resources
│   ├── variables.css          # CSS custom properties
│   ├── reset.css              # CSS reset/normalize
│   ├── typography.css         # Typography styles
│   ├── utilities.css          # Utility classes
│   └── breakpoints.css        # Responsive breakpoints
│
├── assets/                    # Static assets
│   ├── icons/                # Icon library (SVG)
│   └── images/               # Images and illustrations
│
└── docs/                     # Additional documentation
    ├── color-system.md
    ├── typography-guide.md
    ├── spacing-guide.md
    ├── accessibility.md
    └── figma-setup.md
```

## Component File Structure

Each component directory should contain:

```
ComponentName/
├── ComponentName.jsx           # Component implementation (React example)
├── ComponentName.module.css    # Component styles
├── ComponentName.stories.js    # Storybook stories
├── ComponentName.test.js       # Unit tests
└── README.md                   # Component documentation
```

## Naming Conventions

### Files
- Use PascalCase for component files: `Button.jsx`, `InputField.jsx`
- Use kebab-case for utility files: `design-tokens.json`, `grid-system.md`

### Components
- Use PascalCase: `Button`, `NavigationSidebar`, `DataTable`
- Be descriptive and specific: `PrimaryButton`, `SecondaryButton`

### CSS Classes
- Use kebab-case: `.button-primary`, `.nav-item-active`
- Use BEM notation for variants: `.button--large`, `.button--disabled`

### Variables (CSS)
- Use kebab-case with double dash: `--color-primary`, `--spacing-lg`
- Group by category: `--color-*`, `--spacing-*`, `--font-*`

## Asset Organization

### Icons
```
assets/icons/
├── navigation/
│   ├── home.svg
│   ├── settings.svg
│   └── profile.svg
├── actions/
│   ├── edit.svg
│   ├── delete.svg
│   └── add.svg
└── status/
    ├── success.svg
    ├── error.svg
    └── warning.svg
```

### Size Variants
- 16px: Small icons
- 20px: Navigation icons
- 24px: Default UI icons
- 32px+: Large feature icons

## Implementation Approach

### Phase 1: Foundation
1. Set up design tokens
2. Create base styles (reset, typography, utilities)
3. Implement grid system

### Phase 2: Atoms
1. Build basic components (Button, Input, Icon, Badge)
2. Create all states and variants
3. Write documentation and stories

### Phase 3: Molecules
1. Combine atoms into molecules
2. Implement common patterns
3. Test compositions

### Phase 4: Organisms
1. Build complex components
2. Implement layouts
3. Create interactive examples

### Phase 5: Templates
1. Design page templates
2. Create responsive layouts
3. Document usage patterns

## Version Control

### Branch Strategy
- `main` - Production-ready code
- `develop` - Development branch
- `feature/*` - Feature branches
- `component/*` - Component-specific branches

### Commit Messages
```
feat(Button): add loading state
fix(Input): correct focus outline
docs(README): update installation guide
style(Card): adjust padding values
```

## Framework Integration

### React
```jsx
import { Button } from '@design-system/components';
import tokens from '@design-system/tokens';

<Button size="large" variant="primary">
  Click Me
</Button>
```

### Vue
```vue
<template>
  <ds-button size="large" variant="primary">
    Click Me
  </ds-button>
</template>

<script>
import { DsButton } from '@design-system/components';
</script>
```

### Vanilla CSS
```html
<button class="button button--large button--primary">
  Click Me
</button>
```

## Documentation

Each component should have:
- **Purpose:** What problem does it solve?
- **Anatomy:** What are its parts?
- **States:** What states does it have?
- **Variants:** What variants are available?
- **Accessibility:** ARIA labels, keyboard navigation
- **Examples:** Code examples and live demos
- **Best Practices:** When to use, when not to use

## Accessibility Guidelines

- All interactive elements must be keyboard accessible
- Maintain color contrast ratios (WCAG AA minimum)
- Provide ARIA labels for screen readers
- Support reduced motion preferences
- Ensure responsive text sizing

## Browser Support

- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)
- Mobile Safari (iOS 12+)
- Chrome Mobile (Android 8+)
