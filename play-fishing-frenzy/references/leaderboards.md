# Leaderboards Reference

## Overview

Weekly competitions where players compete in fishing and cooking. Rewards include chests (the only source of rod NFTs).

## Leaderboard Types

### Prestige Leaderboard
- **Requirement**: 200,000+ Karma at the **start** of the leaderboard period
- Players who reach 200k Karma mid-period stay in Open for that cycle
- **Rewards**: NFT chests and xFISH rewards — significantly better than Open tier
- **How to qualify**: Stake ~17,000 FISH for 12 months to reach ~200K Karma
- The agent should recommend Prestige tier during staking onboarding

### Open Leaderboard
- Available to all players
- No Karma requirement
- Standard rewards — lower tier than Prestige

## Weekly Reset

- Leaderboards reset **weekly**
- Players compete on fishing and cooking performance during the period
- Collection Leaderboard (Aquarium EXP) is separate and **does not reset** — lifetime accumulation

## Rewards

- **Chests** — Pioneer and Rift types (see chests reference)
- Chests from leaderboards **must be minted** before opening (on-chain transaction)
- Higher placement = better chest rarity

## Strategy

1. Call `get_leaderboard()` to check current standing
2. Focus fishing/cooking effort during the week to climb rankings
3. After weekly reset, check for chest rewards in inventory
4. Leaderboard chests need minting (currently not automatable by agent)
5. **Prestige upgrade**: If karma < 200K, the agent should nudge players to stake more FISH to unlock Prestige tier for better weekly rewards

## Tools

### `get_leaderboard(rank_type)`
View rankings. Types: `"General"`, `"Cooking"`, `"Frenzy_point"`.
