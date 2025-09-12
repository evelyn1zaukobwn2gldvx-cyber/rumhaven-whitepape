
<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

# 3.2 The Ships of Rumhaven (ShipNFT)

<div class="container">

Ships are the core tool for exploration and wealth accumulation in the Rumhaven Isles. Each vessel is a unique ERC-721 standard NFT, with its ownership and metadata permanently recorded on the Binance Smart Chain and managed by the `ShipNFT.sol` contract. A ship's metadata, including its ID and faction, is dynamically generated on-chain via the `tokenURI` function, forming an immutable "official deed" for each vessel.

Based on the `kindOf` mapping in the `ShipNFT.sol` contract, all ships are divided into two factions:
* **Merchant Ships (Kind 0):** These vessels are the workhorses of the isles' trade routes. Built for sturdiness, they focus on stable and efficient transport. Merchant captains excel at planning, building reliable trade networks to steadily accumulate $RUM wealth.
* **Pirate Ships (Kind 1):** These ships are born for speed and surprise. They navigate dangerous, uncharted waters in search of high-value targets. The life of a pirate captain is filled with uncertainty, but each successful venture can yield immense rewards far exceeding those of merchant trade.

A ship's faction determines not only its backstory but also its fundamental capabilities and route suitability in the core gameplay, "Fortune's Voyage."

</div>

