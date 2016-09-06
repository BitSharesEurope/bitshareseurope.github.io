---
author: Fabian Schuh
title: Decentralized Exchange Union
---

In crypto currencies, one of the many holy grails is connecting several blockchains together to allow cross-blockchain transactions also referred to as 2-way peg, or side chains. The still unresolved technical difficulties with a sidechains are a result of the very nature of limiting access to Bitcoins by one or several private keys. BitShares acknowledges these limitations and proposes to reimplement an exchange union by means of a multi-signature scheme to achieve a 1:1 exchange of tokens of the secondary chain into IOUs on the secondary chain that are provably backed 100% and secured by many.

<!--more-->

## Overview

In the fiat world today, a national central bank backed by its government and issues new shares of a respective fiat currency. These are then lend to other (potentially commercial) banks that might act in a more regionally limited area. A simple example is the European Central Bank that is the sole creator of new Euro (€) and lends these to national banks, which then lend them to private banks. In this case the central bank has the trust of multiple involved countries and is thus not controlled by a single entity but by a consortium consisting of many, e.g. financial advisors, ministers and experts, which then collectively make decisions. But in the end, all the people have the faith that the currency that they are using, that has been issued by a central bank, can be used to redeem a predictable value and thus serves as an I owe you (IOU). Since it has a face value, that is recognized and accepted by many, these tokens can be used between people for trade and exchange, knowing that it is backed eventually.

This whole concept can easily be brought to modern Bitcoin 3.0 blockchain technologies such as BitShares by means of a cryptographically secured accounts which are controlled not by a single entity but by many entities. In order to access these multi-signature accounts many set of well-defined (but flexible) entities need to agree on any action that is been taken.

Giving that group access to accounts on different blockchain, allows them to serve the same purpose as a central bank with the major difference, that they can back their IOUs on one blockchain, by their savings in another blockchain. This allows public verification and audits as long as supply of IOUs on one blockchain and available reserves on another blockchain.

## Governance

With the fact that BitShares distinguishes between Owner and Active permissions, we can reimplemented a board of director (owner) whose members collectively decide over the board of finance (active) whose members collectively agree on spending and the issuance of new shares for the backed IOUs. The collective control for both permissions can be split with uniform or non-uniform weights among dozens of members and even hierarchical structure of the traditional banking systems could be replicated flexibly.

For the secondary chain (e.g. Bitcoin), this kind of flexibility may not not available. In Bitcoin, for instance, the collective is implemented by means of a simple M-of-N multi-signature address with uniform weights among members. To require 50%+1 consensus for spending rights, e.g. 6-of-10, or 8-of-15, any arbitrary set of M people would be sufficient. Another limitation in Bitcoin’s multi-signature schemes allows us to choose M no bigger than 15 which limits the size of the boards (for the Bitcoin side) as follows:

At most 15 public keys can sign a multi-signature transaction in Bitcoin while many public keys could be available for these transactions. If we distinguish two distinct boards (directors and finance), both boards needs to maintain spending powers over the multi-signature-secured bitcoin address such that no single point of failure exists. Thus, we need to put 15 valid keys from the board of directors and 15 more keys from the board of finance. Both can spend from the multisignature-secured address.

On the BitShares side, there is no such limitation and almost arbitrary complex, even hierarchical authority structures could be implemented to control issuance of new shares.

## A decentralized BTC IOU

The idea is to have a decentralized BTC token that is fully collateralized with real Bitcoin (on the Bitcoin blockchain), locked away in a multi-signature-secured public “cold-storage”. Thus, for every BTC in that address, a BTC IOU could be issued by the multi-signature-secured board of finance. The actual supply can be verified by anybody since both “supplies” are public.

These BTC IOUs can then be forwarded to private banks, e.g. centralized exchanges, that can hand out these tokens to their customers for every BTC deposited. Of course, these IOUs can not just be lend to the private institutes since they need to be backed by real BTC. Instead, these BTC IOUs are sold at a 1:1 (or close to) rate versus real BTC from these centralized exchanges.

Each bank would be asked to provide a reference BTC address and BTS account which will be used to identify the partner in both networks and exchange tokens, e.g. BTC sent to the multi-signature-secured cold storage address from that BTC address identify the centralized exchange and the corresponding IOUs can be send to the BTS account, accordingly, and vise versa.

This way we achieve a stable 2-way peg between the BTC IOU and real BTC, while centralized exchanges keep their customers and business model. Another advantage of course would be that there is only a single BTC IOU to trade against instead of every exchange having their own.

Centralized exchanges would be asked to initially send real BTC into the multi-signature-secured coldstorage address to be provided with the corresponding liquidity in BTC IOUs.

What makes this idea a decentralized central bank is the fact that anybody could register as an exchange partner by providing a BTC address/BTS account exchange pair. Furthermore, this idea and the according software need to be provided open source so that the whole concept could not only be applied to BTC, but also to any other crypto currency with their own board of director.

### Bitcoin Multi-Signature Specifications

Given a set of N members in the board of finance, we propose to create a P2SH multi-signature address (BIP16) with type

    OP_HASH160 <Hash160(redeemScript)> OP_EQUAL

Funds from that address can be redeemed by the redeemScript

    N <ordered-pub-keys> M OP_CHECKMULTISIG

With `N` and `M` defining the size and required signatures for this multisignature scheme and the ordered pub keys being alphabetically sorted and in their compressed format. Limitations in the standardness of transactions require us to limit ourselves to up to 15 public keys.

## Deposit Procedure

Customers deposit BTC at any centralized exchange they prefer that is part of this decentralized central banking network. They provide you with a Bitcoin address to send Bitcoins to and they will credit you with BTC IOUs out of their hot wallet.
If you deposit more than what is available in the exchanges hot wallet, you might need to be a little more patient. However, due to the need to wait for several confirmations (6) for larger deposits, the time it takes for these confirmations should be enough for them to forward them (after 3 confirmation) to their reference Bitcoin address and send them to the multi-signature-secured (after another 2 confirmations) cold storage address to get credited the BTC IOUs immediately. These can then be forwarded to the BTS account name provided by the customers.

## Withdrawal Procedure

For withdrawals into real BTC, a customer sends their BTC IOUs to the exchange partner and provides a bitcoin address in the memo to get credited out of the hot wallet of the exchange. If the funds of the hot wallet are not sufficient for payout, the exchange may need to forward the BTC-IOUs to the decentralized central bank account (via its reference account) to be credited real BTC into the reference address. Forwarding the corresponding amount of real BTC to the user thus may take up to two confirmation times.

## Advantages

* BTC IOUs are fungible and can be exchange into real BTC at any partner bank
* BTC IOUs are backed 100% from funds in the multi-signature-secured addresses
* liquidity is no longer scattered among several BTC IOUs
anyone could be a partner bank for himself
* the concept can be applied for any currency (not just crypto currencies) and enable local community currencies

## Disadvantages

multi-signature-secured “coldstorage” can’t be cold to be reactive (possibe solution: cascade of several cold storage addresses)
Replacing members of the board of finance (active authority) requires to move to a new cold storage address on every external blockchain (e.g. Bitcoin)

## References

* [http://www.truthcoin.info/blog/drivechain/](http://www.truthcoin.info/blog/drivechain/)
* [http://bitcoin.stackexchange.com/a/28092](http://bitcoin.stackexchange.com/a/28092 )
* [https://github.com/bitcoin/bips/blob/master/bip-0016.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0016.mediawiki)
* [https://bitcoin.org/en/developer-examples#p2sh-multisig](https://bitcoin.org/en/developer-examples#p2sh-multisig)
