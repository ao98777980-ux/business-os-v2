# BusinessOS Phase R3e Visual Parity & Evidence Audit Report

> **Audit Viewport:** 1440 × 900 (Canonical), 1024 × 768, 768 × 1024, 390 × 844, 360 × 740
> **Desktop Pixel Parity:** **93.73% Match** (6.27% Diff)
> **Elements Evaluated:** **179 Elements** (Target: $\ge 120$)
> **Discrete Visual Regions Evaluated:** **25 Regions** (Target: $\ge 20$)

## 1. R3b Evidence Verification Table

| Viewport | Mode | Route Tested | Computed Canvas | Computed Frame | Computed Ink | Disparity Check | SVG Text Check |
|---|---|---|---|---|---|---|---|
| **1440 × 900** | Light | `/dev/lime-overview` | `rgb(229, 231, 235)` | `rgb(248, 250, 252)` | `rgb(15, 23, 42)` | ✅ PASS | ✅ 0 Clipped, 0 Overlapping |
| **1440 × 900** | Dark | `/dev/lime-overview` | `rgb(11, 14, 17)` | `rgb(18, 22, 27)` | `rgb(241, 245, 249)` | ✅ PASS | ✅ 0 Clipped, 0 Overlapping |

## 2. Discrete Region Parity Table (25 Regions)

| Region Name | Bounding Box | Differing Pixels | Visual Match % | Status |
|---|---|---|---|---|
| **TopNav: Brand Logo & Title** | `(53, 56, 199x36)` | 950 / 7164 | **86.74%** | ❌ FAIL |
| **TopNav: Primary Nav Pills** | `(278, 54, 493x36)` | 1628 / 17748 | **90.83%** | ❌ FAIL |
| **TopNav: Search & User Controls** | `(867, 53, 520x36)` | 1675 / 18720 | **91.05%** | ❌ FAIL |
| **Floating Quick Dock Rail** | `(53, 120, 56x790)` | 685 / 44240 | **98.45%** | ✅ PASS |
| **Header Greeting Typography** | `(133, 124, 408x72)` | 5399 / 29376 | **81.62%** | ❌ FAIL |
| **Workspace Status Health Card** | `(1013, 152, 374x50)` | 2551 / 18700 | **86.36%** | ❌ FAIL |
| **AI Announcement Banner** | `(133, 218, 1254x58)` | 6816 / 72732 | **90.63%** | ❌ FAIL |
| **Summary Tile 1: New Project** | `(133, 292, 306x66)` | 994 / 20196 | **95.08%** | ✅ PASS |
| **Summary Tile 2: Internal Studio** | `(449, 292, 306x66)` | 964 / 20196 | **95.23%** | ✅ PASS |
| **Summary Tile 3: Client Work** | `(765, 292, 306x66)` | 895 / 20196 | **95.57%** | ✅ PASS |
| **Summary Tile 4: Leads & Enquiries** | `(1081, 292, 306x66)` | 856 / 20196 | **95.76%** | ✅ PASS |
| **Summary Tile 5: Media Library** | `(133, 368, 306x60)` | 929 / 18360 | **94.94%** | ❌ FAIL |
| **Summary Tile 6: Files & Contracts** | `(449, 368, 306x60)` | 797 / 18360 | **95.66%** | ✅ PASS |
| **Summary Tile 7: Review Queue** | `(765, 368, 306x60)` | 884 / 18360 | **95.19%** | ✅ PASS |
| **Summary Tile 8: Invoices & Finance** | `(1081, 368, 306x60)` | 1184 / 18360 | **93.55%** | ❌ FAIL |
| **Board Action Bar: View Switcher** | `(133, 448, 358x34)` | 1359 / 12172 | **88.84%** | ❌ FAIL |
| **Board Action Bar: Buttons** | `(1003, 451, 384x28)` | 2542 / 10752 | **76.36%** | ❌ FAIL |
| **Column 1 Planned Header** | `(144, 513, 281x27)` | 144 / 7587 | **98.10%** | ✅ PASS |
| **Column 2 Production Header** | `(461, 513, 281x27)` | 121 / 7587 | **98.41%** | ✅ PASS |
| **Column 3 Review Header** | `(778, 513, 281x27)` | 161 / 7587 | **97.88%** | ✅ PASS |
| **Column 4 Delivered Header** | `(1095, 513, 281x27)` | 202 / 7587 | **97.34%** | ✅ PASS |
| **Card 1.1: Brand Film** | `(144, 551, 281x221)` | 3363 / 62101 | **94.58%** | ❌ FAIL |
| **Card 2.1: Product Launch (Highlighted)** | `(461, 551, 281x221)` | 4072 / 62101 | **93.44%** | ❌ FAIL |
| **Card 3.1: Ebay Website** | `(778, 551, 281x221)` | 5755 / 62101 | **90.73%** | ❌ FAIL |
| **Card 4.1: Finalize Brand Campaign** | `(1095, 551, 281x221)` | 6555 / 62101 | **89.44%** | ❌ FAIL |

## 3. Element Delta Verification Table (179 Elements)

| Element Name | Reference BBox | Rebuild BBox | $\Delta x$ | $\Delta y$ | $\Delta w$ | $\Delta h$ | Status |
|---|---|---|---|---|---|---|---|
| **Main Frame Window** | `(28, 28, 1384x907)` | `(28, 28, 1384x925)` | 0px | 0px | 0px | 18px | ⚠️ DEVIATION |
| **Top Navigation Container** | `(53, 53, 1334x47)` | `(53, 53, 1334x47)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Left Floating Dock** | `(53, 120, 56x790)` | `(53, 120, 56x790)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Content Workspace** | `(133, 120, 1254x775)` | `(133, 120, 1254x808)` | 0px | 0px | 0px | 33px | ⚠️ DEVIATION |
| **Nav: Logo Icon Box** | `(53, 56, 36x36)` | `(53, 56, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Nav: Brand Title** | `(101, 60, 112x28)` | `(66, 66, 10x16)` | 35px | 6px | 102px | 12px | ⚠️ DEVIATION |
| **Nav: Pro Badge** | `(219, 69, 35x19)` | `(66, 66, 10x16)` | 153px | 3px | 25px | 3px | ⚠️ DEVIATION |
| **Nav: Pill Container** | `(278, 54, 529x40)` | `(268, 56, 493x36)` | 10px | 2px | 36px | 4px | ⚠️ DEVIATION |
| **Nav: Pill Overview** | `(282, 58, 106x32)` | `(273, 61, 93x26)` | 9px | 3px | 13px | 6px | ⚠️ DEVIATION |
| **Nav: Pill Updates** | `(388, 58, 86x32)` | `(371, 61, 75x26)` | 17px | 3px | 11px | 6px | ⚠️ DEVIATION |
| **Nav: Pill Operations** | `(473, 58, 103x32)` | `(450, 61, 91x26)` | 23px | 3px | 12px | 6px | ⚠️ DEVIATION |
| **Nav: Pill Calendar** | `(577, 58, 89x32)` | `(546, 61, 79x26)` | 31px | 3px | 10px | 6px | ⚠️ DEVIATION |
| **Nav: Pill Clients** | `(666, 58, 76x32)` | `(629, 61, 68x26)` | 37px | 3px | 8px | 6px | ⚠️ DEVIATION |
| **Nav: Pill Files** | `(742, 58, 61x32)` | `(701, 61, 55x26)` | 41px | 3px | 6px | 6px | ⚠️ DEVIATION |
| **Nav: Search Box** | `(867, 59, 256x30)` | `(859, 59, 256x30)` | 8px | 0px | 0px | 0px | ⚠️ DEVIATION |
| **Nav: Search Input** | `(867, 59, 256x30)` | `(859, 59, 256x30)` | 8px | 0px | 0px | 0px | ⚠️ DEVIATION |
| **Nav: Team Avatars Pill** | `(1135, 55, 124x38)` | `(1127, 56, 138x36)` | 8px | 1px | 14px | 2px | ⚠️ DEVIATION |
| **Nav: Notifications Bell** | `(1271, 56, 36x36)` | `(1277, 56, 36x36)` | 6px | 0px | 0px | 0px | ⚠️ DEVIATION |
| **Nav: Profile Dropdown** | `(1319, 53, 68x42)` | `(1325, 56, 62x36)` | 6px | 3px | 6px | 6px | ⚠️ DEVIATION |
| **Dock: Theme Switcher** | `(60, 137, 42x80)` | `(60, 137, 42x80)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Sun Light Toggle** | `(65, 142, 32x32)` | `(65, 142, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Moon Dark Toggle** | `(65, 180, 32x32)` | `(65, 180, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Dashboard (Active)** | `(63, 229, 36x36)` | `(63, 229, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Calendar** | `(63, 277, 36x36)` | `(63, 277, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Mail** | `(63, 325, 36x36)` | `(63, 325, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Documents** | `(63, 373, 36x36)` | `(63, 373, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Team** | `(63, 421, 36x36)` | `(63, 421, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Projects** | `(63, 469, 36x36)` | `(63, 469, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Settings** | `(63, 517, 36x36)` | `(63, 517, 36x36)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Help** | `(65, 821, 32x32)` | `(65, 821, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Dock: Logout** | `(65, 861, 32x32)` | `(65, 861, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Header Greeting Section** | `(133, 120, 1254x82)` | `(133, 120, 1254x82)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Status Line** | `(133, 124, 483x16)` | `(133, 130, 408x18)` | 0px | 6px | 75px | 2px | ⚠️ DEVIATION |
| **Greeting Heading** | `(133, 142, 483x40)` | `(133, 150, 408x35)` | 0px | 8px | 75px | 5px | ⚠️ DEVIATION |
| **Greeting Subtitle** | `(133, 182, 483x20)` | `(133, 188, 408x14)` | 0px | 6px | 75px | 6px | ⚠️ DEVIATION |
| **Workspace Status Card** | `(1013, 152, 374x50)` | `(1013, 152, 374x50)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Status: Health Badge** | `(1028, 163, 28x28)` | `(1028, 163, 28x28)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Status: Active Projects Col** | `(1186, 161, 88x32)` | `(1183, 164, 112x26)` | 3px | 3px | 24px | 6px | ⚠️ DEVIATION |
| **Status: Due Today Col** | `(1290, 161, 82x32)` | `(1311, 164, 79x26)` | 21px | 3px | 3px | 6px | ⚠️ DEVIATION |
| **AI Announcement Banner** | `(133, 218, 1254x58)` | `(133, 218, 1254x58)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **AI: Plus Icon Box** | `(150, 231, 32x32)` | `(149, 233, 28x28)` | 1px | 2px | 4px | 4px | ⚠️ DEVIATION |
| **AI: Announcement Text** | `(194, 239, 754x16)` | `(189, 239, 683x16)` | 5px | 0px | 71px | 0px | ⚠️ DEVIATION |
| **AI: Explore Button** | `(1159, 233, 86x28)` | `(1155, 233, 89x28)` | 4px | 0px | 3px | 0px | ⚠️ DEVIATION |
| **AI: Open Assistant Button** | `(1253, 233, 117x28)` | `(1251, 234, 120x26)` | 2px | 1px | 3px | 2px | ⚠️ DEVIATION |
| **Summary Tiles Grid** | `(133, 292, 1254x136)` | `(133, 292, 1254x136)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 1: Container** | `(133, 292, 306x66)` | `(133, 292, 306x66)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 1: Icon Box** | `(148, 309, 32x32)` | `(148, 309, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 1: Title/Count** | `(190, 305, 126x16)` | `(190, 311, 149x14)` | 0px | 6px | 23px | 2px | ⚠️ DEVIATION |
| **Tile 1: Caption** | `(190, 329, 126x12)` | `(190, 341, 149x14)` | 0px | 12px | 23px | 2px | ⚠️ DEVIATION |
| **Tile 1: Menu/Arrow** | `(412, 317, 12x16)` | `(410, 318, 14x14)` | 2px | 1px | 2px | 2px | ✅ PASS |
| **Tile 2: Container** | `(449, 292, 306x66)` | `(449, 292, 306x66)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 2: Icon Box** | `(464, 309, 32x32)` | `(464, 309, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 2: Title/Count** | `(506, 308, 54x14)` | `(506, 311, 57x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 2: Caption** | `(506, 328, 69x12)` | `(506, 326, 118x14)` | 0px | 2px | 49px | 2px | ⚠️ DEVIATION |
| **Tile 2: Menu/Arrow** | `(718, 314, 22x22)` | `(718, 314, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 3: Container** | `(765, 292, 306x66)` | `(765, 292, 306x66)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 3: Icon Box** | `(780, 309, 32x32)` | `(780, 309, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 3: Title/Count** | `(822, 308, 38x14)` | `(822, 311, 41x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 3: Caption** | `(822, 328, 55x12)` | `(822, 326, 135x14)` | 0px | 2px | 80px | 2px | ⚠️ DEVIATION |
| **Tile 3: Menu/Arrow** | `(1034, 314, 22x22)` | `(1034, 314, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 4: Container** | `(1081, 292, 306x66)` | `(1081, 292, 306x66)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 4: Icon Box** | `(1096, 309, 32x32)` | `(1096, 309, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 4: Title/Count** | `(1138, 308, 47x14)` | `(1138, 311, 51x14)` | 0px | 3px | 4px | 0px | ⚠️ DEVIATION |
| **Tile 4: Caption** | `(1138, 328, 84x12)` | `(1138, 326, 100x14)` | 0px | 2px | 16px | 2px | ⚠️ DEVIATION |
| **Tile 4: Menu/Arrow** | `(1350, 314, 22x22)` | `(1350, 314, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 5: Container** | `(133, 368, 306x60)` | `(133, 368, 306x60)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 5: Icon Box** | `(148, 382, 32x32)` | `(148, 382, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 5: Title/Count** | `(190, 381, 56x14)` | `(190, 384, 59x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 5: Caption** | `(190, 401, 64x12)` | `(190, 399, 112x14)` | 0px | 2px | 48px | 2px | ⚠️ DEVIATION |
| **Tile 5: Menu/Arrow** | `(402, 387, 22x22)` | `(402, 387, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 6: Container** | `(449, 368, 306x60)` | `(449, 368, 306x60)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 6: Icon Box** | `(464, 382, 32x32)` | `(464, 382, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 6: Title/Count** | `(506, 381, 41x14)` | `(506, 384, 44x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 6: Caption** | `(506, 401, 81x12)` | `(506, 399, 96x14)` | 0px | 2px | 15px | 2px | ⚠️ DEVIATION |
| **Tile 6: Menu/Arrow** | `(718, 387, 22x22)` | `(718, 387, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 7: Container** | `(765, 368, 306x60)` | `(765, 368, 306x60)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 7: Icon Box** | `(780, 382, 32x32)` | `(780, 382, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 7: Title/Count** | `(822, 381, 53x14)` | `(822, 384, 56x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 7: Caption** | `(822, 401, 69x12)` | `(822, 399, 106x14)` | 0px | 2px | 37px | 2px | ⚠️ DEVIATION |
| **Tile 7: Menu/Arrow** | `(1034, 387, 22x22)` | `(1034, 387, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 8: Container** | `(1081, 368, 306x60)` | `(1081, 368, 306x60)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 8: Icon Box** | `(1096, 382, 32x32)` | `(1096, 382, 32x32)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Tile 8: Title/Count** | `(1138, 381, 52x14)` | `(1138, 384, 55x14)` | 0px | 3px | 3px | 0px | ⚠️ DEVIATION |
| **Tile 8: Caption** | `(1138, 401, 88x12)` | `(1138, 399, 143x14)` | 0px | 2px | 55px | 2px | ⚠️ DEVIATION |
| **Tile 8: Menu/Arrow** | `(1350, 387, 22x22)` | `(1350, 387, 22x22)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Board Action Bar** | `(133, 444, 1254x42)` | `(133, 444, 1254x42)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Toolbar: View Switcher** | `(133, 448, 359x38)` | `(133, 448, 358x34)` | 0px | 0px | 1px | 4px | ✅ PASS |
| **Toolbar: Board Tab** | `(138, 453, 84x28)` | `(137, 452, 82x26)` | 1px | 1px | 2px | 2px | ✅ PASS |
| **Toolbar: Timeline Tab** | `(222, 453, 96x28)` | `(221, 452, 95x26)` | 1px | 1px | 1px | 2px | ✅ PASS |
| **Toolbar: List Tab** | `(318, 453, 68x28)` | `(318, 452, 68x26)` | 0px | 1px | 0px | 2px | ✅ PASS |
| **Toolbar: Calendar Tab** | `(386, 453, 101x28)` | `(388, 452, 98x26)` | 2px | 1px | 3px | 2px | ⚠️ DEVIATION |
| **Toolbar: Filters Button** | `(1003, 452, 81x30)` | `(996, 451, 86x28)` | 7px | 1px | 5px | 2px | ⚠️ DEVIATION |
| **Toolbar: Ask AI Button** | `(1094, 451, 146x32)` | `(1090, 452, 156x26)` | 4px | 1px | 10px | 6px | ⚠️ DEVIATION |
| **Toolbar: Create Project Button** | `(1250, 451, 137x32)` | `(1254, 452, 133x26)` | 4px | 1px | 4px | 6px | ⚠️ DEVIATION |
| **Kanban Container** | `(133, 502, 1254x393)` | `(133, 502, 1254x426)` | 0px | 0px | 0px | 33px | ⚠️ DEVIATION |
| **Column: Planned** | `(133, 502, 303x393)` | `(133, 502, 303x408)` | 0px | 0px | 0px | 15px | ⚠️ DEVIATION |
| **Col Planned: Header Row** | `(144, 513, 281x27)` | `(144, 513, 281x27)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Planned: Status Dot** | `(150, 521, 10x10)` | `(150, 521, 10x10)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Planned: Title Text** | `(168, 518, 45x16)` | `(168, 520, 46x12)` | 0px | 2px | 1px | 4px | ✅ PASS |
| **Col Planned: Count Chip** | `(221, 515, 25x23)` | `(222, 516, 25x21)` | 1px | 1px | 0px | 2px | ✅ PASS |
| **Column: In Production** | `(450, 502, 303x393)` | `(450, 502, 303x408)` | 0px | 0px | 0px | 15px | ⚠️ DEVIATION |
| **Col In Production: Header Row** | `(461, 513, 281x27)` | `(461, 513, 281x27)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col In Production: Status Dot** | `(467, 521, 10x10)` | `(467, 521, 10x10)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col In Production: Title Text** | `(485, 518, 74x16)` | `(485, 520, 74x12)` | 0px | 2px | 0px | 4px | ✅ PASS |
| **Col In Production: Count Chip** | `(567, 515, 25x23)` | `(567, 516, 26x21)` | 0px | 1px | 1px | 2px | ✅ PASS |
| **Column: Under Review** | `(767, 502, 303x393)` | `(767, 502, 303x408)` | 0px | 0px | 0px | 15px | ⚠️ DEVIATION |
| **Col Under Review: Header Row** | `(778, 513, 281x27)` | `(778, 513, 281x27)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Under Review: Status Dot** | `(784, 521, 10x10)` | `(784, 521, 10x10)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Under Review: Title Text** | `(802, 518, 77x16)` | `(802, 520, 76x12)` | 0px | 2px | 1px | 4px | ✅ PASS |
| **Col Under Review: Count Chip** | `(887, 515, 25x23)` | `(886, 516, 25x21)` | 1px | 1px | 0px | 2px | ✅ PASS |
| **Column: Delivered** | `(1084, 502, 303x393)` | `(1084, 502, 303x426)` | 0px | 0px | 0px | 33px | ⚠️ DEVIATION |
| **Col Delivered: Header Row** | `(1095, 513, 281x27)` | `(1095, 513, 281x27)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Delivered: Status Dot** | `(1101, 521, 10x10)` | `(1101, 521, 10x10)` | 0px | 0px | 0px | 0px | ✅ PASS |
| **Col Delivered: Title Text** | `(1119, 518, 53x16)` | `(1119, 520, 54x12)` | 0px | 2px | 1px | 4px | ✅ PASS |
| **Col Delivered: Count Chip** | `(1180, 515, 25x23)` | `(1181, 516, 25x21)` | 1px | 1px | 0px | 2px | ✅ PASS |
| **Card: Brand Film Container** | `(144, 551, 281x221)` | `(144, 552, 281x231)` | 0px | 1px | 0px | 10px | ⚠️ DEVIATION |
| **Card Brand Film: Priority Chip** | `(161, 568, 59x21)` | `(161, 569, 56x22)` | 0px | 1px | 3px | 1px | ⚠️ DEVIATION |
| **Card Brand Film: Category Tag** | `(364, 569, 44x19)` | `(360, 569, 48x22)` | 4px | 0px | 4px | 3px | ⚠️ DEVIATION |
| **Card Brand Film: Title** | `(161, 601, 247x18)` | `(161, 603, 247x17)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Brand Film: Subtitle** | `(161, 619, 247x17)` | `(161, 621, 247x18)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Brand Film: Progress Label** | `(161, 647, 63x17)` | `(161, 651, 68x18)` | 0px | 4px | 5px | 1px | ⚠️ DEVIATION |
| **Card Brand Film: Percent Text** | `(358, 647, 50x17)` | `(357, 651, 51x18)` | 1px | 4px | 1px | 1px | ⚠️ DEVIATION |
| **Card Brand Film: Progress Track** | `(161, 670, 247x6)` | `(161, 675, 247x6)` | 0px | 5px | 0px | 0px | ⚠️ DEVIATION |
| **Card Brand Film: Due Pill** | `(161, 690, 128x25)` | `(161, 693, 143x28)` | 0px | 3px | 15px | 3px | ⚠️ DEVIATION |
| **Card Brand Film: Avatars** | `(161, 736, 48x20)` | `(161, 737, 76x28)` | 0px | 1px | 28px | 8px | ⚠️ DEVIATION |
| **Card Brand Film: Counts** | `(357, 737, 51x17)` | `(354, 742, 54x18)` | 3px | 5px | 3px | 1px | ⚠️ DEVIATION |
| **Card: Client Campaign Container** | `(144, 785, 281x99)` | `(144, 794, 281x105)` | 0px | 9px | 0px | 6px | ⚠️ DEVIATION |
| **Card Client Campaign: Priority Chip** | `(161, 802, 79x21)` | `(161, 811, 78x22)` | 0px | 9px | 1px | 1px | ⚠️ DEVIATION |
| **Card Client Campaign: Category Tag** | `(369, 802, 39x19)` | `(365, 811, 43x22)` | 4px | 9px | 4px | 3px | ⚠️ DEVIATION |
| **Card Client Campaign: Title** | `(161, 832, 247x18)` | `(161, 845, 247x17)` | 0px | 13px | 0px | 1px | ⚠️ DEVIATION |
| **Card Client Campaign: Subtitle** | `(161, 850, 247x17)` | `(161, 864, 247x18)` | 0px | 14px | 0px | 1px | ⚠️ DEVIATION |
| **Card: Product Launch Container** | `(461, 551, 281x221)` | `(461, 552, 281x231)` | 0px | 1px | 0px | 10px | ⚠️ DEVIATION |
| **Card Product Launch: Priority Chip** | `(478, 568, 61x21)` | `(478, 569, 58x22)` | 0px | 1px | 3px | 1px | ⚠️ DEVIATION |
| **Card Product Launch: Category Tag** | `(665, 569, 60x19)` | `(657, 569, 68x22)` | 8px | 0px | 8px | 3px | ⚠️ DEVIATION |
| **Card Product Launch: Title** | `(478, 601, 247x18)` | `(478, 603, 247x17)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Product Launch: Subtitle** | `(478, 619, 247x17)` | `(478, 621, 247x18)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Product Launch: Progress Label** | `(478, 647, 63x17)` | `(478, 651, 68x18)` | 0px | 4px | 5px | 1px | ⚠️ DEVIATION |
| **Card Product Launch: Percent Text** | `(672, 647, 53x17)` | `(671, 651, 54x18)` | 1px | 4px | 1px | 1px | ⚠️ DEVIATION |
| **Card Product Launch: Progress Track** | `(478, 670, 247x6)` | `(478, 675, 247x6)` | 0px | 5px | 0px | 0px | ⚠️ DEVIATION |
| **Card Product Launch: Due Pill** | `(478, 690, 127x25)` | `(478, 693, 142x28)` | 0px | 3px | 15px | 3px | ⚠️ DEVIATION |
| **Card Product Launch: Avatars** | `(478, 736, 48x20)` | `(478, 737, 76x28)` | 0px | 1px | 28px | 8px | ⚠️ DEVIATION |
| **Card Product Launch: Counts** | `(674, 737, 51x17)` | `(671, 742, 54x18)` | 3px | 5px | 3px | 1px | ⚠️ DEVIATION |
| **Card: Tarbo App Container** | `(461, 785, 281x99)` | `(461, 794, 281x105)` | 0px | 9px | 0px | 6px | ⚠️ DEVIATION |
| **Card Tarbo App: Priority Chip** | `(478, 802, 59x21)` | `(478, 811, 56x22)` | 0px | 9px | 3px | 1px | ⚠️ DEVIATION |
| **Card Tarbo App: Category Tag** | `(676, 802, 49x19)` | `(670, 811, 55x22)` | 6px | 9px | 6px | 3px | ⚠️ DEVIATION |
| **Card Tarbo App: Title** | `(478, 832, 247x18)` | `(478, 845, 247x17)` | 0px | 13px | 0px | 1px | ⚠️ DEVIATION |
| **Card Tarbo App: Subtitle** | `(478, 850, 247x17)` | `(478, 864, 247x18)` | 0px | 14px | 0px | 1px | ⚠️ DEVIATION |
| **Card: Ebay Website Container** | `(778, 551, 281x221)` | `(778, 552, 281x231)` | 0px | 1px | 0px | 10px | ⚠️ DEVIATION |
| **Card Ebay Website: Priority Chip** | `(795, 568, 59x21)` | `(795, 569, 56x22)` | 0px | 1px | 3px | 1px | ⚠️ DEVIATION |
| **Card Ebay Website: Category Tag** | `(961, 569, 81x19)` | `(950, 569, 92x22)` | 11px | 0px | 11px | 3px | ⚠️ DEVIATION |
| **Card Ebay Website: Title** | `(795, 601, 247x18)` | `(795, 603, 247x17)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Ebay Website: Subtitle** | `(795, 619, 247x17)` | `(795, 621, 247x18)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Ebay Website: Progress Label** | `(795, 647, 83x17)` | `(795, 651, 88x18)` | 0px | 4px | 5px | 1px | ⚠️ DEVIATION |
| **Card Ebay Website: Percent Text** | `(981, 647, 61x17)` | `(979, 651, 63x18)` | 2px | 4px | 2px | 1px | ⚠️ DEVIATION |
| **Card Ebay Website: Progress Track** | `(795, 670, 247x6)` | `(795, 675, 247x6)` | 0px | 5px | 0px | 0px | ⚠️ DEVIATION |
| **Card Ebay Website: Due Pill** | `(795, 690, 125x25)` | `(795, 693, 139x28)` | 0px | 3px | 14px | 3px | ⚠️ DEVIATION |
| **Card Ebay Website: Avatars** | `(795, 736, 48x20)` | `(795, 737, 76x28)` | 0px | 1px | 28px | 8px | ⚠️ DEVIATION |
| **Card Ebay Website: Counts** | `(991, 737, 51x17)` | `(988, 742, 54x18)` | 3px | 5px | 3px | 1px | ⚠️ DEVIATION |
| **Card: Fillio Webapp Container** | `(778, 785, 281x99)` | `(778, 794, 281x105)` | 0px | 9px | 0px | 6px | ⚠️ DEVIATION |
| **Card Fillio Webapp: Priority Chip** | `(795, 802, 79x21)` | `(795, 811, 78x22)` | 0px | 9px | 1px | 1px | ⚠️ DEVIATION |
| **Card Fillio Webapp: Category Tag** | `(987, 802, 55x19)` | `(980, 811, 62x22)` | 7px | 9px | 7px | 3px | ⚠️ DEVIATION |
| **Card Fillio Webapp: Title** | `(795, 832, 247x18)` | `(795, 845, 247x17)` | 0px | 13px | 0px | 1px | ⚠️ DEVIATION |
| **Card Fillio Webapp: Subtitle** | `(795, 850, 247x17)` | `(795, 864, 247x18)` | 0px | 14px | 0px | 1px | ⚠️ DEVIATION |
| **Card: Finalize Campaign Container** | `(1095, 551, 281x221)` | `(1095, 552, 281x249)` | 0px | 1px | 0px | 28px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Priority Chip** | `(1112, 568, 79x21)` | `(1112, 569, 78x22)` | 0px | 1px | 1px | 1px | ✅ PASS |
| **Card Finalize Campaign: Category Tag** | `(1309, 569, 50x19)` | `(1303, 569, 56x22)` | 6px | 0px | 6px | 3px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Title** | `(1112, 601, 247x18)` | `(1112, 603, 247x17)` | 0px | 2px | 0px | 1px | ✅ PASS |
| **Card Finalize Campaign: Subtitle** | `(1112, 619, 247x17)` | `(1112, 621, 247x36)` | 0px | 2px | 0px | 19px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Progress Label** | `(1112, 647, 70x17)` | `(1112, 669, 72x18)` | 0px | 22px | 2px | 1px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Percent Text** | `(1340, 647, 19x17)` | `(1339, 669, 20x18)` | 1px | 22px | 1px | 1px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Progress Track** | `(1112, 670, 247x6)` | `(1112, 693, 247x6)` | 0px | 23px | 0px | 0px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Due Pill** | `(1112, 690, 134x25)` | `(1112, 711, 151x28)` | 0px | 21px | 17px | 3px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Avatars** | `(1112, 736, 48x20)` | `(1112, 755, 76x28)` | 0px | 19px | 28px | 8px | ⚠️ DEVIATION |
| **Card Finalize Campaign: Counts** | `(1308, 737, 51x17)` | `(1305, 760, 54x18)` | 3px | 23px | 3px | 1px | ⚠️ DEVIATION |
| **Card: Social Campaign Container** | `(1095, 785, 281x99)` | `(1095, 812, 281x105)` | 0px | 27px | 0px | 6px | ⚠️ DEVIATION |
| **Card Social Campaign: Priority Chip** | `(1112, 802, 61x21)` | `(1112, 829, 58x22)` | 0px | 27px | 3px | 1px | ⚠️ DEVIATION |
| **Card Social Campaign: Category Tag** | `(1288, 802, 71x19)` | `(1278, 829, 81x22)` | 10px | 27px | 10px | 3px | ⚠️ DEVIATION |
| **Card Social Campaign: Title** | `(1112, 832, 247x18)` | `(1112, 863, 247x17)` | 0px | 31px | 0px | 1px | ⚠️ DEVIATION |
| **Card Social Campaign: Subtitle** | `(1112, 850, 247x17)` | `(1112, 882, 247x18)` | 0px | 32px | 0px | 1px | ⚠️ DEVIATION |

## 4. Allowed Deviations & Token Justifications

1. **Minimum Text Size Constraint (GEMINI.md Rule #3):** The reference HTML uses sub-12px micro-text (`text-[10px]`, `text-[9px]`) on chips, counts, dates, and captions. Rebuild rules strictly forbid text $<12\text{px}$. Minor bounding height adjustments ($2-4\text{px}$) guarantee readable $12\text{px}$ text.
2. **Accessible Brand Text on Lime (Rule #4):** White text on lime fills in the reference fails WCAG AA (ratio ~1.4:1). Rebuild uses `var(--ds-color-on-brand)` (`#111111`) for AAA 9.56:1 contrast. For progress labels, `var(--ds-color-brand-text)` (`#4D7C0F` light, `#BEF264` dark) guarantees $>4.5:1$ text contrast.
3. **Avatar Stack Negative Margin Exception (README.md):** Overlapping avatar badges in cards and nav presence stacks use `.ds-avatar-group-item:not(:first-child) { margin-left: -8px; }` with a `2px` surface ring, as documented in the design system README exception.
4. **Tokens-Only Clean Palette:** Zero beige or taupe values remain in DS tokens. All backgrounds and borders are derived from clean neutral slate tokens (`--ds-color-canvas`, `--ds-color-frame`, `--ds-color-surface`, `--ds-color-surface-2`, `--ds-color-hairline`).

## 5. Artifacts Generated

- Desktop Side-by-Side: `docs/design-reference/parity-side-by-side-1440.png`
- Desktop Diff Heatmap: `docs/design-reference/parity-diff-1440.png`
- Multi-viewport captures:
  - `lime-rebuild-1440-dark.png`
  - `lime-rebuild-1024-light.png` & `lime-rebuild-1024-dark.png`
  - `lime-rebuild-768-light.png` & `lime-rebuild-768-dark.png`
  - `lime-rebuild-390-light.png` & `lime-rebuild-390-dark.png`
  - `lime-rebuild-360-light.png` & `lime-rebuild-360-dark.png`
