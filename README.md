# BusinessOS Design System (DS)

The BusinessOS Design System is a modern, token-driven component architecture built for creative and media agency workflows. It provides accessible, responsive, high-performance UI primitives with strict token isolation, zero outside margins, and guaranteed WCAG 2.1 AA accessibility.

---

## 🏛️ Core Engineering Rules

Every component in this design system MUST adhere to these non-negotiable rules:

### 1. Tokens Only (`var(--ds-*)`)

- All styling must reference design system CSS custom properties (`var(--ds-*)`).
- Zero hardcoded colors (`#hex`, `rgb`, `hsl`) or arbitrary pixel values are allowed outside `tokens.json`.
- Spacing must strictly use the 9-tier scale: `4px`, `8px`, `12px`, `16px`, `20px`, `24px`, `32px`, `40px`, `48px` (`var(--ds-space-*)`).
- Elevation and layering must strictly use the 6 Z-index tiers: `base`, `sticky`, `dropdown`, `drawer`, `modal`, `toast` (`var(--ds-z-*)`).

### 2. Zero Outside Margins

- Components must NEVER set their own outer margins (`margin`, `margin-top`, etc.).
- Spacing and positioning must be handled exclusively by layout components (`Stack`, `Inline`, `Grid`, `Frame`) using `gap` and padding.
- **Rule Exception (Overlapping Stacks):** The sole documented exception is compact avatar grouping (`.ds-avatar-group-item:not(:first-child)` and `.ds-avatar-overflow`), which use negative inline margin (`-8px`) paired with a 2px surface ring (`box-shadow: 0 0 0 2px var(--ds-color-surface)`) to render overlapping circular badges.
- This prevents margin-collapse bugs and ensures modular composability.

### 3. Minimum Text Size (at least 12px)

- Minimum font size is strictly `12px` (`var(--ds-text-min)`).
- Sub-12px micro-text is forbidden anywhere in the system to guarantee readability across all devices.

### 4. Lime Brand Fill Rule

- Brand lime (`#84CC16` light / `#A3E635` dark) is permitted **ONLY as a fill / accent background**, never as raw text color.
- Text placed on lime fills must always be dark `#111111` (`var(--ds-color-on-brand)`), guaranteeing at least 9.5:1 contrast in light mode and at least 12.5:1 in dark mode.
- For brand text on neutral surfaces, use dedicated high-contrast tokens (`var(--ds-color-brand-text)`: `#4D7C0F` in light, `#BEF264` in dark).

### 5. Single Component Per Purpose

- Exactly one source of truth per primitive and pattern.
- No redundant duplicate components (e.g. no separate `PrimaryButton`, `SecondaryButton`; use `<Button variant="..." />`).

### 6. `ds-` Class Prefix

- All CSS classes must be prefixed with `ds-` (e.g., `.ds-btn`, `.ds-panel`, `.ds-stack`).
- Never use un-prefixed generic utility classes that could collide with legacy code.

### 7. React `forwardRef`

- All components must use `React.forwardRef<HTMLElement, ComponentProps>`.
- The forwarded ref must be attached to the root interactive/DOM element.

### 8. `className` & `data-testid` Passthrough

- All components must accept optional `className` and `data-testid` props.
- `className` must be merged (concatenated), never replaced.
- `data-testid` must be attached to the root DOM node for automated testing.

---

## 📐 Architecture & Hierarchy

```text
src/packages/ui/src/ds/
├── settings/
│   └── tokens.json            # Single source of truth for all DS tokens
├── styles/
│   ├── base.css               # Imports all styles and fonts
│   ├── tokens.generated.css   # Generated CSS variables for light & dark modes
│   ├── root.css               # DsRoot container & font setup
│   ├── layout.css             # Frame, Stack, Inline, Grid, Panel, Tile, Divider, Container
│   ├── primitives.css         # Button, Input, Select, Checkbox, Switch, Avatar, etc.
│   ├── overlays.css           # Modal, Drawer, Popover, DropdownMenu, Tooltip
│   └── feedback.css           # StatusPill, Toast, EmptyState, Skeleton
├── primitives/                # Buttons, form controls, indicators
├── layout/                    # Layout wrappers & primitives
├── overlays/                  # Modals, drawers, popovers, dropdowns
├── feedback/                  # Status pills, toasts, skeletons, empty states
├── tools/
│   ├── build-tokens.mjs       # Build script generating tokens.generated.css & tokens.ts
│   └── ui-audit.mjs           # WCAG contrast validator & Playwright browser auditor
├── format.ts                  # Currency & date formatters
├── root.tsx                   # DsRoot & useDsMode hook
└── index.ts                   # Unified public barrel export
```

---

## 🛠️ Step-by-Step: Adding a New Component

Follow this checklist when adding a new component to the design system:

### Step 1: Create Component File

Create `src/packages/ui/src/ds/<category>/<ComponentName>.tsx`.

```tsx
import React, { forwardRef } from 'react'

export interface ComponentNameProps extends React.HTMLAttributes<HTMLDivElement> {
  variant?: 'primary' | 'secondary'
  'data-testid'?: string
}

export const ComponentName = forwardRef<HTMLDivElement, ComponentNameProps>(
  ({ variant = 'primary', className = '', 'data-testid': testId, children, ...rest }, ref) => {
    return (
      <div
        ref={ref}
        className={`ds-component-name ds-component-name--${variant} ${className}`.trim()}
        data-testid={testId}
        {...rest}
      >
        {children}
      </div>
    )
  }
)

ComponentName.displayName = 'ComponentName'
```

### Step 2: Add Component Styles

Add class definitions in `src/packages/ui/src/ds/styles/<category>.css`.

- Ensure all colors, paddings, borders, shadows, and radii use `var(--ds-*)`.
- Never set `margin`.
- Ensure `font-size >= var(--ds-text-min)`.

### Step 3: Export from Barrel Files

1. Export from category index `src/packages/ui/src/ds/<category>/index.ts`.
2. Export from root barrel `src/packages/ui/src/ds/index.ts`.

### Step 4: Write Unit Tests

Create `src/apps/web/src/tests/ds/ds-<component>.test.tsx`:

- Test default render and variants.
- Test disabled/loading/interactive states.
- Test `ref` forwarding.
- Test `data-testid` and `className` passthrough.
- Test keyboard interactions and ARIA accessibility.

### Step 5: Add to Dev Showcase Page

Add an interactive demonstration in `src/apps/web/src/pages/dev/DsShowcasePage.tsx` under `/dev/ds`.
Show all states (default, hover, focus, pressed, disabled, loading, error) and verify inside the 300px narrow container.

### Step 6: Verify & Audit

Run the automated verification suite:

```bash
# 1. Lint DS compliance (no hardcoded colors, strict prefixing, etc.)
pnpm ui:lint

# 2. Automated browser audit (WCAG contrast, overflow, micro-text, screenshots)
pnpm ui:audit --browser

# 3. TypeScript typecheck
pnpm typecheck

# 4. Unit tests
pnpm test
```
