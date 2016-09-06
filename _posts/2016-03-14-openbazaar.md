---
author: Fabian Schuh
title: Open Letter to OpenBazaar
---
Dear OpenBazaar community,

I have followed the OpenBazaar development with quite some excitement and am very happy to see such a great idea evolve into a great project with an awesome community. Congratulations for the successful launch in the Bitcoin Testnet!

<!--more-->

Let me tell you, that when I met the OB1 team in Amsterdam I was very, very excited and couldn't wait to see their presentation at the [d10e conference](http://d10e.org). The whole demonstration, not only of the project itself but also of the community and the team made me realize that I had to join the OpenBazaar meetup that took place the day after. We received a full afternoon of demonstrations, technical discussions and talks about almost anything related to decentralized market places and how OpenBazaar can certainly replace well-known inefficient and expensive centralized competitors.

In the days after the conference, I took some days off only to take a closer look into OpenBazaar, the backend, the frontend, the API, community, documentation, etc. Let me tell you this: I am deeply impressed by what you have built there and the whole OpenBazaar community can be proud to have the guys behind OB1!

Then, I recalled Dr. Washington's talk about his ideas of how to improve OpenBazaar in the future and saw him become very excited about how recent developments in blockchain technologies and cryptography could significantly improve OpenBazaar (threshold signatures, decentralized exchanges and prediction markets, on-chain reputation networks, etc.) and I share his excitement.

In contrast to the OB1 team, I never got up the nerve to start such a huge endeavor but instead joined an existing ecosystem around a newly evolving blockchain technology, helped evolve it to something bigger and am still very excited about it: [BitShares](http://BitShares.org). Interestingly, I am not the only one among the BitShares community that is very excited about OpenBazaar and how it can decentralize trading on a global scale ([1](https://bitsharestalk.org/index.php/topic,9651.0.html) [2](https://bitsharestalk.org/index.php/topic,7716.0.html) [3](https://bitsharestalk.org/index.php/topic,21633.0.html) [4](https://bitsharestalk.org/index.php/topic,8180.0.html) [5](https://bitsharestalk.org/index.php/topic,21508.0.html) [6](https://bitsharestalk.org/index.php/topic,6782.0.html) [7](https://bitsharestalk.org/index.php/topic,9554.0.html) [8](https://bitsharestalk.org/index.php/topic,20493.0.html) [9](https://bitsharestalk.org/index.php/topic,15885.0.html)).

Of course, I understand the reasons for integrating OpenBazaar with Bitcoin instead of any other existing blockchain technology and, back when they started, I would not have recommended any differently!

However, now both of our systems have matured to solid foundations, it is my impression that we should found a **partnership** or even better, a **joint venture** to follow our common goals of financial freedom and freedom to trade with no restrictions.

If you have already formed the opinion that BitShares is just another altcoin, please continue reading. You might learn something you didn't know about it yet.

About the BitShares Ecosystem
-----------------------------

Let's start with the obvious: We suck at marketing! Literally. That's why many still think BitShares is an alternative coin or a crypto currency while in fact it is way more than that. However, I don't want to give you a boring introduction of every single feature available with our underlying blockchain technology and instead only pick those that I think might be interesting for OpenBazaar. 

### Distributed Decentralized and Shareholder Governed Blockchain

BitShares is a distributed blockchain technology with a decentralized P2P network. The consensus algorithm for block confirmation allows shareholders to collectively vote for the set of trusted block producers. With this voting mechanism, BitShares can govern itself and is thus autonomous.

### Real-Time Scalable Blockchain Technology

We obviously can't trick you into thinking that our blockchain is capable of doing anything in real-time, but considering that we have a superior consensus mechanism that allows our block producers to agree on timing, we are the only blockchain that can confirm your transactions every 3 seconds -- not just on average. Further, once we have improved our P2P network code, we could even reduce that time and could maybe even go down to 1 second confirmation times, without requiring a hard- or soft-fork!

We have also shown already that we can run our network on 1,800 transactions per second on a globally distributed testnet. We used an alpha release back then and are convinced that the tech can deal with way more than that. In fact, first lab tests have shown we can go up to over 100k transactions per second! That is the kind of scalability we would have hoped to see in Bitcoin, but to be honest, we don't see it coming any time soon.

### Integrated Fiat Support

One of the core problems we see in Bitcoin, when using it for payments and not as a store of value, is that your customers need to deal with the volatility and capital gains. This is not a big problem when using Bitcoin as a store of value but it certainly is a barrier for bigger merchants to enter OpenBazaar. BitShares could help you bring them in by offering stable tokens. In contrast to our competitors that offer a wide variety of stable but centralized crypto currencies, our so called smartcoins are decentralized with software being your counterparty. Every single bitUSD (a smartcoin that is pegged to the U.S. dollar) is backed by at least 190% reservers in a smart contract that implements a contract for difference. With smartcoins your customers could pay for their goods with USD! Or you go one step further and let them offer Gold bullions that can be bought with a decentralized version of digital GOLD? By integrating with BitShares, you can do all of this and transfers will soon be free! 

### Zero/0 Transfer Fees

BitShares will soon offer transfers for free (as in "nada"). We prevent spam by rate-limiting free transactions. The number of free transactions an account can perform depends on the stake it owns. The more stake an account owns the more free transactions are available to it in a given time period. The account of course has an unlimited number of fee based transactions once the free transactions are used up for a given time period.

### Integrated Decentralized Exchange

Has any one of you ever looked into Dr. Washington's gist repository at github? There is great stuff to be found! One of these things is his idea of a [decentralized exchange for crypto currencies](https://gist.github.com/drwasho/aa6ab79e92f2a876073e) and, well, we do have quite some experience in that already. BitShares has been available for more than 2 years and the decentralized exchange has had quite some volume. To be honest with you, the recent upgrade to our new blockchain foundations, and the new APIs, have caused some challenges for our trading partners who will need some more time to implement their market making algorithms. Once everyone is upgraded we will see some more liquidity  again. We are working with them on that.

### Integrated Market place for Stock, securities, bonds, event tickets and ownership tokens

Another idea of the OpenBazaar developers has been to [trade different kinds of assets](https://github.com/drwasho/openbazaar-documentation/blob/master/04%20Marketplaces.md#4-marketplaces) and of course we have most of them available as well: Stock, Securities, and Derivatives. Also, we will probably soon see a [decentralized Bond market](https://gist.github.com/drwasho/2c40b91e169f55988618) integrated into BitShares that offers P2P lending. These tokens can of course also be used as event tickets or for ownership tracking which fits perfectly with the idea of OpenBazaar in my mind.
 
### Already Available Prediction markets

Prediction markets are another nice thing that your developers are already thinking of and which has been implemented in BitShares ready to go today!

### Stealth Transfers

Of course, there is a way to deal with your shops in [private and hide transactions](https://gist.github.com/drwasho/a0225f5455e508095ac2) for instance from your wife :). Not only can you be sure that your transactions cannot be linked to you, but also can you hide the actual amount that you have transfered from every one not involved in your transfer!

### Insurance Networks

Some ideas that I personally like best are the insurance networks proposed [here](https://gist.github.com/drwasho/3670bb1c59e620fffb24), [here](https://gist.github.com/drwasho/9759924342859872851e) and [here](https://gist.github.com/drwasho/352a565475a7f1e6dda0), and I am pleased to let you know that we have had something close in mind as well that we could offer OpenBazzar: [Benefit Societies](https://github.com/bitshares/bsips/blob/master/bsip-0009.md). And if not for the smartcoins, this feature could potentially help OpenBazaar be a killer application for the future internet!

### On-Chain Identity management

Currently, OpenBazaar deals with identities as they are offered by Onename and I really like the idea. One nice feature of BitShares, though, is that it comes with its own identity management system integrated to be used for this case. It even features white-listing and black-listing for establishing a reputation web-of-trust. The idea would be to have your BitShares account integrated into onename as well so that you can leverage these BitShares features from within OpenBazaar.

This can even be used to improve the moderation process as we already have threshold multi-signature schemes deployed that can even be nested for a hierarchical moderation schemes!

### Extensibility due to Network Upgrade capabilities and Turing Completeness

On another note, and we clearly failed to market this feature: BitShares is indeed Turing Complete. The only difference to Ethereum is that new smart contracts need to be integrated in C++ but as a result come with incredible efficiency and speed. So, if you have a feature in mind that is not yet possible, tell us and we can surely make it possible!

### Some thoughts about what this might bring

Let's think about what would become possible by combining BitShares and OpenBazaar.

* Kickstarter-style crowdfunding:
  Every participant could buy into the development of a product by
  simply purchasing a token of that project using OpenBazaar!
* Kickstarter-like P2P-investing:
  If we improve the idea above, the developer of a project could even
  distribute a portion of his profits to those that made the idea
  possible in the beginning! Hence, you don't just get a T-shirt but you
  get a share of future profits!
* Ebay-style acution:
  Did you read about BitShares having a block every 3 seconds? If not,
  please start over at line 1 :). I'll leave the rest as an exercise to
  the reader :D.

TL;DR;
------

You certainly *want* OpenBazaar to integrate with BitShares and leverage our technology!

Contact
-------

Together wit this proposal, we are trying to become more active in the OpenBazaar slack group and many of us will probably be reachable in the *bitshares* channel in your slack group. Alternatively, you are very welcome to reach out to us on our [slack group](http://slack.bitshares.org) or the [bitsharestalk forums](http://bitsharestalk.org).

We are looking forward to a fruitful partnership!

Disclaimer
----------

This writeup represents the opinion of BitSharesEurope!
