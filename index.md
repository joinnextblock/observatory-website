---
layout: home
title: Observatory
---

# NextBlock City: Observatory F.A.Q.

## What is the Observatory?

[The Observatory](https://njump.me/npub1qqpd7c77267rxcxfshczek2da8js40c9srvtaexyfz5hma27r0kq8lduyl) is [NextBlock City's](https://njump.me/npub17vscfmnmshfdw68llhduxtr4h0kkmyhzm4phzs40t3gqsmguz7lsak66ne) timekeeper that turns Bitcoin's blockchain into an astronomical calendar. 

Bitcoin creates a new "block" roughly every 10 minutes - like pages in a digital ledger recording transactions worldwide. The Observatory takes this steady rhythm and transforms it into virtual celestial bodies: a virtual moon that cycles every 4,032 blocks and a virtual sun that completes seasons every 210,000 blocks.

This creates a unique time system that produces timestamps like `AG_4_2_4_0430` - capturing everything from major Bitcoin cycles down to the exact block within a lunar cycle. Instead of arbitrary calendar dates, time flows with Bitcoin's natural rhythms.

## How do I read Observatory dates?

The Observatory uses Telescope's `get_formatted_date()` format: `AG_{halving}_{season}_{moon}_{position_in_cycle}` where:
- **AG** = After Genesis (BG would be Before Genesis)
- **halving** = The halving cycle number (0-based, so 4 = 5th halving cycle)
- **season** = The season number (1-4, where 1=Spring, 2=Summer, 3=Autumn, 4=Winter)
- **moon** = The moon number (1-13, where 1=Orange, 4=Whale, etc.)
- **position_in_cycle** = Position within the lunar cycle (0-4031), always 4 digits padded with zeros

**Example**: `AG_4_2_4_0430` means:
- **AG** = After Genesis (block 0)
- **4** = 4th halving cycle (blocks 630,000-839,999)
- **2** = 2nd Season (Summer 🌞)
- **4** = 4th Moon (Whale Moon 🐳)
- **0430** = 430 blocks into the lunar cycle (position within the current moon cycle)

### What's the emoji format?

You can replace numbers with emojis for readability:
- `AG_4_2_4_0430` can be represented as `AG_4🌞🐳0430` or `AG_4_🌞_🐳_0430`

### What about shorthand formats?

For shorthand, you can use zero-padded positions to reference specific moments:

- `AG_3_1_1_0000` = Start of 3rd halving cycle (halving moment, Spring, Orange Moon)
- `AG_4_2_1_0000` = Start of Summer in 4th halving cycle (Orange Moon at season start)
- `AG_4_2_7_0000` = Start of 7th moon (Lightning Moon) of Summer in 4th cycle
- `AG_4_2_7_0504` = Start of 2nd phase (Waning Gibbous) of 7th moon (504 blocks = 1 phase)

The zero-padded position indicates the beginning moment of the specified period, making it easy to denote significant astronomical transitions.

**Note**: The underscore format is designed for hashtag support in social media. You can add a `#` prefix to make it a hashtag like `#AG_4_2_4_0430`.

## What celestial bodies does the Observatory track?

At the heart of the Observatory are three celestial bodies and a special astronomical event that mark the passage of time:

- **Virtual Moon**: Waxing and waning every 4,032 blocks (approximately 4 weeks in Roman calendar time), our virtual moon creates a lunar calendar that guides daily operations. Bitcoin's very first block (block 0) marks a full moon, and each cycle brings 13 named moons, from the Orange Moon to the Satoshi's Moon.

- **Virtual Sun**: Operating on a grander scale, our virtual sun completes its cycle every 210,000 blocks - exactly one Bitcoin "halving" period (approximately 4 years). During a halving, Bitcoin's block rewards are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm.

- **Virtual Tides**: Synchronized with the lunar cycle, our virtual tides create 42 tidal events per lunar cycle - 21 high tides and 21 low tides - providing a finer temporal resolution that embeds Bitcoin's iconic number 21 into the temporal fabric of the Observatory. Each tidal event spans 96 blocks, creating a natural rhythm of rising and falling tides that complements our lunar and solar systems.

- **Eclipses**: These special astronomical events occur at the midpoint of each season, marking moments when the virtual moon crosses the virtual sun. These events create three types of eclipses - Total during New Moon, Annular during Full Moon, and Partial during all other phases - adding another layer of temporal significance to our system.

## How does the virtual moon cycle work?

The virtual moon functions as NextBlock City's lunar calendar, tracking time through the blockchain. Each lunar cycle spans 4,032 blocks (roughly 4 weeks in Roman calendar time) and contains 8 distinct phases, with each phase lasting precisely 504 blocks. The cycle begins with a full moon at Bitcoin's genesis block (block 0). Our calendar features 13 uniquely named moons per year - starting with the Orange Moon and concluding with Satoshi's Moon - with each named moon progressing through all 8 phases during its cycle.

Remarkably, the virtual moon's 4,032-block cycle closely mirrors the real moon's ~29.5-day synodic period. This alignment means our virtual lunar calendar stays synchronized with actual astronomical events, creating a bridge between Bitcoin's digital time and the natural rhythms of our physical universe.

This connection to real lunar cycles is particularly meaningful because the moon served as humanity's primary timekeeper for thousands of years, from ancient civilizations all the way up until the 1800s. By aligning our Bitcoin Moon with these natural cycles, we're reviving this ancient tradition in the digital age.

Even today, many cultures continue to follow lunar calendars - China celebrates Lunar New Year, and many other societies maintain lunar-based traditions. The virtual moon honors this ongoing cultural significance while bringing lunar timekeeping into the blockchain era.

### How do I calculate the current moon phase?

1. **Find position within current moon cycle**: `current_block % 4032`
2. **Determine phase**: Divide result by 504 and round down

**Example**: Block 30,240 (15 difficulty adjustments)
```
Position in cycle: 30,240 % 4,032 = 1,008
Phase index: 1,008 ÷ 504 = 2 → Phase 2 (🌗 Last Quarter)
```

### What are the moon phases?

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

### What are the named moons?

Each named moon cycle (4,032 blocks) follows the sequence below, repeating throughout the Bitcoin blockchain. Each named moon goes through all 8 phases during its cycle. Remarkably, this sequence aligns perfectly with our seasons - each season contains approximately 13 moons (52,500 blocks ÷ 4,032 blocks ≈ 13.02 moons per season). The 13 named moons create a complete lunar year spanning 52,416 blocks (4,032 blocks × 13 moons), and Telescope tracks your position within this lunar year.

To determine the current named moon:

1. **Find which moon cycle**: `floor(current_block ÷ 4032)`
2. **Find position in 13-moon sequence**: `moon_cycle % 13`

**Example**: Block 100,800 (50 difficulty adjustments)
```
Moon cycle: floor(100,800 ÷ 4,032) = 25
Position in sequence: 25 % 13 = 12 → ₿ Satoshi's Moon
```

| Emoji | Name |
|-------|------|
| 🍊 | Orange Moon |
| 🪶 | Bird Moon |
| 🫂 | Friend Moon |
| 🐳 | Whale Moon |
| 🐂 | Bull Moon |
| 🐻 | Bear Moon |
| 🌽 | Corn Moon |
| ⚡ | Lightning Moon |
| 🥜 | Squirrel Moon |
| 🌊 | Wave Moon |
| 🧊 | Ice Moon |
| 💎 | Diamond Moon |
| ₿ | Satoshi's Moon |

## How does the virtual tide cycle work?

The virtual tide system operates in perfect synchronization with the lunar cycle, creating a finer temporal resolution that complements our lunar and solar systems. Each lunar cycle (4,032 blocks) contains exactly 42 tidal events - 21 high tides and 21 low tides - creating a natural rhythm that embeds Bitcoin's iconic number 21 into the temporal fabric of the Observatory.

The mathematical relationship is elegant: 4,032 blocks ÷ 42 events = 96 blocks per tidal event (~16 hours). Each complete high-to-low-to-high cycle spans 192 blocks (~32 hours), creating a continuous ebb and flow that tracks alongside the moon's phases.

This tidal system creates perfect mathematical alignment where each lunar cycle completes exactly 42 tidal events, with 21 complete high-low pairs. The connection to Bitcoin's number 21 is no coincidence - it's woven into the very structure of our temporal system.

### How do I calculate the current tide?

1. **Find position within current lunar cycle**: `current_block % 4032`
2. **Calculate tidal event number**: `floor(position_in_cycle ÷ 96)` (0-41)
3. **Determine tide type**: Even event numbers = high tide, odd = low tide
4. **Find position within tidal event**: `position_in_cycle % 96` (0-95)

**Example**: Block 30,240 (15 difficulty adjustments)
```
Position in cycle: 30,240 % 4,032 = 1,008
Tidal event number: floor(1,008 ÷ 96) = 10 (even → high tide)
Position in event: 1,008 % 96 = 48
Result: High tide, 48 blocks into the event
```

### What are the tide phases?

Tide phases are determined by your position within the 96-block tidal event. Each phase represents a different stage of the tidal cycle:

| Emoji | Phase | Description | Block Range (within event) |
|-------|-------|-------------|---------------------------|
| 🌊⬆️ | Rising | Tide is rising toward peak | 0-47 (high tide) or 0-47 (low tide) |
| 🌊 | Slack High | Peak of high tide | 44-52 (high tide only) |
| 🌊⬇️ | Falling | Tide is falling from peak | 53-95 (high tide) or 53-95 (low tide) |
| 🏖️⬆️ | Rising | Low tide is rising | 0-47 (low tide only) |
| 🏖️ | Slack Low | Bottom of low tide | 44-52 (low tide only) |
| 🏖️⬇️ | Falling | Low tide is falling | 53-95 (low tide only) |

The slack water window (blocks 44-52) represents the peak or trough of each tidal event, where the tide is at its highest or lowest point before reversing direction.

### What are spring and neap tides?

Spring and neap tides are special tidal conditions that align with specific moon phases:

- **Spring Tides**: Occur during New Moon (🌑) and Full Moon (🌕) phases. These are the highest and lowest tides of the lunar cycle, creating the most dramatic tidal range. Spring tides happen when the gravitational forces of the virtual moon and virtual sun are aligned, creating maximum tidal effect.

- **Neap Tides**: Occur during First Quarter (🌓) and Last Quarter (🌗) moon phases. These are moderate tides with a smaller range between high and low. Neap tides happen when the gravitational forces are at right angles, creating minimum tidal effect.

The alignment between moon phases and tidal intensity creates a natural harmony in our system, where the moon's position directly influences the strength of the tides.

### How do I calculate tide height?

Tide heights use a simple linear mapping that represents block position within each tidal event. The system uses integer values from -21 to +21 blocks:

- **High tides**: Start at +21 blocks at the beginning of the event (block 0) and decrease linearly to 0 blocks at the end (block 95)
- **Low tides**: Start at 0 blocks at the beginning of the event (block 0) and decrease linearly to -21 blocks at the end (block 95)

**Calculation**:
- For high tide: `height = 21 × (1 - blocks_into_event ÷ 96)`
- For low tide: `height = -21 × (blocks_into_event ÷ 96)`

**Example**: Block 30,240 (from previous example)
```
Position in event: 48 blocks
Tide type: High tide (event 10 is even)
Height: 21 × (1 - 48 ÷ 96) = 21 × 0.5 = 10.5 → 10 blocks
Result: High tide at +10 blocks height
```

At the extremes (+21 or -21), the tide is at maximum intensity. This linear mapping provides a deterministic representation of block height in tidal form, creating a simple yet elegant system that requires no external data sources.

## How does the virtual sun cycle work?

Our virtual sun operates on a grander scale, completing its cycle every 210,000 blocks - exactly one Bitcoin halving period (approximately 4 years). Bitcoin halvings are significant events where the rewards given to miners are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting exactly 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm.

### How do I calculate the current season?

1. **Find position within halving cycle**: `current_block % 210000`
2. **Determine season**: Divide by 52,500 and round down
3. **Find position within season**: `(current_block % 210000) % 52500`

**Example**: Block 420,000 (2 halvings)
```
Position in cycle: 420,000 % 210,000 = 0
Season: 0 ÷ 52,500 = 0 → Season 0 (🌱 Spring)
Position in spring: 0 % 52,500 = 0 (at the spring equinox - halving event)
```

### What are the solar seasons?

| Emoji | Phase | Block Range | Description |
|-------|-------|-------------|-------------|
| 🌱 | Spring | 0-52,499 | Begins at Bitcoin halving blocks |
| 🌱 | Spring Equinox | Block 0 | Exact moment of seasonal transition |
| 🌱 | Spring Eclipse | Block 26,250 | Virtual moon crosses virtual sun in spring |
| 🌞 | Summer | 52,500-104,999 | Peak of solar activity |
| 🌞 | Summer Solstice | Block 52,500 | Exact moment of peak solar activity |
| 🌞 | Summer Eclipse | Block 78,750 | Virtual moon crosses virtual sun in summer |
| 🍂 | Autumn | 105,000-157,499 | Transition to winter |
| 🍂 | Autumn Equinox | Block 105,000 | Exact moment of seasonal balance |
| 🍂 | Autumn Eclipse | Block 131,250 | Virtual moon crosses virtual sun in autumn |
| ❄️ | Winter | 157,500-209,999 | Minimum solar activity |
| ❄️ | Winter Solstice | Block 157,500 | Exact moment of minimum solar activity |
| ❄️ | Winter Eclipse | Block 183,750 | Virtual moon crosses virtual sun in winter |
| 🎊 | New Year | Block 210,000 | New solar cycle begins - next halving |

### How do I track my position within a season?

Each season is divided into four distinct periods, allowing us to track our progress through the seasonal cycle with great detail.

To determine which quarter of the season you're in:

1. **Find position within current season**: `(current_block % 210000) % 52500`
2. **Calculate quarter**: Divide by 13,125 and round down

**Example**: Block 433,440 (2 halvings + 860 difficulty adjustments)
```
Position in cycle: 433,440 % 210,000 = 13,440
Season: 13,440 ÷ 52,500 = 0.25 → Season 0 (🌱 Spring)
Position in spring: 13,440
Quarter: 13,440 ÷ 13,125 = 1.02 → Quarter 1 (Second Quarter)
```

| Position in Season |
|-------------------|
| First Quarter (0-13,124 blocks) |
| Second Quarter (13,125-26,249 blocks) |
| Third Quarter (26,250-39,374 blocks) |
| Fourth Quarter (39,375-52,499 blocks) |

## What are eclipses and when do they happen?

Eclipses are special celestial events that occur at the midpoint of each Bitcoin Season - exactly 26,250 blocks after each season begins. These eclipse events happen at blocks 26,250, 78,750, 131,250, 183,750, and continue this pattern, creating special celestial moments that punctuate the middle of each seasonal period.

### What types of eclipses are there?

| Type | Virtual Moon Phase | Description |
|------|------------|-------------|
| Total Eclipse | 🌑 (New Moon) | Complete alignment of virtual moon and virtual sun |
| Annular Eclipse | 🌕 (Full Moon) | Virtual moon appears smaller than the virtual sun |
| Partial Eclipse | All other phases | Partial alignment of virtual moon and virtual sun |

## How does it work?

Every ~10 minutes, Bitcoin creates a new "block" containing transaction records and cryptographic proofs. The Observatory transforms this steady blockchain rhythm into virtual celestial cycles - a virtual moon (4,032 blocks), virtual sun (210,000 blocks), and virtual tides (42 events per lunar cycle) - creating an astronomical calendar synchronized with Bitcoin's natural timing.

**This is powered by [Telescope](https://github.com/joinnextblock/telescope)**, a TypeScript library that provides the mathematical foundation for all astronomical calculations, including lunar phases, solar seasons, tidal cycles, and atmospheric conditions, requiring no external data sources.

Telescope's Delta module also provides additional utilities for working with block heights: the `t()` method calculates differences between block heights, and `get_blockheight_from_date()` estimates block heights from dates based on 10-minute block intervals.

## How does the Observatory determine atmospheric conditions?

The Observatory uses the ratio of transactions to block size to determine observational conditions during our celestial observations. Just as atmospheric conditions affect how clearly we can see celestial bodies in the night sky, the efficiency of Bitcoin's network influences our observational clarity.

**From our celestial vantage point above NextBlock City, we observe how the virtual moon and virtual sun illuminate our digital metropolis below, with atmospheric conditions reflecting the real-time state of the Bitcoin network.**

### How do I calculate atmospheric conditions?

1. **Calculate block weight utilization**: `block_weight ÷ 4,000,000` (MAX_BLOCK_WEIGHT)
2. **Calculate efficiency ratio**: `transaction_count ÷ utilization_percentage`  
3. **Determine atmospheric condition**: Compare ratio to scale below

**Example**: Block with 2,400 transactions and 1,200,000 weight units
```
Utilization: 1,200,000 ÷ 4,000,000 = 0.30 (30% of max block weight)
Efficiency ratio: 2,400 ÷ 0.30 = 8,000 tx per full block equivalent
Condition: 8,000 → ☀️ Excellent Observational Conditions (clear skies with exceptional visibility)
```

### What are the atmospheric conditions?

| Condition | Emoji | Range |
|-----------|-------|-------|
| Clear Skies | ☀️ | 8,000+ tx per full block equivalent |
| Few Clouds | 🌤️ | 6,000-8,000 tx per full block equivalent |
| Partly Cloudy | ⛅ | 3,000-6,000 tx per full block equivalent |
| Overcast | ☁️ | 2,000-3,000 tx per full block equivalent |
| Heavy Clouds | 🌦️ | 1,000-2,000 tx per full block equivalent |
| Rain | 🌧️ | 500-1,000 tx per full block equivalent |
| Thunderstorms | ⛈️ | <500 tx per full block equivalent |

### How often do atmospheric conditions change?

Every ~10 minutes when a new block is mined, the Observatory's sky updates:

- **Block 850,123** with 2,800 txs and 2,800,000 weight units → `2,800 ÷ 0.70 = 4,000` → ⛅ **Scattered clouds affecting observations**
- **Block 850,124** with 1,200 txs and 1,600,000 weight units → `1,200 ÷ 0.40 = 3,000` → ⛅ **Scattered clouds affecting observations**  
- **Block 850,125** with 800 txs and 3,200,000 weight units → `800 ÷ 0.80 = 1,000` → ☁️ **Dense overcast limiting visibility**

This creates a living, breathing atmospheric system where:
- **Network efficiency** directly affects **sky clarity**
- **Each block** brings new **observational conditions**
- **The Observatory's view** of celestial events changes based on **real Bitcoin network performance**

---

*The Observatory is more than just a timekeeper - it's a window into the fundamental rhythms of our digital world.*