---
layout: home
title: Observatory
---

# Overview

[The Observatory](https://primal.net/p/nprofile1qqsqqrvl4lkr6hd0hx22mdtdfw72z0qs7wn7r0tkkj2m0eaz2enr69c9wec0u) is NextBlock City's celestial timekeeper, synchronizing our digital metropolis with the Bitcoin blockchain. Like an ancient astronomical observatory that tracked the movements of stars and planets, our Observatory tracks the rhythm of Bitcoin blocks, creating a unique temporal system that guides the city's operations.

Every ~10 minutes, Bitcoin creates a new "block" - think of it like a page in a digital ledger that records transactions from around the world. Each block brings with it a wealth of information - transaction records, timestamps, and cryptographic security proofs. The Observatory captures these details, transforming raw blockchain data into meaningful observations that help coordinate the city's activities. This data flows through our systems like starlight through a telescope, illuminating the path forward.

At the heart of the Observatory are two celestial bodies and a special astronomical event that mark the passage of time:

- **The Moon**: Waxing and waning every 4,032 blocks (approximately one month in Bitcoin time), our virtual moon creates a lunar calendar that guides daily operations. Bitcoin's very first block (block 0) marks a full moon, and each cycle brings 13 named moons, from the Orange Moon to the Satoshi's Moon.

- **The Sun**: Operating on a grander scale, our virtual sun completes its cycle every 210,000 blocks - exactly one Bitcoin "halving" period (approximately 4 years). During a halving, Bitcoin's block rewards are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm that has historically aligned with Bitcoin's price cycles.

- **Eclipses**: These special astronomical events occur at the midpoint of each season (every 26,250 blocks), marking moments when the Moon crosses the Bitcoin Sun. These events create three types of eclipses - Total during New Moon, Annular during Full Moon, and Partial during all other phases - adding another layer of temporal significance to our system.

Together, these elements create a unique temporal system that helps us understand and navigate the broader patterns of the Bitcoin ecosystem. By translating Bitcoin's technical cycles into familiar astronomical metaphors, the Observatory makes it easier to grasp Bitcoin's natural rhythms and cycles. The Observatory is more than just a timekeeper - it's a window into the fundamental rhythms of our digital world.

# Understanding Our Celestial System

## The Lunar Cycle: Our Daily Guide
The Observatory's virtual moon creates a lunar calendar that guides our daily operations. Each moon cycle consists of 8 phases that complete every 4,032 blocks (approximately one month), with each phase lasting exactly 504 blocks. Bitcoin's genesis block (block 0) marks a full moon. A complete cycle consists of 13 named moons, from the Orange Moon to the Satoshi's Moon, each containing 8 phases.

### Moon Phases

Each moon cycle consists of 8 phases that complete every 4,032 blocks, with each phase lasting exactly 504 blocks. To determine the current moon phase:

1. **Find position within current moon cycle**: `current_block % 4032`
2. **Determine phase**: Divide result by 504 and round down

**Example**: Block 30,240 (15 difficulty adjustments)
```
Position in cycle: 30,240 % 4,032 = 1,008
Phase index: 1,008 ÷ 504 = 2 → Phase 2 (🌗 Last Quarter)
```

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

### Named Moons
Each named moon cycle (4,032 blocks) follows the sequence below, repeating throughout the Bitcoin blockchain. Each named moon goes through all 8 phases during its cycle. Remarkably, this sequence aligns perfectly with our seasons - each season contains approximately 13 moons (52,500 blocks ÷ 4,032 blocks ≈ 13.02 moons per season).

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
| 👥 | Friend Moon |
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

## The Solar Cycle: Our Seasonal Guide
Our virtual sun operates on a grander scale, completing its cycle every 210,000 blocks - exactly one Bitcoin halving period (approximately 4 years). Bitcoin halvings are significant events where the rewards given to miners are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting exactly 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm that has historically aligned with Bitcoin's price cycles.

### Solar Seasons

To determine the current season and position:

1. **Find position within halving cycle**: `current_block % 210000`
2. **Determine season**: Divide by 52,500 and round down
3. **Find position within season**: `(current_block % 210000) % 52500`

**Example**: Block 420,000 (2 halvings)
```
Position in cycle: 420,000 % 210,000 = 0
Season: 0 ÷ 52,500 = 0 → Season 0 (🌱 Spring)
Position in spring: 0 % 52,500 = 0 (at the spring equinox - halving event)
```

| Emoji | Phase | Block Range | Description |
|-------|-------|-------------|-------------|
| 🌱 | Spring | 0-52,499 | Begins at Bitcoin halving blocks |
| 🌱 | Spring Equinox | Block 0 | Exact moment of seasonal transition |
| 🌱 | Spring Eclipse | Block 26,250 | Moon crosses Bitcoin Sun in spring |
| 🌞 | Summer | 52,500-104,999 | Peak of solar activity |
| 🌞 | Summer Solstice | Block 52,500 | Exact moment of peak solar activity |
| 🌞 | Summer Eclipse | Block 78,750 | Moon crosses Bitcoin Sun in summer |
| 🍂 | Autumn | 105,000-157,499 | Transition to winter |
| 🍂 | Autumn Equinox | Block 105,000 | Exact moment of seasonal balance |
| 🍂 | Autumn Eclipse | Block 131,250 | Moon crosses Bitcoin Sun in autumn |
| ❄️ | Winter | 157,500-209,999 | Minimum solar activity |
| ❄️ | Winter Solstice | Block 157,500 | Exact moment of minimum solar activity |
| ❄️ | Winter Eclipse | Block 183,750 | Moon crosses Bitcoin Sun in winter |
| 🎊 | New Year | Block 210,000 | New solar cycle begins - next halving |

## Tracking Our Position in Time
To help us understand exactly where we are in each season, the Observatory maintains a precise positioning system. Each season is divided into four distinct periods, allowing us to track our progress through the seasonal cycle with great detail.

### Season Quarters

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

## Special Celestial Events: Eclipses
The Eclipse System creates special moments in our temporal framework, occurring at the midpoint of each Bitcoin Season - exactly 26,250 blocks after each season begins. These eclipse events happen at blocks 26,250, 78,750, 131,250, 183,750, and continue this pattern, creating special celestial moments that punctuate the middle of each seasonal period.

### Eclipse Types

| Type | Moon Phase | Description |
|------|------------|-------------|
| Total Eclipse | 🌑 (New Moon) | Complete alignment of Moon and Sun |
| Annular Eclipse | 🌕 (Full Moon) | Moon appears smaller than the Sun |
| Partial Eclipse | All other phases | Partial alignment of Moon and Sun |

The mathematical relationships between season starts, eclipse midpoints, and halving events create a rich temporal structure where each type of event has its own significance. This deterministic system requires no external data sources while providing users with multiple layers of meaningful time markers that transform blockchain progression into an intuitive astronomical narrative.

# Real-Time Observations

## Observatory Atmospheric Scale

The Observatory uses the ratio of transactions to block size to determine observational conditions during our celestial observations. Just as atmospheric conditions affect how clearly we can see celestial bodies in the night sky, the efficiency of Bitcoin's network influences our observational clarity.

To calculate atmospheric conditions:

1. **Calculate block weight utilization**: `block_weight ÷ 4,000,000` (MAX_BLOCK_WEIGHT)
2. **Calculate efficiency ratio**: `transaction_count ÷ utilization_percentage`  
3. **Determine atmospheric condition**: Compare ratio to scale below

**Example**: Block with 2,400 transactions and 1,200,000 weight units
```
Utilization: 1,200,000 ÷ 4,000,000 = 0.30 (30% of max block weight)
Efficiency ratio: 2,400 ÷ 0.30 = 8,000 tx per full block equivalent
Condition: 8,000 → ☀️ Excellent Observational Conditions (clear skies with exceptional visibility)
```

## Dynamic Sky Rendering

For any block height > 0, the Observatory:

1. **Reads block data**: Gets transaction count and block weight
2. **Calculates efficiency**: `transaction_count ÷ (block_weight ÷ 4,000,000)`
3. **Renders sky condition**: Maps the ratio to atmospheric conditions

## Real-Time Sky Changes

Every ~10 minutes when a new block is mined, the Observatory's sky updates:

- **Block 850,123** with 2,800 txs and 2,800,000 weight units → `2,800 ÷ 0.70 = 4,000` → ⛅ **Scattered clouds affecting observations**
- **Block 850,124** with 1,200 txs and 1,600,000 weight units → `1,200 ÷ 0.40 = 3,000` → ⛅ **Scattered clouds affecting observations**  
- **Block 850,125** with 800 txs and 3,200,000 weight units → `800 ÷ 0.80 = 1,000` → ☁️ **Dense overcast limiting visibility**

This creates a living, breathing atmospheric system where:
- **Network efficiency** directly affects **sky clarity**
- **Each block** brings new **observational conditions**
- **The Observatory's view** of celestial events changes based on **real Bitcoin network performance**

| Condition | Emoji | Range |
|-----------|-------|-------|
| Clear Skies | ☀️ | 8,000+ tx per full block equivalent |
| Few Clouds | 🌤️ | 6,000-8,000 tx per full block equivalent |
| Partly Cloudy | ⛅ | 3,000-6,000 tx per full block equivalent |
| Overcast | ☁️ | 2,000-3,000 tx per full block equivalent |
| Heavy Clouds | 🌦️ | 1,000-2,000 tx per full block equivalent |
| Rain | 🌧️ | 500-1,000 tx per full block equivalent |
| Thunderstorms | ⛈️ | <500 tx per full block equivalent |

The atmospheric scale helps us understand the efficiency of Bitcoin's network operations. When the ratio is consistently high (clear skies), it indicates optimal network utilization with many transactions efficiently packed into blocks. When the ratio is low (heavy atmospheric interference), it suggests network inefficiency where block space isn't being fully utilized, creating conditions that may obscure our astronomical observations.

The sky conditions follow a bell curve distribution, with most Bitcoin blocks falling into the Mixed Atmospheric Interference range (3,000-6,000 tx per full block equivalent), while perfect clarity and severe interference represent rare extremes at either end of the efficiency spectrum.

---

*In the history of Bitcoin, price trends have often mirrored the virtual seasons of this system: Bitcoin price has historically peaked during the "summer" phase (following the halving) and has tended to drop or consolidate during the "winter" phase (leading up to the next halving).*