---
description: How are liquidations exploited?
---

# Liquidations

Back-running strategies also apply to liquidations whereby a transaction sender wishes to be the first to liquidate a loan right after a price oracle update \(which will allow liquidation to be triggered\).

* Fixed spread liquidation used by Compound, Aave, and dYdX allows a liquidator to purchase collateral at a fixed discount when repaying debt.

{% tabs %}
{% tab title="Strategy 1" %}
A detects a liquidation opportunity at block B \(i.e., after the execution of B\). A then issues a liquidation transaction T, which is expected to be mined in the next block B +1. A attempts to destructively front-run other competing liquidators by setting high transaction fees for his liquidation transaction T.
{% endtab %}

{% tab title="Strategy 2" %}
A observes a transaction T, which will create a liquidation opportunity \(e.g., an oracle price update transaction which will render a collateralized debt liquidatable\). A then back-runs T with a liquidation transaction TA to avoid the transaction fee bidding competition.
{% endtab %}
{% endtabs %}

* The auction liquidation allows a liquidator to start an auction that lasts for a pre-configured period \(e.g., 6 hours\). Competing liquidators can engage and bid on the collateral price.

