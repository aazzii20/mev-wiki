# Optimism

### ![](../../.gitbook/assets/image%20%2810%29.png)Optimism

Optimism are the original proposers of MEVA.

MEV Auction \(MEVA\) is created in which the winner of the auction has the right to reorder submitted transactions and insert their own, as long as they do not delay any specific transaction by more than N blocks.

![MEVA on Ethereum](../../.gitbook/assets/image%20%287%29.png)

#### Implementing the Auction <a id="implementing-the-auction"></a>

The auction is able to extract MEV from miners by separating two functions 1\) Transaction inclusion; and 2\) transaction ordering. In order to implement MEVA roles are defined. **Block producers** determine transaction inclusion, and **Sequencers** determine transaction ordering.

#### Block producers - Transaction Inclusion <a id="block-producers-transaction-inclusion"></a>

Block proposers are most analogous to traditional blockchain miners. Instead of proposing blocks with an ordering, they simply propose a set of transactions to eventually be included before N blocks.

#### Sequencers - Transaction Ordering <a id="sequencers-transaction-ordering"></a>

Sequencers are elected by a smart contract managed auction run by the block producers called the MEVA contract. This auction assigns the right to sequence the last N transactions. If, within a timeout the sequencer has not submitted an ordering which is included by block proposers, a new sequencer is elected.

#### Implementation on Layer 2 <a id="implementation-on-layer-2"></a>

It is possible to enshrine this MEVA contract directly on layer 1 \(L1\) blockchain consensus protocols. However, it is also possible to non-invasively add this mechanism in layer 2 \(L2\) and use it to manage Optimistic Rollup transactio ordering. In L2, L1 miners are repurposed and utilized as block proposers. MEVA contract is implemented and designated a single sequencer at a time.

{% hint style="info" %}
**Links:**

* [https://optimism.io/](https://optimism.io/)
* [https://ethresear.ch/t/mev-auction-auctioning-transaction-ordering-rights-as-a-solution-to-miner-extractable-value/6788](https://ethresear.ch/t/mev-auction-auctioning-transaction-ordering-rights-as-a-solution-to-miner-extractable-value/6788)
* [https://docs.google.com/presentation/d/1RaF1byflrLF3yUjd-5vXDZB1ZIRofVeK3JYVD6NPr30/edit\#slide=id.gc9bdacc472\_0\_96](https://docs.google.com/presentation/d/1RaF1byflrLF3yUjd-5vXDZB1ZIRofVeK3JYVD6NPr30/edit#slide=id.gc9bdacc472_0_96)
{% endhint %}

