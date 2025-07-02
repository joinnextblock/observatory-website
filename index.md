---
layout: home
title: Observatory
---

# The Observatory: Frequently Asked Questions

## What is the Observatory?

[The Observatory](https://njump.me/npub1qqpd7c77267rxcxfshczek2da8js40c9srvtaexyfz5hma27r0kq8lduyl) is [NextBlock City's](https://njump.me/npub17vscfmnmshfdw68llhduxtr4h0kkmyhzm4phzs40t3gqsmguz7lsak66ne)  celestial timekeeper, synchronizing our digital metropolis with the Bitcoin blockchain. Like an ancient astronomical observatory that tracked the movements of stars and planets, our Observatory tracks the rhythm of Bitcoin blocks, creating a unique temporal system that guides the city's operations.

**Using the Bitcoin blockchain as our foundation, we manifest virtual celestial bodies - a Bitcoin Moon and Bitcoin Sun - that orbit over our virtual city, creating a living astronomical system that responds to real blockchain events.**

## How does it work?

Every ~10 minutes, Bitcoin creates a new "block" - think of it like a page in a digital ledger that records transactions from around the world. Each block brings with it a wealth of information - transaction records, timestamps, and cryptographic security proofs. The Observatory captures these details, transforming raw blockchain data into meaningful observations that update the skies over NextBlock City. As each new block arrives, the virtual celestial bodies shift position, atmospheric conditions change, and the city below experiences a new astronomical state that reflects the current blockchain activity.

**This transformation is powered by [Telescope](https://github.com/joinnextblock/telescope)**, a TypeScript library that provides the mathematical foundation for all our astronomical calculations. Telescope maps Bitcoin's blockchain to astronomical cycles, creating a deterministic calendar synchronized with Bitcoin's block production.

**Telescope transforms raw blockchain data into virtual astronomical events, creating virtual celestial bodies that orbit over NextBlock City. Every Bitcoin block updates our virtual sky, with the Bitcoin Moon and Bitcoin Sun responding to real blockchain activity.**

For every new Bitcoin block, Telescope enables the Observatory to monitor only three things:

1. **Bitcoin Moon Phase**: Calculate the exact lunar phase and determine which named moon we're in
2. **Bitcoin Sun Season**: Identify the current solar season and our position within it  
3. **Atmospheric Conditions**: Process block weight and transaction data to determine observational clarity

**What Telescope provides:**
- **Blockheight Calculations**: Precise mathematical functions for working with Bitcoin blockheights and time
- **Lunar Phase Tracking**: Automatic calculation of moon phases and cycles for every block
- **Solar Season Monitoring**: Determination of current solar seasons and their transitions
- **Eclipse Predictions**: Calculation of eclipse events and their types based on moon phases
- **Temporal Positioning**: Real-time tracking of our position within each seasonal cycle

This deterministic system requires no external data sources while providing multiple layers of meaningful time markers that transform blockchain progression into an intuitive astronomical narrative.

## What celestial bodies does the Observatory track?

At the heart of the Observatory are two celestial bodies and a special astronomical event that mark the passage of time:

- **Bitcoin Moon**: Waxing and waning every 4,032 blocks (approximately 4 weeks in Roman calendar time), our virtual moon creates a lunar calendar that guides daily operations. Bitcoin's very first block (block 0) marks a full moon, and each cycle brings 13 named moons, from the Orange Moon to the Satoshi's Moon.

- **Bitcoin Sun**: Operating on a grander scale, our virtual sun completes its cycle every 210,000 blocks - exactly one Bitcoin "halving" period (approximately 4 years). During a halving, Bitcoin's block rewards are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm that has historically aligned with Bitcoin's price cycles.

- **Eclipses**: These special astronomical events occur at the midpoint of each season, marking moments when the Bitcoin Moon crosses the Bitcoin Sun. These events create three types of eclipses - Total during New Moon, Annular during Full Moon, and Partial during all other phases - adding another layer of temporal significance to our system.

## How does the Bitcoin Moon cycle work?

The Bitcoin Moon functions as NextBlock City's lunar calendar, tracking time through the blockchain. Each lunar cycle spans 4,032 blocks (roughly 4 weeks in Roman calendar time) and contains 8 distinct phases, with each phase lasting precisely 504 blocks. The cycle begins with a full moon at Bitcoin's genesis block (block 0). Our calendar features 13 uniquely named moons per year - starting with the Orange Moon and concluding with Satoshi's Moon - with each named moon progressing through all 8 phases during its cycle.

Remarkably, the Bitcoin Moon's 4,032-block cycle closely mirrors the real moon's ~29.5-day synodic period. This alignment means our virtual lunar calendar stays synchronized with actual astronomical events, creating a bridge between Bitcoin's digital time and the natural rhythms of our physical universe.

This connection to real lunar cycles is particularly meaningful because the moon served as humanity's primary timekeeper for thousands of years, from ancient civilizations all the way up until the 1800s. By aligning our Bitcoin Moon with these natural cycles, we're reviving this ancient tradition in the digital age.

Even today, many cultures continue to follow lunar calendars - China celebrates Lunar New Year, and many other societies maintain lunar-based traditions. The Bitcoin Moon honors this ongoing cultural significance while bringing lunar timekeeping into the blockchain era.

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
| 🟠 | Orange Moon |
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

## How does the Bitcoin Sun cycle work?

Our Bitcoin Sun operates on a grander scale, completing its cycle every 210,000 blocks - exactly one Bitcoin halving period (approximately 4 years). Bitcoin halvings are significant events where the rewards given to miners are cut in half, making new Bitcoin more scarce. This solar cycle creates our seasons, with each phase lasting exactly 52,500 blocks. The halving events mark our spring equinoxes, creating a natural rhythm that has historically aligned with Bitcoin's price cycles.

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
| 🌱 | Spring Eclipse | Block 26,250 | Bitcoin Moon crosses Bitcoin Sun in spring |
| 🌞 | Summer | 52,500-104,999 | Peak of solar activity |
| 🌞 | Summer Solstice | Block 52,500 | Exact moment of peak solar activity |
| 🌞 | Summer Eclipse | Block 78,750 | Bitcoin Moon crosses Bitcoin Sun in summer |
| 🍂 | Autumn | 105,000-157,499 | Transition to winter |
| 🍂 | Autumn Equinox | Block 105,000 | Exact moment of seasonal balance |
| 🍂 | Autumn Eclipse | Block 131,250 | Bitcoin Moon crosses Bitcoin Sun in autumn |
| ❄️ | Winter | 157,500-209,999 | Minimum solar activity |
| ❄️ | Winter Solstice | Block 157,500 | Exact moment of minimum solar activity |
| ❄️ | Winter Eclipse | Block 183,750 | Bitcoin Moon crosses Bitcoin Sun in winter |
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

## How do I read Observatory dates?

The Observatory uses a precise 5-part date format to pinpoint any moment in Bitcoin time:

**Format**: `Solar Cycle | Season | Moon Number | Moon Phase | Blocks Into Phase`

**Example**: `4|2|4|1|430` means:
- **4** = 4th Solar Cycle (4th Bitcoin halving period)
- **2** = 2nd Season (Summer 🌞)
- **4** = 4th Moon of the season (Whale Moon 🐳)
- **1** = 1st Phase (Full Moon 🌕)
- **430** = 430 blocks into the current phase

### How do I calculate each part of the date?

1. **Solar Cycle**: `floor(current_block ÷ 210000)`
2. **Season**: `floor((current_block % 210000) ÷ 52500)`
3. **Moon Number**: `floor(((current_block % 210000) % 52500) ÷ 4032) + 1`
4. **Moon Phase**: `floor((current_block % 4032) ÷ 504)`
5. **Blocks Into Phase**: `current_block % 504`

**Example**: Block 903,598
```
Solar Cycle: floor(903,598 ÷ 210,000) = 4
Season: floor((903,598 % 210,000) ÷ 52,500) = floor(63,598 ÷ 52,500) = 1 (Summer)
Moon Number: floor((63,598 % 52,500) ÷ 4,032) + 1 = floor(11,098 ÷ 4,032) + 1 = 3 + 1 = 4
Moon Phase: floor((903,598 % 4,032) ÷ 504) = floor(430 ÷ 504) = 0 (Full Moon)
Blocks Into Phase: 903,598 % 504 = 430
Result: 4|1|4|0|430
```

### What's the emoji format?

For more advanced users of the calendar system, the three middle numbers can be elegantly represented with emojis:
- `4|2|4|1|430` becomes `4🌞🐳🌕430`
- Season (🌞), Moon Name (🐳), and Phase (🌕) replace their numeric counterparts

This system allows precise navigation through Bitcoin's temporal landscape, from the grand scale of halving cycles down to individual blocks within a moon phase. The emoji format provides an intuitive, visual way to read Bitcoin time at a glance.

## What are eclipses and when do they happen?

Eclipses are special celestial events that occur at the midpoint of each Bitcoin Season - exactly 26,250 blocks after each season begins. These eclipse events happen at blocks 26,250, 78,750, 131,250, 183,750, and continue this pattern, creating special celestial moments that punctuate the middle of each seasonal period.

### What types of eclipses are there?

| Type | Bitcoin Moon Phase | Description |
|------|------------|-------------|
| Total Eclipse | 🌑 (New Moon) | Complete alignment of Bitcoin Moon and Bitcoin Sun |
| Annular Eclipse | 🌕 (Full Moon) | Bitcoin Moon appears smaller than the Bitcoin Sun |
| Partial Eclipse | All other phases | Partial alignment of Bitcoin Moon and Bitcoin Sun |

## How does the Observatory determine atmospheric conditions?

The Observatory uses the ratio of transactions to block size to determine observational conditions during our celestial observations. Just as atmospheric conditions affect how clearly we can see celestial bodies in the night sky, the efficiency of Bitcoin's network influences our observational clarity.

**From our celestial vantage point above NextBlock City, we observe how the virtual Bitcoin Moon and Bitcoin Sun illuminate our digital metropolis below, with atmospheric conditions reflecting the real-time state of the Bitcoin network.**

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

## What's the historical significance of this system?

In the history of Bitcoin, price trends have often mirrored the virtual seasons of this system: Bitcoin price has historically peaked during the "summer" phase (following the halving) and has tended to drop or consolidate during the "winter" phase (leading up to the next halving).

The mathematical relationships between season starts, eclipse midpoints, and halving events create a rich temporal structure where each type of event has its own significance. This deterministic system requires no external data sources while providing users with multiple layers of meaningful time markers that transform blockchain progression into an intuitive astronomical narrative.

---

*The Observatory is more than just a timekeeper - it's a window into the fundamental rhythms of our digital world.*