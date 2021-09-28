---
description: What is a uncle bandit attack?
---

# Uncle bandit attack

Bundles are groups of transactions Flashbots users submit. Those transactions must be included in the order submitted, and either the whole bundle is included, or nothing is. A bundle should never be split up.

Robert Miller found that for a specific bundle, only the "Buy" part of a sandwich bundle submitted had landed on-chain, and right after that Buy someone else had inserted a 7 gas transaction that arbitraged it.

How?

In Ethereum occasionally two blocks are mined at roughly the same time, and only one block can be added to the chain. The other gets "uncled" or orphaned. Anyone can access transactions in an uncled block and some of the transactions may not have ended up in the non-uncled block. In a way some transactions end up in a sort of mempool like state: they are now public as a part of the uncled block and perhaps still valid too.

A Sandwicher's bundle was included in an uncled block. An attacker saw this, grabbed only the Buy part of the Sandwich, threw away the rest, and added an arbitrage after. The attacker then submitted that as a bundle, which was then mined.

Instead of seeing something late in time and rewinding it \(time-bandit attack\), the uncle bandit attack is when an attacker sees something in an uncle and brings it forward. This also shows that attacks extend beyond the mempool and into uncled blocks as well.

{% hint style="info" %}
[https://twitter.com/bertcmiller/status/1382673587715342339?s=20](https://twitter.com/bertcmiller/status/1382673587715342339?s=20)
{% endhint %}

