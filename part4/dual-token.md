
# 5.1 The Dual-Token Model

<!-- Publication styles -->
<link rel="stylesheet" href="../assets/styles.css">

<div class="container">
The economy of the Rumhaven Isles is driven by a carefully designed dual-token model, where each token plays a unique and complementary role.

</div>

**RUM (The Currency)**
* **Role:** The primary in-game reward and utility token. $RUM is the "currency" of daily economic activity in the isles, generated through the core gameplay of "Fortune's Voyage."
* **Economic Profile:** $RUM is an inflationary token whose supply increases with active player participation. The `RUMToken.sol` contract includes a `mint` function, allowing the game protocol to create new tokens based on player earnings.
* The value of $RUM is derived from its future utility and consumption sinks within the game system (e.g., ship upgrades, repairs, purchasing items).

**LOT (The Equity)**
* **Role:** The community equity and governance credential. $LOT represents a higher-level "stake" in the isles' economy. Holding $LOT is a prerequisite for participating in community treasury events (Staking, Lottery).
* **Economic Profile:** The total supply of $LOT is fixed. More importantly, $LOT benefits from a constant deflationary pressure created by the lottery system—**10% of every ticket's cost is permanently burned**. This mechanism is designed to enhance the scarcity and long-term value of $LOT.

