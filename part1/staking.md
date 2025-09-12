# 2.3 The Merchant's Guild: Stake to Share in the Isles' Prosperity

<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

The Merchant's Guild offers a stable platform for $LOT holders who wish to support the long-term prosperity of the isles to earn $RUM rewards. The system is built on the `Staking.sol` smart contract, ensuring its security and reliability.

**Staking Mechanics**
* **Process:** Users call the `deposit` function to stake their $LOT tokens in the contract. In return, they share in the profits from the $RUM reward pool.
<div class="container">
* **Principal Lock:** As defined by the `LOCK_SECS` constant, all newly deposited $LOT principal is subject to a mandatory **7-day lock-up period**. This design encourages long-term staking, maintains the stability of the staking pool, and prevents short-term speculation from disrupting the ecosystem.

**Campaign-Based Reward System**
$RUM rewards are not distributed through infinite inflation. Instead, they are allocated through time-limited **"Reward Campaigns."** The project team initiates a campaign by calling the `startCampaign` function, injecting a specific amount of $RUM and a set duration into the contract.

This model makes the release of $RUM both controllable and strategic. It avoids the runaway inflation problems seen in many projects with infinite staking rewards. The team can launch new campaigns at key moments—such as version updates or community milestones—to incentivize the community, guide liquidity, and precisely reward long-term supporters. This is a mature design that demonstrates fiscal responsibility.

**The Founder's Bounty**
The first staking reward campaign, "The Founder's Bounty," is now live.

<div class="callout">
**The Founder's Bounty**
The first staking reward campaign, "The Founder's Bounty," is now live.

| Parameter | Value |
| :--- | :--- |
| Staking Token | <span class="token-lot">$LOT</span> |
| Reward Token | <span class="token-rum">$RUM</span> |
| Principal Lock-up | 7 Days |
| First Campaign Pool | <span class="token-rum">100,000 $RUM</span> |
| First Campaign Duration | 7 Days |

During this campaign, a total of **<span class="token-rum">100,000 $RUM</span>** will be distributed linearly and fairly, second by second, to all users staking <span class="token-lot">$LOT</span>. Your share of the rewards is directly proportional to your share of the total staking pool.
</div>

### Staking Reward Schedule & Examples

To help stakers estimate potential returns, the Merchant's Guild exposes clearly defined reward campaigns. Each campaign specifies the total $RUM pool and duration. The contract distributes rewards pro rata to stakers' share of the total pool.

| Campaign Name | Total Pool ($RUM) | Duration | Estimated APR (example) | Notes |
| :--- | :---: | :---: | :---: | :--- |
| Founder's Bounty | 100,000 | 7 days | 45% (approx) | High initial APR to bootstrap staking participation |
| Season One | 250,000 | 30 days | 18% (approx) | Moderated emission for sustainable rewards |
| Long-Term Reserve | 1,000,000 | 365 days | 5% (approx) | Slow drip to support long-term engagement |

**APR Calculation Example**: APR estimates are illustrative and depend on the total amount of $LOT staked. If 10,000 $LOT are staked during Founder's Bounty (100,000 $RUM pool over 7 days), a user staking 100 $LOT would receive approximately (100 / 10,000) * 100,000 = 1,000 $RUM over the campaign — which annualized gives an estimated APR.

</div>

