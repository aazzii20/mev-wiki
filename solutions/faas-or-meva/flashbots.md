# Flashbots

### ![](../../.gitbook/assets/image%20%2810%29.png)Flashbots <a id="backrunme-by-bloxroute"></a>

Flashbots is a research and development organization formed to mitigate the negative externalities and existential risks posed by MEV. They aim to Democratize MEV Extraction through MEV-Geth, which enables a sealed-bid block space auction mechanism for communicating transaction order preference.

{% hint style="info" %}
**ELI5 Link:**[  
https://twitter.com/\_silto\_/status/1381292907567722498](%20https://twitter.com/_silto_/status/1381292907567722498)
{% endhint %}

Flashbots created an ETH node for miners, that not only watches the mempool like any other node, but also connects to a relayer \(a server\) operated by Flashbots. This MEV-Relay is a kind of parallel channel that directly connects miners to bots that want their transactions included.

The transactions that the bots want to include are sent through the MEV-Relay as bundles containing:

* the transactions to execute
* a tip to the miner, coming as an ETH transfer

These transactions use a 0 gwei gas price, as the payment to the miner is included in the transaction itself as the tip.

Since these transactions are sent through a parallel private relay, it reduces the mempool bidding war, failed transactions bloating the blockchain, and overall gas cost for users.

{% hint style="info" %}
**Links:**

* GitHub: [https://github.com/flashbots](https://github.com/flashbots)
* Research: [https://github.com/flashbots/mev-research](https://github.com/flashbots/mev-research)
* Monthly Meetings: [https://github.com/flashbots/pm](https://github.com/flashbots/pm)
* API: [https://blocks.flashbots.net/](https://blocks.flashbots.net/)
* Discord: [https://discord.gg/7hvTycdNcK](https://discord.gg/7hvTycdNcK)
* Medium: [https://medium.com/flashbots](https://medium.com/flashbots)
* [https://medium.com/flashbots/frontrunning-the-mev-crisis-40629a613752](https://medium.com/flashbots/frontrunning-the-mev-crisis-40629a613752)
* [https://medium.com/flashbots/quantifying-mev-introducing-mev-explore-v0-5ccbee0f6d02](https://medium.com/flashbots/quantifying-mev-introducing-mev-explore-v0-5ccbee0f6d02)
* [https://ethresear.ch/t/flashbots-frontrunning-the-mev-crisis/8251](https://ethresear.ch/t/flashbots-frontrunning-the-mev-crisis/8251)
{% endhint %}

