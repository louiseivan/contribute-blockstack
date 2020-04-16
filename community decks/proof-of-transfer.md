---
title: Blockstack Proof of Transfer Community Deck
tags: Community Decks, PoX, Mining, Stacking
description: View the slide with "Slide Mode".
---

# 🔄Proof of Transfer: A novel consensus mechanism

This is the community presentation for the recently proposed consensus mechanism, Proof of Transfer.

slide: https://hackmd.io/@kf0897riSlaPvlj6tUW5hA/SkeL7ErD8


---

## Blockstack History

Years of deep distributed systems R&D for a solid foundation
```
• Founded by Princeton Computer Scientists
• 2 scientists with Presidential Career Awards
• 13,000+ research citations among whitepaper authors
• Research published at USENIX ATC, DCCl
• Nominated by Princeton for SIGCOMM dissertation award Board: Mongo DB (IPO), Twilio (IPO), Etsy (IPO)
```

---

![](https://i.imgur.com/1wwO7Zg.png)


---

### From R&D to Production 
$70M+ raised from industry-leading investors.

* 2017 - R&D and dev platform
* 2018 - Launched Stacks v1 blockchain
* 2019 - 360+ apps on the network + SEC-qualified offering
* 2020 - Stacks 2.0 + further decentralization

---

![](https://i.imgur.com/9xaQHiI.png)

---

## PoX - Proof of Transfer Overview

<style>
code.blue {
  color: #337AB7 !important;
}
code.orange {
  color: #F7A004 !important;
}
</style>

- <code class="orange">Bitcoin</code> as Digital Gold and reserve currency.
- Creates New Use Case for Bitcoin
- You only need to go from electricity to PoW currency only once. 
- Can use existing PoW cryptocurrency to secure new blockchains and mint units of new cryptocurrency
- <code class="orange">Proof-of-transfer (PoX)</code> on the base cryptocurrency by miners.
- <code class="orange">Bitcoin is the “king of PoW”</code> and further consolidation might happen.

---

![](https://i.imgur.com/bf9oiLh.png)

---

### PoX Mining
| Name     | Acronym | Miner action to mint new cryptocurrency |
| ----     | ----- | -------- |
| Proof-of-work   | PoW    | Consume electricity and computation to mint units of a new cryptocurrency.|
| Proof-of-stake | PoS    |Dedicate economic stake in a base cryptocurrency to mint units of the same cryptocurrency.|
| Proof-of-burn    | PoB    |Destroy a base cryptocurrency to mint units of new cyrptocurrency|
| Proof-of-transfer    | PoX    |Transfer a base cryptocurrency to mint units of a new cryptocurrency|

---

### Stacking
<style>
code.blue {
  color: #337AB7 !important;
}
code.orange {
  color: #F7A004 !important;
}
</style>

- <code class="blue">Stackers </code> lock their STX and run full-nodes to participate in the consensus algorithm. Earn a payout (roughly) per month for actively participating.
- <code class="blue">STX miners</code> process transactions, Clarity contracts, write new blocks, and mint new STX.
#### Economics
- Stackers earn Bitcoin rewards.
- Combines economic benefits from PoS with security and stability of PoW.

---

### Pre-requisites for participating Stacker
 
- Should control a STX wallet with >=0.02% of unlocked total share of STX or participate in mining pools(30k-100k adjusting reward thresholds).
- Locks the STX for specified time (10 days to 3 months).
- Provides BTC address to receive rewards.
- Votes on a Stacks chain tip.
- Native support for delegation available for those below stacking threshold to join a stacking pool.

---


### Phases of Stacking Algorithm 

1. Prepare Phase
2. Reward Phase

---

### Prepare Phase
<style>
code.blue {
  color: #337AB7 !important;
}
code.orange {
  color: #F7A004 !important;
}
</style>

- <code class="blue">Anchor Block Selection</code> -  Stacks chain block. Mining descendant forks of anchor block  requires transfering mining funds to reward address.

- <code class="blue"> Consensus on Reward set</code>-  Eligible Stackers BTC address ,Has to be agreed by network .

---

#### Anchor Block Selection

1. Require certain number of miner confirmations.
2. Anchor Block confirmed by **F*W** miner support.
```
F= large fraction or higher threshold 
W= Window of BTC blocks before reward cycle begins.
```
3. Secured by threshold t of valid Stacker support message signals.

---

### Reward Phase
  
1. Leader election by VRF and user-supported burns.
2. Leader sends committed BTC funds to burn address / reward address based on address selection rules.

---

#### Mining the next Block /Leader Election:
 Leader election with user-supported burns.
 
    Step 1:- Register a VRF public key
    Step 2: Commit STX chain tip , new VRF seed(M) , &Transfer
    Step 3:- If selected, broadcast VRF proof(P) & block
  
 Index sample with Mn=hash(Pn)
 Randomize order with POW nonce
 
---
 
#### Reward Address Fact :

- Receives funds when miner builds off descendant of anchor block.
- Per Block 5 address selected from reward set Using VRF.
- Once selected, reward address is removed from next sortition.

---

#### Address Validity Rules:

| Miner Action                                              | Funds to Burn address | Funds to Reward Address |
| --------------------------------------------------------- | --------------------- | ----------------------- |
| Building off any chain tip not descendant of anchor block | Yes                   |                         |
| Building off descendant of anchor block                   | No                    | Yes                     |

---

#### Facts of Reward cycle:

- Fixed Length.
- Each reward cycle may transfer miner funds to up to 5000 Bitcoin addresses
- Per block /Per sortition 5 address selected from reward set.
- Few Participating Address in Stacking than available slots -Remaining miner commitments sent to Burn address. 

---

#### Stacking Delegation:

- Allows a Stacks wallet address (the represented address) to designate another address (the delegate address) for participating in the Stacking protocol.
- Two new transaction types Delegate Funds and Terminate Delegation.
- Single STX address as Delegate for many represented STX address, then Broadcast Signed Stacking message/Each address.

---


### Rewards in Stacks 2.0: All rewards distributed post completion of reward cycle.

| Rewards                        | Miners Context | Stackers Context |
| ------------------------------ | -------------- | ---------------- |
| Block Rewards/New STX          | Yes            |                  |
| Clarity Fees                   | Yes            |                  |
| Transaction Fee                | Yes            |                  |
| BTC commitment funds of Miners |                | Yes              |
| User-supported burns rewards   | Yes            |                  |

---

###  Ongoing Research/Consolidations    
* Addressing Miner Consolidation
* Time-Bounded POX
```
   - Initial Phase
   - Sunset Phase
```
* Developer Fund
* Discounted Mining
* Bitcoin Bandwidth

---

## For the community. Made by the community :heart:

Get connected to the blockstack community through


- :computer: **GitHub** https://github.com/blockstack/
- :video_game: **Discord** https://discord.gg/TQebdvp
- :mailbox: **Telegram** @blockstack
- :bird: **Twitter** @blockstack / @blockstackr
- :pick: Interested to be a miner? Apply [here](https://blocksurvey.org/survey/1216tyLMMnobWmRDpGx2z33uUcwjww4kMm/65a3e307-5d43-45e4-ad64-5d791304a0d8) :point_up: 