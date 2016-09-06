---
author: Fabian Schuh
title: PeerPlays Providing Code for Profit Sharing
---

By the end of last week, [PeerPlays Inc](http://peerplays.com) has published [their work](https://github.com/BunkerChainLabsInc/peerplays-profitshare) on **profit sharing** using the Graphene Toolkit.

The [explicit commit](https://github.com/BunkerChainLabsInc/peerplays-profitshare/commit/2aae8a47d8926a7e0f2a9973635eade78fa24eda) has been written by [Blocktrades](http://www.blocktrades.us), can be found on github and may, after proper audit, be included into the BitShares code base aswell (assuming BitShares shareholders approve a network upgrade to include these new features).

<!--more-->

From the code, we can see that the *profit sharing* can be used to pay out dividends to holders of a particular asset. It seems that all profits need to be send to a specifiy account from which profits are shared to their respective shareholders at the given payout intervals.

The code comes with a couple new blockchain operations:

* **asset_dividend_distribution_operation**: Virtual operation that takes asset, company account and amount to distribute among shareholders
* **asset_update_dividend_operation**: Is used to update the assets's dividend-specific options and takes issuer, asset to update and the set of options consisting of *next payout time* and *payout interval*.

The commit also comes with a new command for the `cli_wallet` called `update_dividend_asset`. It seems that it can be used like this:

    update_dividend_asset SYMBOL new_Options true

Profits can be shared at most every *maintenance interval* (1hr).

We are looking forward to see this code audited properly and run in action!
