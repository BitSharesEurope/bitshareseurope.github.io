---
author: Fabian Schuh
title: Peermit 2-Factor-Authentication deployed in the TESTNET!
---

After quite some coding, refacturing, cleanups and more refacturing of
processes as well as with the great progress made by jcalfee1 and svk,
the peermit team is proud to show the first minimum viable product for
Peermit 2-Factor-Authentication in the BitShares testnet.

<!--more-->

This gives you a free way to play around, setting up a secured account
and learning how things will most probably be deployed also on the main
network and hopefully gives me some material and feedback that I can use
to improve the UI and the backend code.

## How It Works:

### Setting Up an Account

1. Create a new account on [the BitShares TEST network](http://testnet.bitshares.eu)
2. Create a new "secured" account
3. Make a backup to secure the owner key that will give ultimate access to your account
4. Unlock your wallet
5. Open the Permissions page of your account and click on the tab "2FA"
6. Provide a mail address that shall be used to contact you on proposals
7. Provide a reference account name (a secondary account that you have control over) that has to also approve any proposals
8. Enable 2 Factor Authentication
9. Finally publish the changes made to your account

Now, you can essentially delete your newly created wallet that contains only one
(secured) account and for which you have a backof of the owner key.

### Transfering Funds out of the Secured Account

1) Open up your regular wallet
2) Open the account page your your secured account
3) Propose a transfer from that account similar to a regular transfer except that you now **flip the "propose" switch**.
4) Afterwards, open the secured account.
5) You should see the proposal below the list of assets. Click on "Approve" and add your approval from the corresponding accounts.

Once you have proposed that transfer, you should receive an (currently
ugly) email with a link to peermit.com. After providing the secret token
to peermit.com, they will approve your transfer. After both approval
transactions have been confirmed, the transfer will be executed.

[Feedback and Discussion](https://bitsharestalk.org/index.php/topic,22193.msg289294.html#msg289294) are welcome!
