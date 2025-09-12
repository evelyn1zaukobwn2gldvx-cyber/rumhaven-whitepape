# 2.2 The Governor's Lottery: A Game of Chance and Deflation

<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

The Governor's Lottery is a periodic, high-reward drawing system driven entirely by the `Lottery.sol` smart contract, designed to offer $LOT holders both entertainment and an opportunity for wealth creation. All rules are locked on-chain, ensuring transparency and immutability.

<div class="container">

**Participation Mechanics**
* **Ticket Purchase:** Players use $LOT tokens to buy tickets. The fixed price, defined by the `LOT_PRICE_PER_TICKET` constant, is **1,000 $LOT** per ticket.
* **Round Structure:** Each lottery round has a hard cap of **100 tickets**, as defined by the `CAP` constant. When the 100th ticket is sold, the round immediately concludes, automatically triggering the prize draw and the start of the next round.

**The Deflation Engine**
The lottery system features a powerful built-in deflationary mechanism that supports the long-term value of the $LOT token.
* **Permanent Burn:** For every ticket purchased, **10% of the cost (100 $LOT)** is automatically sent to a burn address (`0x...dEaD`). This is a hard-coded rule in the contract, ensuring a continuous reduction of the total $LOT supply.
* **Prize Pool Contribution:** The remaining 90% of the cost (900 $LOT) goes into the current round's prize pool.

**Prize Pool Distribution**
Each round's total $LOT prize pool is distributed according to the following fixed ratios:
* **Grand Prize:** **50%** of the pool is awarded to a single grand prize winner.
* **Second Prize:** **20%** of the pool is split evenly among up to 10 second prize winners.
* **Seed Fund:** The remaining **30%** of the pool automatically rolls over into the next round's prize pool, ensuring every round begins with an attractive starting prize.


<div class="callout">
**The Founder's Bounty: Instant $RUM Rewards**
To celebrate the maiden voyage, a special reward pool of **<span class="token-rum">100,000 $RUM</span>** has been deposited into the lottery contract via the `depositRUM` function. This fund is separate from the $LOT prize pool and is used to instantly reward participants during the ticket sale process, governed by specific contract rules:
* **Buyer's Bonus (`RUM_BUYER`):** Every ticket purchase grants a fixed, instant $RUM reward.
* **Milestone Prize (`RUM_MILESTONE`):** Purchasing a ticket at a specific number (e.g., 10th, 20th, 30th, determined by the `MILESTONE_EVERY` parameter) triggers an additional $RUM bonus.
* **Lucky Hit (`RUM_LUCKY`):** Each ticket purchase has a chance, determined by the `LUCKY_BPS` parameter, to trigger a one-time, high-value lucky $RUM reward.

| Parameter | Value |
| :--- | :--- |
| Ticket Cost | 1,000 $LOT |
| Tickets Per Round | 100 |
| $LOT Burn Rate | 10% per ticket |
| Grand Prize | 50% of $LOT Pool |
| Second Prize | 20% of $LOT Pool (split by up to 10 winners) |
| Next Round Seed | 30% of $LOT Pool |
| Founder's Bounty | 100,000 $RUM (for instant rewards) |
</div>

### Lottery Parameters & Mechanics (Detailed)

The lottery contract exposes several tunable parameters and fixed mechanics designed for fairness and anti-exploit protection.

| Field | Solidity Constant | Value | Description |
| :--- | :--- | :---: | :--- |
| `LOT_PRICE_PER_TICKET` | `uint256` | 1,000 $LOT | Cost of one ticket paid in $LOT |
| `CAP` | `uint16` | 100 | Tickets per round; triggers instant draw on sell-out |
| `BURN_BPS` | `uint16` | 1,000 (10%) | Basis points of each ticket burned to `0x...dEaD` |
| `GRAND_PRIZE_BPS` | `uint16` | 5,000 (50%) | Grand prize share of pool |
| `SECOND_PRIZE_BPS` | `uint16` | 2,000 (20%) | Share allocated to secondary winners |
| `SEED_BPS` | `uint16` | 3,000 (30%) | Rollover percentage into next round |
| `RUM_BUYER` | `uint256` | 50 $RUM | Instant reward to buyer per ticket (example) |
| `RUM_MILESTONE` | `uint256` | 500 $RUM | Milestone bonus (every 10th ticket) |
| `LUCKY_BPS` | `uint16` | 100 (1%) | Chance to trigger a lucky hit reward |

**Instant Reward Example**: When a user buys a ticket, the contract attempts to pay `RUM_BUYER` directly from the Founder's Bounty pool. If the pool does not have sufficient funds, the instant reward mechanism gracefully reduces or defers those payments as defined in the contract.

</div>

