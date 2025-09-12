# 3.1 The Genesis Auction: A Fair Start for All Captains

<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

<div class="container">

To ensure every pioneer begins on equal footing, the foundational assets of the Rumhaven Isles will be distributed entirely through a one-time "Genesis Auction." This auction is executed by the transparent Presale.sol smart contract, with all rules and asset caps locked immutably on-chain.

Fairness Through Randomness
The auction uses a blind-box mechanism. When you mint, you cannot pre-select the specific type of asset you will receive (Merchant Ship vs. Pirate Ship, or Wavecrest Plains vs. Blackrock Heights). Instead, your asset is determined by a verifiable on-chain random process. This process uses block data (like `block.prevrandao` and `blockhash`) as a source of randomness, ensuring that each mint's outcome is fair, unpredictable, and offers an equal opportunity to all participants.

### Genesis Auction Details (Presale.sol)

| Asset Type | Mint Price (BNB) | Total Supply | Contract Function |
| :--- | :--- | :--- | :--- |
| Ship NFT | 0.1 | 1,000 | `mintShipRandom(n)` |
| Land NFT | 0.3 | 500 | `mintLandRandom(n)` |

Participants can mint NFTs by calling the corresponding contract function, where `n` is the desired quantity. The BNB value sent with the transaction must exactly match `quantity * price`. Minting will automatically cease once the supply cap is reached.

</div>
