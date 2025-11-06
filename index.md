---
layout: home
title: Observatory
---

# NextBlock City: Observatory

[The Observatory](https://njump.me/npub1qqpd7c77267rxcxfshczek2da8js40c9srvtaexyfz5hma27r0kq8lduyl) is [NextBlock City's](https://njump.me/npub17vscfmnmshfdw68llhduxtr4h0kkmyhzm4phzs40t3gqsmguz7lsak66ne) timekeeper that turns Bitcoin's blockchain into an astronomical calendar.

## Quick Start

**Date Format**: `AG_{halving}_{season}_{moon}_{position}`

**Example**: `AG_4_2_4_0430` = 4th halving cycle, Summer 🌞, Whale Moon 🐳, 430 blocks into cycle

**Powered by [Telescope](https://github.com/joinnextblock/telescope)** - a TypeScript library for all astronomical calculations.

## Celestial Bodies

- **🌙 Virtual Moon**: 4,032 blocks per cycle (8 phases, 13 named moons)
- **☀️ Virtual Sun**: 210,000 blocks per cycle (4 seasons aligned with Bitcoin halvings)
- **🌊 Virtual Tides**: 42 events per lunar cycle (21 high + 21 low tides)
- **🌑 Eclipses**: Occur at season midpoints when moon crosses sun

## Date Format

Format: `AG_{halving}_{season}_{moon}_{position_in_cycle}`

- **AG/BG**: After/Before Genesis
- **halving**: Halving cycle number (0-based)
- **season**: 1=Spring, 2=Summer, 3=Autumn, 4=Winter
- **moon**: 1-13 (🍊 Orange, 🪶 Bird, 🫂 Friend, 🐳 Whale, 🐂 Bull, 🐻 Bear, 🌽 Corn, ⚡ Lightning, 🥜 Squirrel, 🌊 Wave, 🧊 Ice, 💎 Diamond, ₿ Satoshi's)
- **position**: 0-4031 (4 digits, padded with zeros)

**Hashtag-ready**: Add `#` prefix for social media (e.g., `#AG_4_2_4_0430`)

## Moon Phases

8 phases per cycle (504 blocks each):

| Emoji | Phase | Block Range |
|-------|-------|-------------|
| 🌕 | Full Moon | 0-503 |
| 🌖 | Waning Gibbous | 504-1007 |
| 🌗 | Last Quarter | 1008-1511 |
| 🌘 | Waning Crescent | 1512-2015 |
| 🌑 | New Moon | 2016-2519 |
| 🌒 | Waxing Crescent | 2520-3023 |
| 🌓 | First Quarter | 3024-3527 |
| 🌔 | Waxing Gibbous | 3528-4031 |

**Calculation**: `phase = floor((block_height % 4032) / 504)`

## Solar Seasons

4 seasons per halving cycle (52,500 blocks each):

| Emoji | Season | Block Range |
|-------|--------|-------------|
| 🌱 | Spring | 0-52,499 |
| 🌞 | Summer | 52,500-104,999 |
| 🍂 | Autumn | 105,000-157,499 |
| ❄️ | Winter | 157,500-209,999 |

**Calculation**: `season = floor((block_height % 210000) / 52500)`

## Tides

42 tidal events per lunar cycle (96 blocks per event):
- 21 high tides (even event numbers)
- 21 low tides (odd event numbers)
- Height range: -21 to +21 blocks
- Spring tides: New/Full Moon phases
- Neap tides: Quarter Moon phases

### Tide Phases

Tide height follows a 42-block cycle pattern:

**Tide Height Pattern** (42-block cycle):
- Blocks 0-42: +21 to -21 (42 blocks) 
- Next 42 blocks: -21 to +21 (42 blocks)
- Pattern repeats every 42 blocks

**Tide Phases** (mapped to 42-block height cycle):

| Emoji | Phase | Height Range | Block Range (42-block cycle) |
|-------|-------|--------------|-----------------------------|
| 🌊 | Peak High | +21 | 0 |
| 🌊⬇️ | Falling | +20 to 0 | 1-21 |
| 🏖️⬇️ | Falling | 0 to -20 | 22-41 |
| 🏖️ | Peak Low | -21 | 42 (start of next cycle) |

**Maximum values**: Height reaches +21 at blocks 0, 42, 84, 126... Height reaches -21 at blocks 42, 84, 126, 168...

**Calculation**: `position_in_42 = block_height % 42`, `tide_height = 21 - position_in_42` (for first half, then reverses for second half)

## Atmospheric Conditions

Based on transaction efficiency (tx per full block equivalent):

| Condition | Range |
|-----------|-------|
| ☀️ Clear Skies | 8,000+ |
| 🌤️ Few Clouds | 6,000-8,000 |
| ⛅ Partly Cloudy | 3,000-6,000 |
| ☁️ Overcast | 2,000-3,000 |
| 🌦️ Heavy Clouds | 1,000-2,000 |
| 🌧️ Rain | 500-1,000 |
| ⛈️ Thunderstorms | <500 |

**Calculation**: `efficiency = transaction_count / (block_weight / 4000000)`

## Eclipses

Occur at season midpoints (blocks 26,250, 78,750, 131,250, 183,750):
- **Total Eclipse**: New Moon phase
- **Annular Eclipse**: Full Moon phase  
- **Partial Eclipse**: All other phases

---

*The Observatory is more than just a timekeeper - it's a window into the fundamental rhythms of our digital world.*
