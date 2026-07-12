# Fondant Queue Craft - Gameplay Fact Card

## App Identity
- **App Name**: Fondant Queue Craft
- **Bundle ID**: com.rosewood.fondantqueuecraft.game
- **Version**: 1.0
- **Platform**: iPhone (Portrait only, iOS 15.0+)
- **Category**: Games / Puzzle

## Core Screen
- Bakery-themed background with a cake preview in the center
- Order card at the top showing open tickets with countdown bars
- Category tabs (Base, Cream, Filling, Decor) above the option grid
- Option grid (3 columns) showing available items for the active category
- Submit Cake button at the bottom
- Pause button in the top-right corner

## Controls
- Tap a category tab to switch between Base / Cream / Filling / Decor
- Tap an option tile to select it; the cake preview updates
- Tap Submit Cake to check the cake against all open tickets
- Tap Pause to open the pause overlay (Resume / Restart / Menu)

## Cake Categories

### Base (6 options)
| Base | Image Asset |
|------|-------------|
| Chocolate | cake_base_chocolate |
| Strawberry | cake_base_strawberry |
| Matcha | cake_base_matcha |
| Cheese | cake_base_cheese |
| Rainbow | cake_base_rainbow |
| Tiramisu | cake_base_tiramisu |

### Cream (6 options)
| Cream | Image Asset |
|-------|-------------|
| White | cream_white |
| Pink | cream_pink |
| Blue | cream_blue |
| Yellow | cream_yellow |
| Green | cream_green |
| Cocoa | cream_cocoa |

### Filling (4 options)
| Filling | Image Asset |
|---------|-------------|
| Vanilla | filling_vanilla |
| Berry | filling_berry |
| Nuts | filling_nuts |
| Custard | filling_custard |

### Decoration (5 options)
| Decoration | Image Asset |
|------------|-------------|
| Candles | deco_candles |
| Flowers | deco_flowers |
| Stars | deco_stars |
| Hearts | deco_hearts |
| Gold | deco_gold |

## Level Progression (50 levels)

### Category Unlock by Level
| Level | Required Categories |
|-------|---------------------|
| 1 | Base only |
| 2 | Cream only |
| 3 | Filling only |
| 4 | Decor only |
| 5 | Base + Cream |
| 6 | Base + Cream + Filling |
| 7+ | All 4 categories |

### Difficulty Scaling
| Level Range | Orders Target | Max Active Orders | Allowed Expired | Order Time Limit | Spawn Interval |
|--------------|---------------|-------------------|-----------------|------------------|----------------|
| 1-10 | 3 | 2 | 3 | 20s → 19s | 7s → 6.35s |
| 11-25 | 4 | 3 | 2 | 18s → 16s | 5.7s → 5.05s |
| 26-30 | 4 | 3 | 2 | 15s | 5.05s → 4.4s |
| 31-40 | 5 | 4 | 1 | 14s → 13s | 4.4s → 3.75s |
| 41-50 | 6 | 4 | 1 | 12s → 10s | 3.75s → 3.2s |

### Formula Details
- **Order Time Limit**: `MAX(10.0, 20.0 - floor((level-1)/5.0))` seconds
- **Spawn Interval**: `MAX(3.2, 7.0 - floor((level-1)/8.0) * 0.65)` seconds
- **Orders Target**: 3 (L1-10), 4 (L11-25), 5 (L26-40... actually L31-40), 6 (L41-50)
  - L1-10: 3, L11-25: 4, L26-40: 5, L41-50: 6
- **Max Active Orders**: 2 (L1-10), 3 (L11-30), 4 (L31-50)
- **Allowed Expired**: 3 (L1-10), 2 (L11-30), 1 (L31-50)

## Order Matching
- Each order specifies one item from each required category
- A submitted cake matches an order if all required categories match
- On match: order is removed, ordersCompleted increments
- On no match: floating text "No matching ticket" appears
- Score: 100 points split equally across required categories

## Data Storage Keys
| Key | Purpose |
|-----|---------|
| FondantQueueCraftProgress | Highest unlocked level (1-50) |
| FondantQueueCraftMusic | Music toggle (default: YES) |
| FondantQueueCraftSound | Sound effects toggle (default: YES) |
| FondantQueueCraftHaptics | Haptics toggle (default: YES) |

## Scenes
1. **COMainMenuScene**: Title, cake preview, Start Order / Levels / Settings buttons, progress display
2. **COLevelSelectScene**: 2-column grid, 10 levels per page, pagination with Prev/Next, LOCKED/OPEN/DONE states
3. **COGameScene**: Main gameplay with order card, cake preview, category tabs, option grid, submit button
4. **COSettingsScene**: Music / Sound Effects / Haptics toggles, version label

## Debug UI Status
- showsFPS = NO
- showsNodeCount = NO
- prefersStatusBarHidden = YES

## Template Residue Check
- No tw_*, game_01_*, Template, or other template residue found.
