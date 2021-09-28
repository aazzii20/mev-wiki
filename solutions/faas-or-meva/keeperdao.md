# KeeperDAO

### ![](../../.gitbook/assets/image%20%2810%29.png)KeeperDAO

KeeperDAO is similar to a mining pool for Keepers. By incentivizing a game theory optimal strategy for cooperation among on-chain arbitrageurs, KeeperDAO provides an efficient mechanism for large scale arbitrage and liquidation trades on all DeFi protocols.

#### The Hiding Game <a id="the-hiding-game"></a>

One of the 3 games that has been built. The Hiding Game refers to the cooperation between users and keepers to “hide” MEV by wrapping trades/debt in specialised on-chain contracts. These contracts restrict profit extracting opportunities to KeeperDAO itself.

#### Here's the ELI5 <a id="heres-the-eli5"></a>

Users route their trades and loans through KeeperDAO, which attempts to extract any arbitrage or liquidation profit available. Those profits are returned back to the user in $ROOK tokens, and profits go into a pool controlled by $ROOK holders. By giving KeeperDAO priority access to arbitrage and liquidations, the Hiding Game maximizes the profits available from these opportunities.

#### kCompound \(Phase 2 of the Hiding Game\) <a id="kcompound-phase-2-of-the-hiding-game"></a>

kCompound is the second phase of the Hiding Game. KeeperDAO posts collateral to save your position from being publicly liquidated. Instead, you get privately liquidated. KeeperDAO keeper will then find the best price for your collateral, targeting a 5% profit margin. This profit will then be split between you, the keeper, and the KeeperDAO treasury, meaning that kCompound borrowers will receive a portion of the profits from their own liquidation.

{% hint style="info" %}
**Links:**

* Website: [https://keeperdao.com/\#/](https://keeperdao.com/#/)
* Wiki: [https://github.com/keeperdao/docs/wiki](https://github.com/keeperdao/docs/wiki)
* kCompound: [https://medium.com/keeperdao/introducing-kcompound-a23511c847a0](https://medium.com/keeperdao/introducing-kcompound-a23511c847a0)
{% endhint %}

