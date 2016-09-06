---
author: Fabian Schuh
title: How to run YOUR Crowdsale in BitShares
---

As we have seen from the [Ethereum/MakerDAO Team](http://makerdao.com)
([MakerDao Exchange](https://x.makerdao.com/?r=xeroc),
[Howto](https://forum.makerdao.com/t/trading-mkr-on-bitshares-a-how-to-guide/440))
making an asset tradable brings confidence to investors and proofs
seriousness to the public.

Of course, making an asset tradable requires an exchange to list an
asset and a save way to manage the asset. We distinguish two cases:

* the crowdsale has not yet taken place
* the crowdsale that already took place

<!--more-->

In the first case the organizers want to collect money for an I owe you
(IOU). This IOU could be listed on a centralized exchange which collects
the money in exchange for tokens of an asset. However, there are several
disadvantages in this approach:

* the asset can only be traded in few markets
* the centralized exchange has the sole responsibility to handout the
  tokens properly and cannot be audited easily

In the second case, investors usually already hold an from the crowdsale
organizers which may be untradable and thus cannot liquidate until the
organizers have the IOU listed on an exchange and distributed the tokens
to the investors.

Fortunately, there now is the BitShares Decentralized Exchange (DEX)
that solves these issues. Let's discuss both use-cases briefly.

## New Crowdsale

In the case an organizer has not yet started a crowdsale and has no
investors, starting a new crowdsale in the BitShares DEX is a matter of
minutes. It works like this:

1. [Create your User-Issued Asset](http://docs.bitshares.eu/bitshares/tutorials/uia-create-gui.html)
2. [Issue Shares of your asset](http://docs.bitshares.eu/bitshares/tutorials/uia-create-gui.html#issuing-shares)
3. [Put a sell order in any market at any price](http://docs.bitshares.eu/bitshares/tutorials/dex-trading.html)

This comes with several advantages over centralized exchanges:

* The issuer of the asset has the control over the asset (no one else!)
* You can pick the markets you want your tokens sold in yourself (e.g. `TOKEN:BTC`, `TOKEN:USD`)
* Your investors can start making any other market (e.g.`TOKEN:GOLD`)
* You pay a one-time fee to create the asset (reserve the symbol)
* You have full control over market fees (starting at 0.000%)

However, there is also a disadvantage namely, that your investors need
to pay a flat fee for creating orders in the DEX (currently
$0.0003-0.001 with a 90% refund on canceled unfilled orders)

## Existing Crowdsale

If you already have had your crowdsale and want to make your IOU liquid
so that new investors can join and a price discovery takes place, you
can still use the BitShares DEX. However, since your already have
distributed your tokens (using a spreadsheet or a sheet of paper), you
need to also handout the corresponding amount of tokens to your
investors after you have created your asset.

The overall process compares to the one above with slight changes:

1. [Create your User-Issued Asset](http://docs.bitshares.eu/bitshares/tutorials/uia-create-gui.html)
2. [Issue Shares of your asset](http://docs.bitshares.eu/bitshares/tutorials/uia-create-gui.html#issuing-shares)
3. Handout the corresponding amount shares to your investors
4. [Let the investors make the markets](http://docs.bitshares.eu/bitshares/tutorials/dex-trading.html)

The task of handing out shares to investors is done by what we call
*gateway* and depends on the way you log the amount of shares of
investors. The procedure goes as follows:

1. An investors tells the crowdsale organizers that he would like to
   have `x IOU` in his BitShares account. The investors either
   * sends an untradable, but liquid asset to the organizers (e.g. on Ethereum) or
   * gets deducted the corresponding amount from a non-blockchain
     database (e.g. the crowdsale spreadsheet)
2. After reception of `x IOU` by the organizers transfer (or issue) `x
   IOU` into the BitShares account of the investor.

From that time on, the investor can trade these tokens in the DEX (e.g.
against OPEN.BTC, an IOU backed by 100% BTC redeemable via
[OpenLedger](https://bitshares.openledger.info/?r=xeroc))

Assuming you have a blockchain to track your investors IOU or an asset
on Ethereum, counterparty, or Omni, you may want to approach businesses
that focus on the gateway aspect and deal with exchanging
**outside-BitShares**-IOUs into **inside-BitShares**-IOUs to have them
tradable in the DEX. This is a list of companies that are currently
available or under development:

* [MetaExchange](http://metaexchange.info)
* [BlockTrades](http://blocktrades.us)
* [OPEN.* by OpenLedger](http://Openledger.info)
* [Shapeshift](http://shapeshift.io)

## BitShares Fees

Fees in BitShares depend on the actual operation and in the case of
creating an asset (i.e. reserving a symbol name in a unique global name
space), the fee depends on the **number of characters of the symbol**.
You can find the current fee schedule on
[Cryptofresh](http://cryptofresh.com/fees?asset=USD) or in the Block
Explorer of the BitShares Wallet.

Note that in the case you want to register a premium short symbol, you
might want to consider upgrading your account to a lifetime member first
(at a fee) as you can then get back 40% of the asset registration fee.
