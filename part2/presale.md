# 3.1 The Genesis Auction: A Fair Start for All Captains

<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

<div class="container">

To ensure every pioneer begins on equal footing, the foundational assets of the Rumhaven Isles will be distributed entirely through a one-time "Genesis Auction." This auction is executed by the transparent Presale.sol smart contract, with all rules and asset caps locked immutably on-chain.

Fairness Through Randomness
The auction uses a blind-box mechanism. When you mint, you cannot pre-select the specific type of asset you will receive (Merchant Ship vs. Pirate Ship, or Wavecrest Plains vs. Blackrock Heights). Instead, your asset is determined by a verifiable on-chain random process. This process uses block data (like `block.prevrandao` and `blockhash`) as a source of randomness, ensuring that each mint's outcome is fair, unpredictable, and offers an equal opportunity to all participants.

### Genesis Auction Details (Presale.sol)

| Asset Type | Mint Price (Hype) | Total Supply | Contract Function |
| :--- | :--- | :--- | :--- |
| Ship NFT | 0.1 | 1,000 | `mintShipRandom(n)` |
| Land NFT | 0.3 | 500 | `mintLandRandom(n)` |

Participants can mint NFTs by calling the corresponding contract function, where `n` is the desired quantity. The Hype value sent with the transaction must exactly match `quantity * price`. Minting will automatically cease once the supply cap is reached.

</div>

### Presale Tiers & Rules

To add clarity for participants, the Genesis Auction features tiered access windows with different limits and incentives. All rules are enforced by `Presale.sol`.

| Tier | Access Window (UTC) | Price (Hype) | Per-wallet Cap | Allocation | Notes |
| :--- | :--- | :---: | :---: | :---: | :--- |
| Early Bird | TBA (first 24 hours) | 0.08 | 5 NFTs | 10% of supply | Discounted price to reward early supporters |
| Standard | TBA (next 48 hours) | 0.10 | 10 NFTs | 70% of supply | Main public mint window |
| Last Call | TBA (final 24 hours) | 0.12 | 2 NFTs | 20% of leftover | Catch-all window for remaining supply |

**Refund Policy & Anti-bot Measures**
- All mints are final. If a transaction fails due to on-chain reverts, the user's funds remain in their wallet (typical on-chain behavior). The contract includes rate-limits per address and reentrancy guards to mitigate automated front-running.

**Example**: If you participate in the Early Bird tier and mint 3 Ship NFTs at `0.08 Hype` each, your required payment is `0.24 Hype`. The actual Ship type will be assigned at mint time via the on-chain randomness oracle.

</div>
