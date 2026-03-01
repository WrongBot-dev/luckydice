# 🎲 5 Dice Fortune — Money & Luck Dice Simulator
A single-page, front-end dice game where you bet from your wallet, roll 5 dice, and win prizes based on classic combinations (pair, two pairs, full house, straight, etc.). The game includes simulated wallet top-ups via Credit Card or Bank Transfer, plus a Luck Bonus that increases with higher bets.
---

 Features

- 5-dice rolling game with animated “rolling” state
- Wallet balance with formatted currency display
- Betting system (bet is deducted before the roll)
- Luck Bonus meter that increases based on bet tiers (max +50%)
- Prize combinations with fixed payouts up to $1,000,000,000
- Stats tracking
  - Total Wins
  - Total Losses
  - Biggest Win
- Roll history (stores up to 20 most recent events)
- Simulated top-ups
  - Credit Card modal with card preview + basic validation
  - Bank Transfer modal with bank selection + basic validation
  - Fake processing + success overlays
  
---

 Gameplay

1. Start with a balance of $1,000.00
2. Enter a Bet Amount
3. Click ROLL DICE
4. The bet is deducted immediately, then the dice resolve
5. If you hit a winning combination, the prize is added to your balance

If your bet exceeds your balance, you’ll be prompted to top up.

---

 Luck Bonus System

Luck is not purely random: higher bets increase the chance that future dice reuse existing values (biasing toward pairs/sets), and at high tiers there’s a small chance to force a straight.

 Luck tiers (as implemented)

| Bet Amount | Luck Bonus |
| $1 – $99 | 2% |
| $100 – $999 | 5% |
| $1,000 – $9,999 | 10% |
| $10,000 – $99,999 | 20% |
| $100,000 – $499,999 | 35% |
| $500,000+ | 50% (max) |

---

 Prize Table

Winning combinations are evaluated from the 5 dice:

| Combination | Prize |
|---|---:|
| Five of a Kind | $1,000,000,000 |
| Four of a Kind | $50,000,000 |
| Full House (3+2) | $10,000,000 |
| Straight (1-2-3-4-5) | $5,000,000 |
| Straight (2-3-4-5-6) | $5,000,000 |
| Three of a Kind | $500,000 |
| Two Pairs | $50,000 |
| One Pair | $5,000 |
| All Different (not a straight) | $100 |
| Nothing | $0 |

---

 Simulated Payments (Top-Up)

Top-ups are for entertainment only and do not process real payments.

 Credit Card Top-Up
- Quick-select amounts or custom amount (up to $1,000,000)
- Basic validation:
  - Card number length (15–16 digits)
  - Name present
  - Expiry present (`MM/YY`)
  - CVV length (3–4)
- Adds funds to balance after a simulated processing delay

 Bank Transfer Top-Up
- Choose a bank, then enter:
  - Account holder name
  - Routing number (9 digits)
  - Account number (min length 4)
- Adds funds to balance after a simulated processing delay

---

## Disclaimer

This project is a simulation intended for entertainment/UI demonstration. It includes “payment” forms and bank/card fields strictly as mock UI; do not use real card or bank information.
