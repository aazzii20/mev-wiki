---
description: What is back-running?
---

# Back-running

Back-running occurs when a transaction sender wishes to have their transaction ordered immediately after some unconfirmed "target transaction".

Example: A back-running bot that back-runs new token listings. Bot monitors the Ethereum mempool for new pairs being created on Uniswap. If it finds a new pair the bot places a buy transaction immediately behind the initial liquidity. The bot swoops in and buys as many tokens as possible \(but not all of them as there needs to be an opportunity for others to buy tokens as well\).The bot then waits for the price to go up as other traders buy the token from Uniswap and proceeds to sell back the tokens at a higher price. The key in this strategy is to be the first to buy tokens, but only after the token has been launched[¹](https://amanusk.medium.com/the-fastest-draw-on-the-blockchain-bzrx-example-6bd19fabdbe1).

In order to maximise their changes of being mined immediately after their target, a typical backrunner will send many identical transactions, with gas price identical to that of the target transaction, sometimes from different accounts, in order to increase the chances that one of their transactions is ordered after the target but before any competitor.

{% hint style="info" %}
1. [https://amanusk.medium.com/the-fastest-draw-on-the-blockchain-bzrx-example-6bd19fabdbe1](https://amanusk.medium.com/the-fastest-draw-on-the-blockchain-bzrx-example-6bd19fabdbe1)
{% endhint %}

