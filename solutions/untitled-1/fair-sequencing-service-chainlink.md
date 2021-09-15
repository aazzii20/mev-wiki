---
description: What is FSS?
---

# Fair sequencing service \(Chainlink\)

The idea behind FSS is to have an oracle network order the transactions sent to a particular contract SC, including both user transactions and oracle reports. Oracle nodes ingest transactions and then reach consensus on their ordering, rather than allowing a single leader to dictate it.

FSS is a framework for implementing ordering policies, of which [Aequitas](https://eprint.iacr.org/2020/269.pdf) \(protocol for order-fairness in addition to consistency and liveness\) is one example. It can alternatively support simpler approaches, such as straightforward encryption of transactions, which can then be decrypted in a threshold manner by oracle nodes after ordering. It will also support various policies for inserting oracle reports into a stream of transactions. \(It can even support MEV auctions, if desired.\)

