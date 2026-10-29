# BusinessOS Lime Overview Visual Spec

> Single source of truth extracted from `docs/design-reference/lime-overview.html` and `docs/design-reference/lime-overview.png`.
> Total Elements Extracted: 59 / 59

## Global Geometry & Palette Foundations
- **Frame Radius:** 36px (`rounded-[36px]`)
- **Dock Width & Radius:** 56px (`w-14`), 28px (`rounded-[28px]`)
- **Outer Canvas:** `#E5E7EB` (`rgb(229, 231, 235)`)
- **Frame Background:** `#F8FAFC` (`rgb(248, 250, 252)`)
- **Brand Lime:** `#84CC16` / `#A3E635` gradient
- **Navy Accent:** `#0F172A` / `#020617` (`slate-900` / `slate-950`)
- **Column Tints:**
  - Planned: `rgba(241, 245, 249, 0.6)` (slate-100/60)
  - In Production: `rgba(247, 254, 231, 0.5)` (lime-50/50)
  - Under Review: `rgba(239, 246, 255, 0.4)` (blue-50/40)
  - Delivered: `rgba(236, 253, 245, 0.4)` (emerald-50/40)

## Elements Specification Table

| Element | Bounding Box (x, y, w, h) | Font (Size, Wt) | Color | Background | Border / Radius | Shadow |
|---|---|---|---|---|---|---|
| **Main Frame Window** | (28, 28, 1384x907) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(248, 250, 252)` | 36px / rgba(255, 255, 255, 0.7) | shadow |
| **Top Navigation Container** | (53, 53, 1334x47) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 0px / rgba(226, 232, 240, 0.6) | none |
| **Logo Badge** | (53, 56, 36x36) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | shadow |
| **Primary Nav Container** | (278, 54, 529x40) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(226, 232, 240, 0.6)` | 9999px / rgb(229, 231, 235) | none |
| **Nav Pill: Overview** | (282, 58, 106x32) | 13px / 700 | `rgb(15, 23, 42)` | `rgb(255, 255, 255)` | 9999px / rgb(229, 231, 235) | shadow |
| **Nav Pill: Updates** | (388, 58, 86x32) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Nav Pill: Operations** | (473, 58, 103x32) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Nav Pill: Calendar** | (577, 58, 89x32) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Nav Pill: Clients** | (666, 58, 76x32) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Nav Pill: Files** | (742, 58, 61x32) | 13px / 600 | `rgb(71, 85, 105)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Search Input** | (867, 59, 256x30) | 12px / 400 | `rgb(51, 65, 85)` | `rgba(255, 255, 255, 0.9)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **Team Avatars Pill** | (1135, 55, 124x38) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(255, 255, 255, 0.8)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **Notifications Bell** | (1271, 56, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgb(255, 255, 255)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **Profile Dropdown** | (1319, 53, 68x42) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(255, 255, 255, 0.6)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **Left Floating Dock** | (53, 120, 56x790) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(241, 245, 249)` | 28px / rgba(255, 255, 255, 0.7) | shadow |
| **Theme Toggle Container** | (60, 137, 42x80) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(255, 255, 255, 0.8)` | 9999px / rgba(226, 232, 240, 0.6) | none |
| **Dock Active Item (Dashboard)** | (63, 229, 36x36) | 16px / 400 | `rgb(255, 255, 255)` | `rgb(15, 23, 42)` | 16px / rgb(229, 231, 235) | shadow |
| **Dock Item: Calendar** | (65, 180, 32x32) | 16px / 400 | `rgb(148, 163, 184)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | none |
| **Dock Item: Mail** | (63, 325, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | none |
| **Dock Item: Documents** | (63, 373, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | none |
| **Dock Item: Team** | (63, 421, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | none |
| **Dock Item: Projects** | (63, 469, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | none |
| **Dock Item: Settings** | (63, 517, 36x36) | 16px / 400 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 16px / rgb(229, 231, 235) | none |
| **Header Greeting Section** | (133, 120, 1254x82) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Status Line** | (133, 124, 483x16) | 12px / 600 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Greeting Heading** | (133, 142, 483x40) | 36px / 800 | `rgb(15, 23, 42)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Greeting Subtitle** | (133, 182, 483x20) | 14px / 500 | `rgb(100, 116, 139)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Workspace Status Card** | (1013, 152, 374x50) | 12px / 400 | `rgb(71, 85, 105)` | `rgba(255, 255, 255, 0.9)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **AI Announcement Banner** | (133, 218, 1254x58) | 16px / 400 | `rgb(255, 255, 255)` | `rgb(2, 6, 23)` | 16px / rgb(30, 41, 59) | shadow |
| **AI Banner: Explore Button** | (1159, 233, 86x28) | 12px / 600 | `rgb(51, 65, 85)` | `rgb(241, 245, 249)` | 9999px / rgb(229, 231, 235) | none |
| **AI Banner: Open Assistant Button** | (1253, 233, 117x28) | 12px / 700 | `rgb(132, 204, 22)` | `rgba(132, 204, 22, 0.1)` | 9999px / rgb(229, 231, 235) | none |
| **Summary Tiles Grid** | (133, 292, 1254x136) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Tile 1: New Project (Dashed)** | (133, 292, 306x66) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(255, 255, 255, 0.8)` | 16px / rgb(203, 213, 225) | none |
| **Tile 2: Internal Studio (8 Projects)** | (449, 292, 306x66) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 3: Client Work (14 Jobs)** | (765, 292, 306x66) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 4: Leads & Enquiries (23 Leads)** | (1081, 292, 306x66) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 5: Media Library (186 Assets)** | (133, 368, 306x60) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 6: Files & Contracts (31 Docs)** | (449, 368, 306x60) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 7: Review Queue (6 Reviews)** | (765, 368, 306x60) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Tile 8: Invoices & Finance (₹1.8L Due)** | (1081, 368, 306x60) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Board Action Bar** | (133, 444, 1254x42) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **View Switcher Pill Bar** | (133, 448, 359x38) | 12px / 600 | `rgb(71, 85, 105)` | `rgba(255, 255, 255, 0.9)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **View Tab: Board** | (138, 453, 84x28) | 12px / 700 | `rgb(255, 255, 255)` | `rgb(15, 23, 42)` | 9999px / rgb(229, 231, 235) | none |
| **Toolbar Filters Button** | (1003, 452, 81x30) | 12px / 600 | `rgb(51, 65, 85)` | `rgb(255, 255, 255)` | 9999px / rgba(226, 232, 240, 0.8) | none |
| **Toolbar Ask AI Button** | (1094, 451, 146x32) | 12px / 700 | `rgb(255, 255, 255)` | `rgba(0, 0, 0, 0)` | 9999px / rgb(229, 231, 235) | shadow |
| **Toolbar Create Project Button** | (1250, 451, 137x32) | 12px / 700 | `rgb(255, 255, 255)` | `rgb(15, 23, 42)` | 9999px / rgb(229, 231, 235) | shadow |
| **Kanban Container** | (133, 502, 1254x393) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(0, 0, 0, 0)` | 0px / rgb(229, 231, 235) | none |
| **Column: Planned** | (133, 502, 303x393) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(241, 245, 249, 0.6)` | 22px / rgba(226, 232, 240, 0.5) | none |
| **Column: In Production** | (450, 502, 303x393) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(247, 254, 231, 0.5)` | 22px / rgba(217, 249, 157, 0.5) | none |
| **Column: Under Review** | (767, 502, 303x393) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(239, 246, 255, 0.4)` | 22px / rgba(191, 219, 254, 0.4) | none |
| **Column: Delivered** | (1084, 502, 303x393) | 16px / 400 | `rgb(30, 41, 59)` | `rgba(236, 253, 245, 0.4)` | 22px / rgba(167, 243, 208, 0.4) | none |
| **Card: Brand Film** | (144, 551, 281x221) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Lambo Campaign** | (144, 785, 281x99) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Product Launch (Highlighted)** | (461, 551, 281x221) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(217, 249, 157, 0.6) | shadow |
| **Card: Tarbo App** | (461, 785, 281x99) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Ebay Website** | (778, 551, 281x221) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Fillio Webapp** | (778, 785, 281x99) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Finalize Brand Campaign** | (1095, 551, 281x221) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
| **Card: Social Campaign Q4** | (1095, 785, 281x99) | 16px / 400 | `rgb(30, 41, 59)` | `rgb(255, 255, 255)` | 16px / rgba(226, 232, 240, 0.8) | shadow |
